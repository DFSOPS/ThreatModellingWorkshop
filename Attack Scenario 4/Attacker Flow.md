# DDoS Attack Scenario Sequence Diagram

```mermaid
sequenceDiagram
    participant Attacker
    participant User
    participant SolarisHealthApp
    participant BackendServer
    participant CnCServer

    %% Attacker prepares the botnet and attack
    Attacker->>CnCServer: Setup and configure botnet
    CnCServer->>Attacker: Botnet ready

    %% User is involved
    User->>SolarisHealthApp: Sends legitimate request

    %% Attacker starts the attack
    Attacker->>BackendServer: Flood with traffic
    BackendServer->>SolarisHealthApp: Overwhelmed with requests
    SolarisHealthApp->>BackendServer: Unresponsive or slow

    %% Attack continues with monitoring and control
    Attacker->>CnCServer: Monitor attack progress
    CnCServer->>Attacker: Provide updates

    %% User experiences issues
    User->>SolarisHealthApp: Encounters slow response or outage

    %% Defensive measures might be triggered
    SolarisHealthApp->>BackendServer: Attempt to mitigate attack
    BackendServer->>SolarisHealthApp: Responds to mitigation efforts
    SolarisHealthApp->>User: Communicate service disruption

    %% Attack continues until mitigated
    Attacker->>CnCServer: Adjust attack methods
    CnCServer->>Attacker: Confirm adjustments
