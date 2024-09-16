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

    H --> |Mitigate with Encryption & Authentication| O[Controls: HTTPS, Certificate Pinning]
    I --> |Mitigate with Secure Access Controls| P[Controls: Network Security, Wi-Fi Security Awareness]
    J --> |Mitigate with Encrypted Communication| Q[Controls: HTTPS, HSTS]
    K --> |Mitigate with Data Protection| R[Controls: Encryption, Secure Data Transmission]
    L --> |Mitigate with Secure Session Management| S[Controls: Session Expiration, MFA]
    M --> |Mitigate with Traffic Monitoring| T[Controls: Network Monitoring, Anomaly Detection]
    N --> |Mitigate with Fraud Detection & Incident Response| U[Controls: Monitoring, Incident Management]

    classDef stride fill:#f9f,stroke:#333,stroke-width:2px;
    classDef control fill:#ccf,stroke:#333,stroke-width:2px;
    class H,I,J,K,L,M,N stride;
    class O,P,Q,R,S,T,U control;
