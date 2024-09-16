# Summary MITRE ATT&CK Sequence

In this scenario, a healthcare application is targeted by an attacker using SQL injection (SQLi) techniques. The attacker begins with reconnaissance, identifying input fields in the application, such as login forms and search boxes, and uses automated tools to scan for vulnerabilities in the app's API endpoints. They then craft a malicious SQL query designed to exploit these vulnerabilities and deliver it by submitting the payload through the app's input fields. Once executed, the SQL injection allows the attacker to bypass authentication, gain unauthorized access to user accounts, and extract sensitive data, including patient records and prescriptions. The attack can lead to significant impacts, such as patient safety risks, privacy violations, financial losses, and reputational damage for the healthcare organization.

## Methodology

```mermaid
flowchart TD
    A[Reconnaissance] -->|Gather Information| B[Initial Access]
    B -->|Exploit Input Validation| C[Execution]
    C -->|Inject Malicious SQL Query| D[Exploitation]
    D -->|Bypass Authentication| E[Credential Access]
    E -->|Access Sensitive Data| F[Data Exfiltration]
    F -->|Extract Patient Records| G[Impact]
    G -->|Patient Safety Risks| H[Privacy Violations]

    classDef attack fill:#f96,stroke:#333,stroke-width:2px;
    classDef technique fill:#bbf,stroke:#333,stroke-width:2px;

    class A attack;
    class B attack;
    class C attack;
    class D attack;
    class E attack;
    class F attack;
    class G attack;
    class H technique;

    %% MITRE ATT&CK Techniques
    class A technique;
    class B technique;
    class C technique;
    class D technique;
    class E technique;
    class F technique;

    A -->|T1592.001: Gather Victim Identity Information| A1[Identify Input Fields]
    B -->|T1190: Exploit Public-Facing Application| B1[Deliver SQL Injection Payload]
    C -->|T1203: Exploitation for Client Execution| C1[Execute SQL Query]
    D -->|T1078: Valid Accounts| D1[Bypass Authentication]
    E -->|T1041: Exfiltration Over Command and Control Channel| E1[Access Sensitive Data]
    F -->|T1048: Exfiltration Over Alternative Protocol| F1[Extract Patient Records]
