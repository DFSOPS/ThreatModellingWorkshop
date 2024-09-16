```mermaid
sequenceDiagram
    participant Attacker
    participant SolarisHealthApp
    participant BackendServer
    participant CnCServer
    participant User

    %% Reconnaissance
    Attacker->>SolarisHealthApp: Analyzes web interface and scans API endpoints

    %% Weaponization
    Attacker->>Attacker: Crafts malicious SQL payload

    %% Delivery
    Attacker->>SolarisHealthApp: Submits SQL injection payload via login form or API

    %% Exploitation
    SolarisHealthApp->>BackendServer: Passes input to BackendServer
    BackendServer->>BackendServer: Executes SQL query with injected payload
    BackendServer->>SolarisHealthApp: Returns data or access confirmation

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
