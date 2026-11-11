
# Cisco SNMPv3 and SolarWinds Monitoring

## Overview

This project covers Cisco switch monitoring using SNMPv3 and SolarWinds.

Network monitoring helps IT teams check device availability, interface status and network issues.

## SNMPv3

SNMPv3 is used for secure network monitoring.

It supports:
- User authentication
- Data encryption
- Controlled access to monitoring information

## SolarWinds Monitoring

SolarWinds can be used to monitor Cisco switches and other network devices.

Common monitoring tasks include:
- Checking whether switches are online
- Monitoring interface status
- Reviewing device alerts
- Checking network performance
- Investigating connectivity issues

## Access Control

Access Control Lists (ACLs) can restrict which monitoring servers are allowed to access SNMP services.

This helps limit monitoring access to approved systems.

## Useful Cisco Commands

| Command | Purpose |
|---|---|
| `show snmp user` | Check configured SNMPv3 users |
| `show snmp group` | Check SNMP groups |
| `show snmp` | View SNMP statistics |
| `show access-lists` | Review ACL rules |
| `show interfaces status` | Check switch ports |
| `show logging` | Review switch logs |

## Troubleshooting

When a switch is not reporting correctly in SolarWinds, I check:

- Network connectivity
- SNMP version and settings
- Authentication and encryption settings
- Monitoring server access
- Switch interface status

## Note

This repository contains general technical documentation. No production SNMP credentials, internal IP addresses or company configurations are included.
