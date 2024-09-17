# STRIDE Threat Modeling for DDoS Attack with Controls

```mermaid
flowchart TD
    %% Attack Stages
    A[Reconnaissance] --> B[Weaponization]
    B --> C[Delivery]
    C --> D[Exploitation]
    D --> E[Command and Control (C2)]
    E --> F[Actions on Objectives]

    %% STRIDE Threats
    G[Spoofing]
    H[Tampering]
    I[Repudiation]
    J[Information Disclosure]
    K[Denial of Service]
    L[Elevation of Privilege]

    %% Threats Linked to Stages
    A --> G
    B --> H
    C --> I
    D --> J
    E --> K
    F --> L

    %% Mitigation Controls
    M[Mitigation Controls]
    N[DDoS Protection Services]
    O[Rate Limiting]
    P[Traffic Monitoring]
    Q[Scalable Infrastructure]
    R[Redundancy]

    %% Linking Threats to Mitigations
    K --> N
    K --> O
    J --> P
    G --> R
    H --> R







