# STRIDE Threat Modeling for DDoS Attack with Controls

```mermaid
graph TD
    A[Reconnaissance]
    B[Weaponization]
    C[Delivery]
    D[Exploitation]
    E[Command and Control (C2)]
    F[Actions on Objectives]

    A --> B
    B --> C
    C --> D
    D --> E
    E --> F

    F --> G[DDoS Protection Services]
    F --> H[Rate Limiting]
    F --> I[Traffic Monitoring]
    F --> J[Scalable Infrastructure]
    F --> K[Redundancy]

    G --> F
    H --> F
    I --> F
    J --> F
    K --> F