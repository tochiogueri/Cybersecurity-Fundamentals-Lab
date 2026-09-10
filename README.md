# Cybersecurity Fundamentals Lab

A hands-on cybersecurity home lab documenting my progression from core networking and system administration to vulnerability assessment, incident response, and security automation.

> **Status:** In progress — repository structure created and Phase 1 planned.

## Project goals

- Build and document an isolated virtual cybersecurity lab.
- Strengthen practical networking, Linux, and Windows administration skills.
- Configure Windows Server, Active Directory Domain Services, DNS, DHCP, users, groups, and Group Policy.
- Capture and analyse network traffic using Wireshark.
- Perform authorised host discovery and vulnerability assessments with tools such as Nmap.
- Investigate simulated security events and document an incident-response workflow.
- Develop small Python tools that automate repeatable security tasks.
- Present clear evidence, findings, and remediation recommendations for each phase.

## Planned lab environment

| Component | Purpose |
|---|---|
| VirtualBox or VMware | Run the isolated virtual machines |
| Windows Server 2022 | Domain controller, AD DS, DNS and DHCP |
| Windows 10/11 | Domain-joined client |
| Linux | Administration and security tooling |
| Cisco Packet Tracer | Routing, switching and VLAN practice |
| Wireshark | Packet capture and protocol analysis |
| Nmap | Authorised network discovery and assessment |
| Python | Security automation |

## Project roadmap

| Phase | Focus | Status |
|---|---|---|
| 1 | Networking fundamentals and lab design | In progress |
| 2 | Windows Server and Active Directory | Planned |
| 3 | Network monitoring and traffic analysis | Planned |
| 4 | Vulnerability assessment and remediation | Planned |
| 5 | Incident response investigation | Planned |
| 6 | Python security automation | Planned |

## Repository structure

```text
Cybersecurity-Fundamentals-Lab/
├── docs/                    # Architecture, decisions and project documentation
├── evidence/                # Sanitised screenshots and supporting evidence
├── phases/                  # Phase-by-phase lab work
├── scripts/                 # Security automation scripts
├── .gitignore
├── LICENSE
├── SECURITY.md
└── README.md
```

## Documentation approach

Each practical exercise will record:

1. Objective and relevant security concept
2. Lab environment and network configuration
3. Implementation steps
4. Sanitised screenshots or command output
5. Validation and test results
6. Problems encountered and troubleshooting
7. Security findings and recommended remediation
8. Skills demonstrated

## Current work

Phase 1 begins with designing an isolated network, creating an IP addressing plan, and documenting the intended lab architecture before deploying virtual machines.

## Ethics and safety

All scanning, testing, and simulated attacks in this repository are limited to systems I own or am explicitly authorised to test. Credentials, secrets, public IP addresses, and sensitive data will not be committed.

## Author

**Tochi Ogueri**  
BSc Computer Science student at Technological University Dublin  
Interested in cybersecurity, data analytics, and software engineering.
