sequenceDiagram
    participant User
    participant SolariHealthApp
    participant BackendServer
    participant CnCServer
    participant Attacker

    %% Reconnaissance
    Attacker->>SolariHealthApp: Analyzes web interface for input fields
    Attacker->>SolariHealthApp: Scans API endpoints for vulnerabilities

    %% Weaponization
    Attacker->>Attacker: Crafts malicious SQL query

    %% Delivery
    Attacker->>SolariHealthApp: Submits SQL injection payload via login form or API

    %% Exploitation
    SolariHealthApp->>BackendServer: Passes input to BackendServer
    BackendServer->>BackendServer: Executes SQL query with injected payload
    BackendServer->>SolariHealthApp: Returns data or confirmation of access

    %% Installation
    BackendServer->>BackendServer: Creates new admin account or modifies user roles

    %% Command and Control (C2)
    BackendServer->>Attacker: Provides continuous access to database
    Attacker->>BackendServer: Sets up scripts or automated queries for ongoing access

    %% Actions on Objectives
    Attacker->>BackendServer: Extracts sensitive patient data
    Attacker->>BackendServer: Alters prescription details or appointment times
    Attacker->>BackendServer: Uses stolen information for identity theft

    %% Impact
    Note right of BackendServer: Patient safety risks, privacy violations, reputational damage, financial loss
