# STRIDE Threat Modeling for DDoS Attack with Controls

```mermaid
graph TD
    A[Reconnaissance] --> B[Weaponization]
    B --> C[Delivery]
    C --> D[Exploitation]
    D --> E[Command and Control (C2)]
    E --> F[Actions on Objectives]

    F --> G[DDoS Protection Services]
    F --> H[Rate Limiting]
    F --> I[Traffic Monitoring]
    F --> J[Scalable Infrastructure]
    F --> K[Redundancy]

    G --> E
    H --> E
    I --> E
    J --> E
    K --> E











