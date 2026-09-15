# Cybersecurity Home Lab

A hands-on cybersecurity project focused on building and securing a small enterprise-style virtual environment. The lab is being developed to strengthen practical skills in Windows Server, Active Directory, networking, traffic analysis, vulnerability assessment, incident response, and security automation.

> **Status:** In progress — DC01 has been promoted to the first domain controller for `tochilab.local`. Post-promotion verification is the next step.

## Project objectives

- Build and document an isolated virtual cybersecurity lab.
- Develop practical Windows Server and Active Directory administration skills.
- Configure and manage DNS, DHCP, users, groups, organisational units, and Group Policy.
- Deploy and manage domain-joined Windows clients.
- Strengthen networking skills through IP addressing, routing, VLANs, and network troubleshooting.
- Capture and analyse network traffic using Wireshark.
- Perform authorised reconnaissance and vulnerability assessments using tools such as Nmap.
- Apply security hardening and document remediation decisions.
- Investigate simulated security incidents and build an incident-response workflow.
- Develop small Python tools for repeatable security and automation tasks.

## Current lab environment

| Component | Purpose | Status |
|---|---|---|
| Oracle VirtualBox | Virtualisation platform for the lab | Configured |
| Windows Server 2022 | Domain controller and Windows infrastructure | Deployed |
| Active Directory Domain Services | Centralised identity and domain management | Installed and promoted |
| DNS Server | Name resolution for the AD environment | Installed; verification pending |
| Windows 10/11 client | Domain-joined workstation | Planned |
| Cisco Packet Tracer | Routing, switching and VLAN practice | Planned |
| Linux | Administration and security tooling | Planned |
| Wireshark | Packet capture and protocol analysis | Planned |
| Nmap | Authorised host and service discovery | Planned |
| Python | Security automation | Planned |

## Current configuration

| Setting | Value |
|---|---|
| Domain Controller | `DC01` |
| Operating System | Windows Server 2022 Standard Evaluation |
| DC01 IPv4 address | `192.168.10.10/24` |
| Active Directory forest/domain | `tochilab.local` |
| NetBIOS domain | `TOCHILAB` |
| DNS role | Installed on DC01 |
| Global Catalog | Enabled |

## Phase 1 — Lab Infrastructure & Active Directory

### Completed

- [x] Created a Windows Server 2022 virtual machine in Oracle VirtualBox.
- [x] Renamed the server to `DC01`.
- [x] Configured the static IPv4 address `192.168.10.10/24` for the isolated lab network.
- [x] Configured DC01 to use itself as its preferred DNS server in preparation for AD-integrated DNS.
- [x] Installed the Active Directory Domain Services (AD DS) role.
- [x] Installed the DNS Server role.
- [x] Created the new Active Directory forest `tochilab.local`.
- [x] Configured the NetBIOS domain name as `TOCHILAB`.
- [x] Enabled DNS Server and Global Catalog capabilities during promotion.
- [x] Completed the AD DS prerequisite checks successfully.
- [x] Promoted DC01 to the first domain controller in the forest.
- [x] Confirmed the domain-aware Windows sign-in screen displays `TOCHILAB\Administrator`.

### Next actions

- [ ] Log in after promotion and verify DC01 is functioning as a domain controller.
- [ ] Verify `tochilab.local` in Active Directory Users and Computers.
- [ ] Verify the DNS forward lookup zone and AD-related DNS records.
- [ ] Create a VirtualBox snapshot of the working DC01 state.

## Project roadmap

| Phase | Focus | Status |
|---|---|---|
| 1 | Lab Infrastructure & Active Directory | In progress |
| 2 | Windows Client & Domain Management | Planned |
| 3 | Network Design, VLANs & Routing | Planned |
| 4 | Network Traffic Analysis | Planned |
| 5 | Vulnerability Assessment | Planned |
| 6 | Security Hardening | Planned |
| 7 | Incident Response / SOC Investigation | Planned |
| 8 | Python Security Automation | Planned |

## Planned next phase

Phase 2 will introduce a Windows client named `PC01`. The client will be configured to use DC01 for DNS, joined to `tochilab.local`, and used to test domain authentication, users, groups, organisational units, Group Policy, and DHCP.

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
2. Lab environment and configuration
3. Implementation steps
4. Sanitised screenshots or command output
5. Validation and test results
6. Problems encountered and troubleshooting
7. Security findings and remediation decisions
8. Skills demonstrated

## Ethics and safety

All scanning, testing, and simulated attacks documented in this repository are limited to systems I own or am explicitly authorised to test. Credentials, secrets, public IP addresses, and sensitive information will not be committed.

## Author

**Tochi Ogueri**  
BSc Computer Science student at Technological University Dublin  
Interested in cybersecurity, data analytics, and software engineering.
