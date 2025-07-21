# Explanations on Logs

## Types of Logs

### :material-arrow-right: System Logs

- The system logs can be helpful in troubleshooting running issues in the OS. These logs provide information on various operating system activities.
- Windows Event Logs, Sysmon Logs and Linux/Unix Syslogs
    - System Startup and shutdown events
    - Driver Loading events
    - System Error events
    - Hardware events

### :material-arrow-right: Security Logs

- The security logs help detect and investigate incidents. These logs provide information on the security-related activities in the system.
- Authentication Logs, IDS/IPS Logs, Endpoint Security Logs
    - Authentication events
    - Authorization events
    - Security Policy changes events
    - User Account changes events - Abnormal Activity events

### :material-arrow-right: Application Logs

- The application logs contain specific events related to the application. Any interactive or non-interactive activity happening inside the application will be logged here.
- App Logs
    - User Interaction events
    - Application Changes events
    - Application Update events
    - Application Error events

### :material-arrow-right: Audit Logs

- The Audit logs provide detailed information on the system changes and user events. These logs are helpful for compliance requirements and can play a vital role in security monitoring as well.
- Audit Trail Logs
    - Data Access events
    - System Change events
    - User Activity events
    - Policy Enforcement events

### :material-arrow-right: Network Logs

- Network logs provide information on the network’s outgoing and incoming traffic. They play crucial roles in troubleshooting network issues and can also be handy during incident investigations.
- Firewall Logs, Proxy Logs, DNS Logs
    - Incoming Network Traffic events
    - Outgoing Network Traffic events
    - Network Connection Logs

### :material-arrow-right: Access Logs

- The Access logs provide detailed information about the access to different resources. These resources can be of different types, providing us with information on their access.
- Database Logs, Web Server / HTTP Logs, API Logs
    - Webserver Access Logs
    - Database Access Logs - Application Access Logs
    - API Access Logs

## Log Formats

- Unstructured Logs
    - No predefined format or syntax
- Semi-Structure Logs
    - Some syntax structure
    - Lack adherence to a schema
    - Syslog
    - Windows Event Log (EVT)
- Structured Logs
    - Well-defined syntax and formatting
    - Adherence to an agreed upon schema
    - CSV, TSV
    - Javascript Object Notation  (JSON)
    - eXtensible Markup Language (XML)
