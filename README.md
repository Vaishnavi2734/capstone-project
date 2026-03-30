 Capstone Project: End-to-End Digital Forensic Investigation

 Overview

This project presents a complete **Digital Forensic Investigation and Malware Analysis** conducted in a simulated enterprise environment. The objective is to investigate a suspected insider threat involving unauthorized access and potential data exfiltration using disk images, network captures, and a suspicious executable.


 Scenario

An organization suspects that an employee has exfiltrated confidential data. The investigation involves analyzing:

* Disk Image (user activity & deleted files)
* PCAP File (network communication)
* Suspicious Executable (malware behavior)

The goal is to identify evidence, correlate findings, and reconstruct the attack timeline.


 Tools Used

| Tool        | Purpose                        |
| ----------- | ------------------------------ |
| FTK Imager  | Evidence acquisition & hashing |
| Autopsy     | Disk forensic analysis         |
| Wireshark   | Network traffic analysis       |
| RegRipper   | Registry artifact extraction   |
| HashMyFiles | Hash verification              |
| PEStudio    | Static malware analysis        |
| FLOSS       | String extraction              |
| ANY.RUN     | Dynamic malware analysis       |
| Draw.io     | Timeline visualization         |
| Google Docs | Report documentation           |


 Investigation Workflow

1. Evidence Intake

* Verified SHA-256 hashes of disk image, PCAP, and executable
* Maintained chain-of-custody documentation


 2. Disk Image Analysis (Autopsy)

* Performed keyword search (*password*, *confidential*)
* Recovered deleted files
* Analyzed file activity timeline


 3. Network Traffic Analysis (Wireshark)

* Applied filters: DNS, HTTP, TCP
* Identified suspicious outbound connections
* Observed unusual communication patterns

 4. Registry Analysis (RegRipper)

* Extracted persistence mechanisms (Run keys)
* Identified recent file access and user activity
* Analyzed USB/device history

 5. Static Malware Analysis

* Identified file type and hash values
* Extracted suspicious strings (URLs, IPs)
* Verified detection via VirusTotal
* Created YARA rule for detection

 6. Dynamic Malware Analysis

* Observed process execution and behavior
* Detected registry modifications and file creation
* Identified outbound network communication
* Mapped behavior to MITRE ATT&CK techniques


  Unified Timeline (Attack Flow)

1. Suspicious file downloaded
2. Malware executed on system
3. Persistence established via registry
4. External network communication initiated
5. Potential data exfiltration occurred

 Key Findings

* Recovered deleted files containing sensitive information
* Detected suspicious outbound connections to external IPs
* Identified persistence mechanisms in registry
* Malware exhibited command-and-control (C2) behavior


 Deliverables

* Chain of Custody Document
* Autopsy Analysis Report + Screenshots
* Wireshark Traffic Analysis (.pcap + report)
* Registry Artifacts Report
* Static Malware Analysis + YARA Rule
* Dynamic Malware Analysis + MITRE Mapping
* Unified Timeline (Draw.io / Sheets)
* 300-word Forensic Investigation Report
* 150-word Stakeholder Summary



---
