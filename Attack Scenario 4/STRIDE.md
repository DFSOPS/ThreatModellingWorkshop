# STRIDE Threat Modeling for DDoS Attack with Controls

```mermaid
graph TD
    A[Reconnaissance] -->|Spoofing| G[Spoofing]
    B[Weaponization] -->|Tampering| H[Tampering]
    C[Delivery] -->|Repudiation| I[Repudiation]
    D[Exploitation] -->|Information Disclosure| J[Information Disclosure]
    E[Command and Control (C2)] -->|Denial of Service| K[Denial of Service]
    F[Actions on Objectives] -->|Elevation of Privilege| L[Elevation of Privilege]

    K -->|Mitigation| M[DDoS Protection Services]
    K -->|Mitigation| N[Rate Limiting]
    J -->|Mitigation| O[Traffic Monitoring]
    K -->|Mitigation| P[Scalable Infrastructure]
    K -->|Mitigation| Q[Redundancy]









