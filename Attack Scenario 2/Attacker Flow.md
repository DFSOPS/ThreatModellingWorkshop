flowchart TD
    A[User] -->|Receives phishing email| B[Attacker]
    B -->|Creates fake login page| C[SolariHealthApp]
    A -->|Clicks on link| C
    C -->|Enters credentials| B
    B -->|Sends credentials to| D[CnCServer]
    D -->|Gains access to| E[BackendServer]
    E -->|Manipulates data| F[SolariHealthApp]
    F -->|Data Theft/Manipulation/Identity Theft| A

    style A fill:#ffcccc,stroke:#333,stroke-width:2px;
    style B fill:#ff6666,stroke:#333,stroke-width:2px;
    style C fill:#66ccff,stroke:#333,stroke-width:2px;
    style D fill:#ffcc66,stroke:#333,stroke-width:2px;
    style E fill:#66ff66,stroke:#333,stroke-width:2px;
    style F fill:#ff99ff,stroke:#333,stroke-width:2px;
