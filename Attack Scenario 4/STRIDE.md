# STRIDE Framework Diagram

```mermaid
flowchart TD
    subgraph STRIDE
        direction TB
        A[**Spoofing**]
        B[**Tampering**]
        C[**Repudiation**]
        D[**Information Disclosure**]
        E[**Denial of Service**]
        F[**Elevation of Privilege**]
    end

    subgraph Techniques_and_Mitigations
        direction TB
        A1[Spoofing Techniques: Phishing, IP Spoofing]
        A2[Spoofing Mitigations: MFA, Strong Authentication]

        B1[Tampering Techniques: SQL Injection, XSS]
        B2[Tampering Mitigations: Input Validation, Escaping Data]

        C1[Repudiation Techniques: Log Tampering, Log Deletion]
        C2[Repudiation Mitigations: Secure Logging, Immutable Logs]

        D1[Information Disclosure Techniques: Data Leakage, Insecure Storage]
        D2[Information Disclosure Mitigations: Encryption, Access Controls]

        E1[Denial of Service Techniques: DDoS, Resource Exhaustion]
        E2[Denial of Service Mitigations: Rate Limiting, DDoS Protection]

        F1[Elevation of Privilege Techniques: Privilege Escalation, Exploits]
        F2[Elevation of Privilege Mitigations: Least Privilege, Regular Patching]
    end

    A --> A1
    A --> A2
    B --> B1
    B --> B2
    C --> C1
    C --> C2
    D --> D1
    D --> D2
    E --> E1
    E --> E2
    F --> F1
    F --> F2
