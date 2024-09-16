```mermaid
sequenceDiagram
    participant User
    participant SolarisHealthApp
    participant BackendServer
    participant CnCServer
    participant Attacker

    User->>SolarisHealthApp: Enters credentials
    SolarisHealthApp->>BackendServer: Sends login request
    BackendServer->>SolarisHealthApp: Validates credentials
    alt Valid credentials
        SolarisHealthApp->>User: Login successful
    else Invalid credentials
        SolarisHealthApp->>User: Login failed
    end

    User->>SolarisHealthApp: Requests prescription data
    SolarisHealthApp->>BackendServer: Fetches prescription data
    BackendServer->>SolarisHealthApp: Returns prescription data
    SolarisHealthApp->>User: Displays prescription data

    User->>SolarisHealthApp: Clicks on malicious link
    SolarisHealthApp->>Attacker: Sends SQL injection payload
    Attacker->>CnCServer: Sends stolen credentials
    CnCServer->>BackendServer: Executes malicious queries
    BackendServer->>CnCServer: Returns sensitive data
    CnCServer->>Attacker: Sends sensitive data
