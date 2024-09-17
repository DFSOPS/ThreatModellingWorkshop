# STRIDE Threat Modeling for DDoS Attack with Controls

```mermaid
flowchart TD
    A[Reconnaissance]
    B[Weaponization]
    C[Delivery]
    D[Exploitation]
    E[Command and Control (C2)]
    F[Actions on Objectives]

    G[Spoofing]
    H[Tampering]
    I[Repudiation]
    J[Information Disclosure]
    K[Denial of Service]
    L[Elevation of Privilege]

    M[Mitigation Controls]
    N[DDoS Protection Services]
    O[Rate Limiting]
    P[Traffic Monitoring]
    Q[Scalable Infrastructure]
    R[Redundancy]

    %% Attacks linked to stages
    A --> G
    B --> H
    C --> I
    D --> J
    E --> K
    F --> L

    %% Mitigations linked to threats
    K --> N
    K --> O
    J --> P
    K --> Q
    K --> R







