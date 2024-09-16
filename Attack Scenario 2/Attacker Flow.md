```mermaid
sequenceDiagram
    participant User
    participant SolariHealthApp
    participant BackendServer
    participant CnCServer
    participant Attacker

    User->>SolariHealthApp: Enters credentials
    SolariHealthApp->>BackendServer: Sends login request
    BackendServer->>SolariHealthApp: Validates credentials
    alt Valid credentials
        SolariHealthApp->>User: Login successful
    else Invalid credentials
        SolariHealthApp->>User: Login failed
    end

    User->>SolariHealthApp: Requests prescription data
    SolariHealthApp->>BackendServer: Fetches prescription data
    BackendServer->>SolariHealthApp: Returns prescription data
    SolariHealthApp->>User: Displays prescription data

    User->>SolariHealthApp: Clicks on malicious link
    SolariHealthApp->>Attacker: Sends SQL injection payload
    Attacker->>CnCServer: Sends stolen credentials
    CnCServer->>BackendServer: Executes malicious queries
    BackendServer->>CnCServer: Returns sensitive data
    CnCServer->>Attacker: Sends sensitive data
