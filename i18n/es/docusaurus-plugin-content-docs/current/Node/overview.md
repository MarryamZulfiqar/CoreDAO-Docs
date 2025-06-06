---
sidebar_label: Tipos de nodos
hide_table_of_contents: false
sidebar_position: 2
---

# Nodos en el ecosistema central

---

En el ecosistema Core, la solidez, la seguridad y la descentralización de la red están respaldadas por los nodos operados por los participantes de la comunidad. Estos nodos facilitan diversas funciones, desde la validación de transacciones hasta la propagación de bloques, garantizando la salud y eficiencia generales de la red.

Según tus objetivos, existen diferentes configuraciones de nodos posibles en la red de Core. Si aún no has iniciado ningún nodo en la red de Core, revisa la documentación para [Ejecutar un Nodo Validador Local](./validator/setting-up-validator.md) antes de proceder con diferentes configuraciones.

- **Si deseas participar en la gobernanza de la Red Core**

    - [**Inicia un Nodo Validador**](./config/validator-node-config.md)

- **Si deseas ejecutar un nodo en la red Core para uso privado**
    - [**Inicia un nodo completo normal**](./config/full-node.md)

- **Si deseas enviar transacciones o consultar la cadena directamente desde tu propio nodo de la blockchain Core**

    - [**Iniciar un nodo RPC**](./config/rpc-node-config.md)

- **Si deseas solicitar datos históricos de la cadena desde el bloque génesis**

    - [**Iniciar un nodo de arhivo**](./config/archive-node-config.md)

- **Si desea ayudar a los operadores de nodos a sincronizarse rápidamente con la red**

    - [\*\*Iniciar un nodo de snapshot](./config/snapshot-node-config.md)

## Tipos de nodos en la red Core

1. **Validadores:**
    - **Rol:** Los validadores son cruciales para proteger la red mediante la producción de bloques y la validación de transacciones dentro del marco de consenso de la cadena Core.
    - **Requisitos:** Los validadores deben hacer staking de una cantidad mínima de **10,000 tokens CORE** para participar, alineando sus incentivos financieros con el rendimiento y la seguridad de la red.
    - **Incentivos:** Los validadores obtienen recompensas en tokens CORE por su papel activo en el mantenimiento y seguridad de las operaciones de la red.

2. **Nodos completos normales:**
    - **Rol:** Los nodos completos normales mantienen una copia completa y en tiempo real del libro mayor de blockchain, validan transacciones y respaldan la red transmitiendo datos de bloques y transacciones. Estos son esencialmente útiles para uso privado.
    - **Requisitos:** Operar un nodo completo requiere importantes recursos computacionales y de almacenamiento para manejar los datos completos de la cadena de bloques y el tráfico continuo de la red.

3. **Nodos RPC:**
    - **Rol:** Los nodos RPC proporcionan una interfaz de programación de aplicaciones (API) para que los desarrolladores y aplicaciones externas interactúen con la cadena de bloques, facilitando consultas y transacciones.
    - **Importancia:** Son esenciales para el desarrollo y operación de aplicaciones descentralizadas (DApps) y para el acceso externo a los datos de blockchain.

4. **Nodos de archivo:**
    - **Función:** Los nodos de archivo almacenan el historial completo de la cadena de bloques, incluidos todos los estados y transacciones desde el bloque de génesis, lo que proporciona un recurso valioso para consultas históricas profundas.
    - **Requisitos:** Estos nodos requieren una gran capacidad de almacenamiento, ya que mantienen todos los estados actuales y vencidos de la cadena de bloques, lo que los hace consumir muchos recursos.
    - **Uso:** Los nodos de archivo son cruciales para los desarrolladores que necesitan acceso a todos los datos históricos de blockchain para análisis, auditorías y consultas avanzadas de blockchain.

5. **Nodo snapshot:**
    - **Función:** Los nodos snapshot mantienen capturas de la blockchain en varios intervalos. Estas capturas incluyen el estado de la cadena de bloques a una altura de bloque determinada, lo que ofrece un punto de restauración para nodos completos o nodos nuevos.
    - **Beneficios:** Proporcionan un medio para una rápida sincronización y recuperación de otros nodos en la red, mejorando la resiliencia y escalabilidad de la infraestructura de la red.

## Importancia de cada tipo de nodo

- **Validadores** garantizan la validez de las transacciones y el consenso de la red.
- Los **nodos completos** y los **nodos de archivo** proporcionan redundancia e integridad de datos.
- Los **Nodos RPC** permiten el desarrollo de aplicaciones y la interacción con la cadena de bloques.
- **Nodos snapshot** ayudan a escalar la red eficientemente y a sincronizar los nodos más rápido.

## Conclusión

Las diversas funciones de los nodos en el ecosistema Core garantizan colectivamente que la cadena de bloques sea segura, eficiente, accesible y robusta. Los validadores, los nodos completos y los nodos de archivo forman la columna vertebral de la seguridad y la integridad de los datos de la red. Al mismo tiempo, los nodos RPC y los nodos snapshot brindan flexibilidad, accesibilidad y escalabilidad. Esta arquitectura de nodo multifacética admite una amplia gama de operaciones, desde el procesamiento de transacciones hasta interacciones complejas de dApps y análisis de datos históricos.