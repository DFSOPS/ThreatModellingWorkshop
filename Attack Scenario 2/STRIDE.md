# SQL Injection Attack Controls - STRIDE Mapping

```mermaid
graph TD
    A[SQL Injection Controls] --> B[Spoofing]
    B --> B1[User Access Controls]
    
    A --> C[Tampering]
    C --> C1[Input Validation]
    C --> C2[Parameterized Queries]
    
    A --> D[Repudiation]
    D --> D1[Monitoring and Logging]
    
    A --> E[Denial of Service]
    E --> E1[Web Application Firewall]
    
    A --> F[Information Disclosure]
    F --> F1[Regular Security Audits]
