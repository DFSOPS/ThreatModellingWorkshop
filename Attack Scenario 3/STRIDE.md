# STRIDE threat modeling framework for the Man-in-the-Middle (MitM) attack scenario

```mermaid
flowchart TD
    A[Reconnaissance] --> B[Weaponization]
    B --> C[Delivery]
    C --> D[Exploitation]
    D --> E[Installation]
    E --> F[Command and Control]
    F --> G[Actions on Objectives]

    A --> |Identify vulnerabilities| H[STRIDE: Spoofing]
    B --> |Setup rogue access point| I[STRIDE: Spoofing, Tampering]
    C --> |Intercept traffic| J[STRIDE: Eavesdropping, Tampering]
    D --> |Capture or modify data| K[STRIDE: Tampering, Information Disclosure]
    E --> |Maintain persistence| L[STRIDE: Tampering, Repudiation]
    F --> |Establish covert channel| M[STRIDE: Eavesdropping, Tampering]
    G --> |Exfiltrate data, commit fraud| N[STRIDE: Information Disclosure, Tampering, Repudiation]

    classDef stride fill:#f9f,stroke:#333,stroke-width:2px;
    class H,I,J,K,L,M,N stride;
