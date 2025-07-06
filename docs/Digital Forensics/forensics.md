# Digital Forensics

## The Investigation Process for Digital Forensics Science

### Identification

- Confirm that an incident or crime has taken place
- Sources of Identification
    - Victim Reports
    - Detections and controls
    - Audits
- Preparing to respond and collect evidence
    - Locating
    - Preserving
- Define scope and focus efforts accordingly

### Preservation

- Ensuring evidence remains intact and unaltered
    - The system is a crime scene.
- Capture a snapshot of the device's current state
    - Maintaining integrity
- Identifyingi relevant data
    - Data volatility (if a pc turned off the volatile data is deleted!)
    - Data location
- Chain of custody
    - Documenting the handling of evidence
    - Tracking everyone who's had possession of evidence
    - Document! (who, what, where, when, why?)
- Secure the evidence
    - Physical and digital security controls

### Collection

- Gather all of the identified evidence
    - Primary devices
    - Peripherals
- Legal authority
    - Warrant
    - Signed consent
    - Collection scope
- Volatility
    - Collect evidence before it's lost.
- Data reduction
- Documentation
    - Chain of custody
    - Labeling, documenting, verifying integrity

### Examination

- Inspect, analyze, and interpret evidence
    - Extract meaningful information from the data
    - Draw conclusions to support the investigation
- Maintain evidence integrity
    - Woring with forensic images of the data.
- Data extraction and interpretation
    - Translate raw data into workable, human-readable data
- Examination checklist
    - But not too specific
- Data Discovery
    - Hidden or deleted data
    - Fire carving, file extraction

### Analysis

- Interpret the evidence
    - How does the evidence support the hypothesis?
    - How does the evidence refute the hypothesis?
    - What does this information actually mean in the contex?
- Data context
    - Don't analyze in a vacuum
- Iteration
    - Analyze, ask new questions. re-analyze
- Relational Analysis
    - Links between people, places, and things
- Functional Analysis
    - How operational configurations relate to the incident
- Temporal Analysis
    - Timeline (sequences) or pattern analysis

### Presentation

- Communicate the results
    - Legal executive, desicion makes
- Ensure finding are communicated clearly
    - Understood by all technical backgrounds
- Guide the audience through the investigation
    - Let the evidence draw conclusions
- Executive summaries
    - Key results
    - Significant findings
    - Clear explanations

### Decision

- Evaluate the results
- Make a decision
    - Are the evidence and conclusions sufficient?
    - Is more investigaiton required?
- Prosecution
    - Building up a legal case
    - Expert testimony

### Data Acquisition

- Evidence
    - Data that supports or refutes an investigative hypothesis
    - Digital Forensic artifacts
    - Evidence is circumstantial
    - Evidence is volatile
- Evidence Sources
    - Desktops and Laptops
    - Smartphones and Tablets
    - Hard Drives and External Storage
    - Servers and Virtual Machines
    - Network Devices
    - Cloud Services

### The Order of Volatility

- CPU Registers and Cache
    - Processor registers
        - Fast storage
        - Memory built directly into the CPU
        - Holds instructions, storage addresses, etc.
    - Cache memory
        - Returns frequently used instructions and data
        - Helps the CPU process quicker
    - Running Processes
        - Programs or binaries currently running on the system
        - Paths, command-line invocations, PIDs, hierarchy
- RAM and Active Network Connections
    - Random Access Memory
        - Short-lived data storage
        - Session data, unsaved documents, process data
    - Network Connections
        - TCP/UDP connections
        - Open ports
    - Routing Table
        - Lists the pathways to network destinations
    - ARP Cache
        - Maps IP addresses to MAC addresses
- Temp Files and System Logs
    - Temporary files
        - Downloads, temporary configurations
        - %TEMP%
        - C:\Windows\Temp
        - /tmp
    - Swap Files
        - Temporary memory space allocated on disk
    - System and application logs
        - Can be overwritten or cleared
- Disk Storage Data
    - Hard Disk Drives
    - Solid State Drives
        - Garbage collections
        - TRIM
    - System configurations
        - Operating system components
        - Installed software
        - User files, configurations, and preferences
        - Documents, executables, backups
- Remote Logging
    - Endpoint telemetry
        - System, security, application logs, etc
        - Historical events
        - Processes, network connections, DNS queries, services
    - Centralized log collection
        - Logging server, SIEM, cloud storage
        - Replicated
        - Centralized
        - Log rotation policies
- Archive Media
    - Long-term Storage Media
        - Backup tapes
        - Optical disks (CDs, DVDs, Blu-rays)
        - Archival hard drives
        - Cloud-based archival storage
    - Backup
        - Files
        - Databases
    - Security Controls
        - Confidentiality
        - Integrity
        - Availability

### Forensic Data Integrity

- Write Blockers
    - Preserving the integrity of storage and devices
    - Hardware or software
    - Prevents any write commands that could alter data
    - Analysis should be conducted on forensic images
- Evidence Bags
    - Contain and protect evidence
    - Tamper-resistant / Tamper-evident
    - Label for documenting case information
- Legal Holds
    - Litigation Hold
    - Preserve relevant case data until resolution
- Documentation
    - Collection procedure, tools, condition, observations

### Chain of Custody

- Tracks evidence throughout the entire investigation
    - From analysis to presentation
- Documents evidence possession
    - Stakeholders, law enforcement, investigators, examiners
    - Whenever evidence transfer, a chain of custody entry must be signed
- Storage conditions
    - Date
    - Time reason
    - Sending and receiving parties

### Common Windows Forensic Artifacts

%SYSTEMROOT%\System32\Config

| Default  | HKEY_USERS.Default           |
| -------- | ---------------------------- |
| SAM      | HKEY_LOCAL_MACHINE\SAM       |
| SECURITY | HKEY_LOCAL_MACHINE\SECURITY  |
| SOFTWARE | HKEY_LOCAL_MACHINE\SOFTWARE  |
| SYSTEM   | HKEY_LOCAL_MACHINE\SYSTEM    |

%USERPROFILE%

| NTUSER.DAT | HKEY_CURRENT_USER      |
| ---------- | ---------------------- |
| SAM        | HKEY_LOCAL_MACHINE\SAM |
