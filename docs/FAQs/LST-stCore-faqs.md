---
sidebar_label: Liquid Staking (stCORE) FAQs
hide_table_of_contents: false
sidebar_position: 2
---

# Liquid Staking (stCORE) FAQs
---

### 1. What is stCORE?
stCORE is an innovative solution on the Core blockchain designed to enhance the utility of CORE tokens by introducing liquid staking. This allows CORE token holders to maximize the potential of their assets with increased flexibility and efficiency. The process involves staking CORE tokens to secure the network and simultaneously gaining liquidity through minting stCORE tokens, which can be utilized in various DeFi protocols.

### 2. What are the benefits of liquid staking with stCORE?
Liquid staking with stCORE allows CORE token holders to participate in DeFi protocols while their assets are staked. This enhances asset utility and potential yield generation without compromising the security contributions to the network.

### 3. What is the redemption period for stCORE?
A **7-day** unlocking period is required by default for withdrawing CORE after redemption initiation.

### 4. How are validators chosen on mint/redeem?

Note that whenever mint/redeem happens, the `Earn` contract delegates CORE to `PledgeAgent` / undelegates CORE from `PledgeAgent`. This is implemented in a way that keeps the bookkeeping simpler.

When calling the `mint()` method, the caller needs to pass in a validator address to stake the CORE tokens to - by doing so, we hope to treat all validator candidates equally, no matter whether they are already elected or queued. However, in order to improve user experiences, we may have the official frontend to randomly choose a proper validator and make it unseen for users.  

During redeem, the `Earn` contract chooses validators randomly -  `_randomIndex()`, an index will be randomly selected, which is used as the start index to iterate through the validators array until enough CORE tokens are undelegated.

### 5. How to maintain a balanced distribution of validators across staking amounts?

Every time when
* A mint happens, the caller can choose a validator freely
* A redeem happens, and the system picks validators randomly

This mechanism ensures that the CORE tokens held by the Earn module can be distributed evenly among different validators.

However, considering there are cases, the balance will be disrupted by certain operations, e.g., large-value mint/redeem. We also introduced a few methods to rebalance stakings to validators from Earn.
* **rebalance():** The system selects the validators with the largest and smallest staking amounts and ensures they break even if the gap exceeds the predefined threshold.  
* **manualRebalance():** The operator manually transfers staking from one validator to another.

### 6. How is the conversion ratio calculated?

In every round after the turn round happens, the Earn module fetches rewards from each validator and delegates them back correspondingly. This is how it does auto-compounding internally. During this period, the system also transfers staking from inactive or jailed validators to active ones to improve the overall APR.

Additionally, the conversion ratio of stCORE/CORE can also be updated afterward. The formula for that is

```
    Amount of CORE tokens staked on PledgeAgent / stCORE.totalsupply()
```

Since **rewards claiming only happens once per day**, in such a design, the conversion rate can be kept the same throughout the day until the next turn round happens.

The above logics are implemented in the `afterTurnRound()` method.

### 7. How to handle the dues protection when delegating or undelegating?

Note that in the `PledgeAgent` contract (the staking contract), when users delegate

* The amount of CORE **must** >= 1

And when they undelegate

* The amount of CORE **must** >= 1 **AND**
* The remaining CORE left on a validator of this address **must** >= 1

When handling delegate/undelegate operations internally, the `Earn` module must also adhere to the same restrictions.

The implementation and case elaborations are in the `_undelegateWithStrategy()` method.

When calling the `mint()` method, the caller needs to pass in a validator address to stake the CORE tokens to - by doing so, we hope to treat all validator candidates equally, no matter whether they are already elected or queued. However, in order to improve user experiences, we may have the official frontend to randomly choosing a proper validator and make it unseen for users.  

During redemption, the Earn contract chooses validators randomly using ` randomIndex()`, where an index is randomly selected to serve as the start index for iterating through the validators array until enough CORE tokens are undelegated.