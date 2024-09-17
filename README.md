Threat Modeling Workshop Overview
=================================

Introduction
------------

A 3-hour threat modeling workshop was conducted to analyze the runbook scenarios involving various AI-driven attacks targeting the web-based healthcare application, Solaris Care Connect 360.

Attendees
---------

The workshop included members from the Care Connect Engineering team, Product Managers, DevEx Engineers, and the DevSecOps team.

Scope
-----

The workshop covered four scenarios: (1) AI-generated phishing emails exploiting admin credentials, (2) Attacks on machine processes and the data lake, (3) SQL injection attacks, and (4) Insider threats involving theft of quantitative algorithms.

Methodology
-----------

Each scenario was evaluated using the cyber attack kill chain, along with the MITRE ATT&CK framework and STRIDE methodology for assessing control gaps, resulting in the identification of key risks.

Conclusion
----------

The threat modeling session identified a total of 5 high-risk vulnerabilities.

Required Controls
-----------------

-   Conduct regular security audits using the Application Security Verification Standard (ASVS) to identify vulnerabilities and weaknesses specific to the Solaris Health 360 application.
-   Implement a patch management process to keep the Solaris Health 360 application and its associated technologies updated and protected from known vulnerabilities.
-   Provide comprehensive training for employees on phishing awareness to help users of Solaris Health 360 recognize and report suspicious emails.
-   Deploy a Web Application Firewall (WAF) customized for the Solaris Health 360 application's traffic to monitor and block malicious requests.
-   Implement Multi-factor Authentication (MFA) to strengthen authentication measures and prevent unauthorized access to the Solaris Health 360 application.
-   Continuously monitor network traffic to detect and address any suspicious activity within the Solaris Health 360 application's infrastructure.
-   Apply Role-based Access Control (RBAC) within the Solaris Health 360 application to restrict access to sensitive health data and functionalities based on user roles and permissions.

# Threat Modelling Process Summary

```mermaid
mindmap
  root((Attack Begins))
    STRIDE/MITRE ATT&CK/Kill Chain
      Conduct Inherent Risk Assesment
      ::icon(fa fa-book)
      Create Critical Asset List
        Schedule and Scope Threat Modelling Workshop
    Controls Required
      Risks<br/>Mitigations
      Risk Summary
        Redmeiation workflow
            Slack
            JIRA 
    Attack Scenarios
      Attack 1
      Attack 2
      Attack 3
      Attack 4

