# STRIDE Threat Modeling for DDoS Attack with Controls

```mermaid
flowchart TD
    A[Reconnaissance] --> B[Weaponization]
    B --> C[Delivery]
    C --> D[Exploitation]
    D --> E[Command and Control (C2)]
    E --> F[Actions on Objectives]

    G[Spoofing] --> A
    H[Tampering] --> B
    I[Repudiation] --> C
    J[Information Disclosure] --> D
    K[Denial of Service] --> E
    L[Elevation of Privilege] --> F

    M[Mitigation Controls]
    N[DDoS Protection Services] --> K
    O[Rate Limiting] --> K
    P[Traffic Monitoring] --> J
    Q[Scalable Infrastructure] --> K
    R[Redundancy] --> K








