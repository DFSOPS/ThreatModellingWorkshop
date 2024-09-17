# STRIDE Threat Modeling for MitM Attack

```mermaid
graph TD
    %% STRIDE Categories
    S[STRIDE Threats] --> Spoofing[Spoofing Identity]
    S --> Tampering[Tampering with Data]
    S --> Repudiation[Repudiation]
    S --> InformationDisclosure[Information Disclosure]
    S --> DenialOfService[Denial of Service]
    S --> ElevationOfPrivilege[Elevation of Privilege]

    %% Spoofing Scenario
    Spoofing -->|Vulnerable Wi-Fi Access Point| MitMSpoofing[MitM: Attacker Spoofs Access Point]
    
    %% Tampering Scenario
    Tampering -->|Modify Communications| MitMTampering[MitM: Data Modification during Transit]
    
    %% Repudiation Scenario
    Repudiation -->|Log Alteration| MitMRepudiation[MitM: No Evidence of Attack]
    
    %% Information Disclosure Scenario
    InformationDisclosure -->|Intercept Sensitive Data| MitMDisclosure[MitM: Stealing Credentials, Medical Data]
    
    %% Denial of Service Scenario
    DenialOfService -->|Flood Requests| MitMDoS[MitM: Disrupting Service by Overloading Network]
    
    %% Elevation of Privilege Scenario
    ElevationOfPrivilege -->|Session Hijacking| MitMEoP[MitM: Gaining Unauthorized Access]
