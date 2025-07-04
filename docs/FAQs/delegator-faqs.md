---
sidebar_label: Delegator FAQs
hide_table_of_contents: false
sidebar_position: 2
---

# Delegator FAQs
---

### 1. What is a delegator on the Core blockchain?

In the Core ecosystem, delegation is a fundamental mechanism that enables Bitcoin miners and Bitcoin and CORE token holders to participate actively in the network's security and governance without requiring them to be validators themselves. This process involves the delegators entrusting their voting and operational power to validators, who then use the delegated resources (Bitcoin hash power, Bitcoin, and CORE) to participate in the network's consensus process and governance decisions.

### 2. What are the different types of delegations that can be done on Core due to the Satoshi Plus Consensus Mechanism?

1. **Bitcoin/CORE Delegation to Validators:** This type of delegation allows Bitcoin and CORE token holders to support specific validators by staking and delegating their tokens to them. In return, validators use the aggregated power to secure the network, validate transactions, and produce blocks. Delegators share in the rewards earned by their chosen validators, receiving a portion of the transaction fees and block rewards in proportion to their stake.
2. **Hash Power Delegation from Bitcoin Miners:** Bitcoin miners can delegate a portion of their computational hash power to validators on the Core network. This unique form of delegation leverages the security and work already being done on the Bitcoin network to enhance the security of the Core blockchain.

### 3. How can one delegate CORE tokens in Core?

By delegating CORE to Validators, CORE holders can help secure the network and share in system rewards. Please refer to the detailed [guide](../stake-and-delegate/CORE-staking.md) on CORE Delegation for more details.

### 4. What are the benefits of delegating Bitcoin or CORE tokens?

This type of delegation allows Bitcoin and CORE token holders to support specific validators by delegating their tokens to them. In return, validators use the aggregated power to secure the network, validate transactions, and produce blocks. Delegators share in the rewards earned by their chosen validators, receiving a portion of the transaction fees and block rewards in proportion to their stake.

### 5. How does one delegate hash power on the Core network?

By delegating hash power to Validators, Bitcoin miners can help secure the network and share in system rewards. Please refer to the detailed [guide](../stake-and-delegate/delegating-hash.md) on hash power delegation for more details.

### 6. How can a delegator maximize their rewards?

To maximize their rewards, delegators will look for both validators who are generous in their payouts and also don’t already have a substantial amount of delegated CORE tokens or delegated Proof-of-Work (PoW). The less a given validator has staked, the greater a contribution from a delegator will be. If a delegator adds one CORE token to a validator that only has one token, they’re 50% of that validator’s total delegation. If they delegate to a validator with 99 CORE tokens, they’re only 1% of that validator’s total delegation. Since payouts are determined in part by the percentage of the total stake each delegator accounts for, they’ll be incentivized to try to find validators with small delegations.

### 7. Can you change your validator once you have delegated?
- **Hash Power:** hash is delegated separately in each Bitcoin block mined, and once delegated, no further transfer can be made.

- **Bitcoin Delegation:** Users lock up their Bitcoin and designate a validator to stake on Core. They can transfer Bitcoin stake to other validators on Core, but will lose the rewards of the current day.

- **CORE Delegation:** Users can transfer to other validators and will still receive the rewards of the current day.

### 8. Are there any fees associated with delegating Bitcoin or CORE tokens or hash power?

Except for the transaction fee and gas charges, Core doesn’t charge any additional fees for delegating Bitcoin hash power, Bitcoin, or CORE tokens.

### 9. How long does it take to start earning rewards after delegating Bitcoin, CORE, or Bitcoin hash power?

- **Bitcoin hash power delegators:** The Core blockchain uses Bitcoin network block records from seven days ago for hybrid score calculations. Additionally, after a validator is elected, staking rewards are distributed on the second day of the switched round. Therefore, after delegating their hash power, miners and mining pools will have their hash power used in the Validator election calculation N+7 days later and will receive claimable rewards N+8 days later.

- **CORE/Bitcoin delegators:** After delegating their CORE/Bitcoin, delegators will have their assets used in the Validator election calculation for the next round. They will have claimable rewards a round later.

### 10. How can delegators claim their rewards?

Refer to the detailed guide [here](../stake-and-delegate/CORE-staking.md#claiming-rewards) on Claiming Rewards earned through staking of Bitcoin and CORE. In case of Bitcoin hash power delegation, refer [here](../stake-and-delegate/delegating-hash#implementation).

### 11. When are the rewards paid out?

The rewards are paid out at the end of each consensus round on the Core blockchain.

### 12. What happens if a validator stops performing or is penalized?

Poor performance or misconduct by validators can result in penalties like slashing of stakes and jailing. Note that delegators will not lose their staked assets; the penalties on validators will only affect the delegator's daily rewards.