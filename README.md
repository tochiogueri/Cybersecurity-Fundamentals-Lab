# Cybersecurity Fundamentals Lab

A hands-on cybersecurity home lab documenting my progression from core networking and system administration to vulnerability assessment, incident response, and security automation.

> **Status:** In progress — Windows Server 2022 domain controller deployed with Active Directory Domain Services and DNS.

## Project goals

- Build and document an isolated virtual cybersecurity lab.
- Strengthen practical networking, Linux, and Windows administration skills.
- Configure Windows Server, Active Directory Domain Services, DNS, DHCP, users, groups, and Group Policy.
- Capture and analyse network traffic using Wireshark.
- Perform authorised host discovery and vulnerability assessments with tools such as Nmap.
- Investigate simulated security events and document an incident-response workflow.
- Develop small Python tools that automate repeatable security tasks.
- Present clear evidence, findings, and remediation recommendations for each phase.

## Lab environment

| Component | Purpose | Status |
|---|---|---|
| Oracle VirtualBox | Run the isolated virtual machines | Configured |
| Windows Server 2022 | Domain controller and core Windows infrastructure | Deployed |
| Active Directory Domain Services | Centralised identity and domain management | Deployed |
| DNS Server | Active Directory-integrated name resolution | Deployed |
| Windows 10/11 | Domain-joined client | Next step |
| Linux | Administration and security tooling | Planned |
| Cisco Packet Tracer | Routing, switching and VLAN practice | Planned |
| Wireshark | Packet capture and protocol analysis | Planned |
| Nmap | Authorised network discovery and assessment | Planned |
| Python | Security automation | Planned |

## Current lab configuration

| Setting | Value |
|---|---|
| Domain Controller | `DC01` |
| Operating System | Windows Server 2022 Standard Evaluation |
| DC01 IPv4 | `192.168.10.10/24` |
| Active Directory forest/domain | `tochilab.local` |
| NetBIOS domain | `TOCHILAB` |
| DNS Server | DC01 |
| Global Catalog | Enabled |

## Work completed

### Windows Server and Active Directory foundation

- Created a Windows Server 2022 virtual machine in Oracle VirtualBox.
- Renamed the server to `DC01`.
- Configured a static IPv4 address of `192.168.10.10/24` for the lab network.
- Configured DC01 to use itself for DNS in preparation for Active Directory-integrated DNS.
- Installed the Active Directory Domain Services (AD DS) role.
- Installed the DNS Server role.
- Created a new Active Directory forest named `tochilab.local`.
- Configured the NetBIOS domain name as `TOCHILAB`.
- Enabled DNS and Global Catalog functionality on the domain controller.
- Completed the AD DS prerequisite checks successfully.
- Promoted DC01 to the first domain controller in the forest.
- Verified the domain-aware sign-in environment with `TOCHILAB\\Administrator`.

## Project roadmap

| Phase | Focus | Status |
|---|---|---|
| 1 | Networking fundamentals and lab design | In progress |
| 2 | Windows Server and Active Directory | In progress |
| 3 | Windows client deployment and domain integration | Planned |
| 4 | Active Directory users, groups, OUs, DHCP and Group Policy | Planned |
| 5 | Network monitoring and traffic analysis | Planned |
| 6 | Vulnerability assessment and remediation | Planned |
| 7 | Incident response investigation | Planned |
| 8 | Python security automation | Planned |

## Next steps

1. Verify Active Directory and DNS services after promotion.
2. Create a VirtualBox snapshot of the working DC01 state.
3. Deploy a Windows client VM named `PC01`.
4. Configure PC01 to use DC01 for DNS.
5. Join PC01 to `tochilab.local`.
6. Create organisational units, users and security groups.
7. Configure and test Group Policy Objects (GPOs).
8. Add DHCP and validate automatic client addressing.
9. Expand the lab into network monitoring, vulnerability assessment and incident-response exercises.

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

## Ethics and safety

All scanning, testing, and simulated attacks in this repository are limited to systems I own or am explicitly authorised to test. Credentials, secrets, public IP addresses, and sensitive data will not be committed.

## Author

**Tochi Ogueri**  
BSc Computer Science student at Technological University Dublin  
Interested in cybersecurity, data analytics, and software engineering.
