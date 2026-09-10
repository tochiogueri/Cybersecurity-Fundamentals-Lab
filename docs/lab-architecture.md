# Lab Architecture

## Objective

Design an isolated and repeatable environment for learning networking, system administration, and defensive security without exposing external systems.

## Planned systems

| Host | Role | Operating system | Planned address |
|---|---|---|---|
| DC01 | Domain controller, DNS and DHCP | Windows Server 2022 | To be assigned |
| CLIENT01 | Domain-joined workstation | Windows 10/11 | DHCP |
| LINUX01 | Administration and security workstation | Linux | To be assigned |

## Network design

The virtual machines will use a private virtual network. Internet access, if required for updates, will be enabled deliberately and separated from lab testing traffic.

## Design decisions

- Use an isolated network for authorised experimentation.
- Use clear hostnames so screenshots and logs are easy to follow.
- Record the IP plan before deployment.
- Never commit passwords, activation keys, tokens, or sensitive host information.

## Next tasks

- [ ] Select the virtualisation platform.
- [ ] Record host hardware and available RAM/storage.
- [ ] Create the IP addressing plan.
- [ ] Draw the first network diagram.
- [ ] Download installation media from official sources.
