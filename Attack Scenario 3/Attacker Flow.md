## M-I-T-M
```mermaid
sequenceDiagram
    participant Attacker
    participant User
    participant SolarisHealthApp
    participant BackendServer
    participant CnCServer

    User->>+SolarisHealthApp: Log in and request prescription details
    SolarisHealthApp->>BackendServer: Send user credentials and request data
    Attacker->>+User: Intercept user communication via MitM
    User->>Attacker: Sends login credentials
    Attacker->>+BackendServer: Relay credentials and modify request
    BackendServer->>SolarisHealthApp: Return prescription and payment data
    SolarisHealthApp->>User: Send prescription and payment data
    Attacker->>+CnCServer: Exfiltrate user credentials and payment data
    User->>SolarisHealthApp: Make payment
    Attacker->>BackendServer: Modify payment details (if possible)
    BackendServer->>Attacker: Confirm payment
    BackendServer->>User: Confirm legitimate payment
    Attacker->>CnCServer: Exfiltrate sensitive data to CnC
