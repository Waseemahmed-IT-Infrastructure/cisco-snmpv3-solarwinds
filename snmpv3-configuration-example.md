
# Cisco SNMPv3 Configuration Example

This is a sample configuration for monitoring a Cisco switch using SNMPv3.

## Example Configuration

```cisco
! Allow a sample monitoring server
ip access-list standard SNMP-MONITOR
 permit 192.0.2.50
 deny any log

! Create an SNMP view
snmp-server view MONITOR-VIEW iso included

! Create an SNMPv3 group
snmp-server group MONITOR-GROUP v3 priv read MONITOR-VIEW access SNMP-MONITOR

! Create an SNMPv3 user
! Replace placeholders with strong, unique secrets
snmp-server user monitoruser MONITOR-GROUP v3 auth sha <AUTH_PASSWORD> priv aes 128 <PRIV_PASSWORD>
```

## What These Commands Do

| Setting | Purpose |
|---|---|
| ACL | Limits access to the monitoring server |
| SNMP view | Defines which monitoring information can be accessed |
| SNMP group | Sets the security level and permissions |
| SNMP user | Provides authentication and encryption |

## SolarWinds Monitoring

After configuring SNMPv3, the switch can be added to SolarWinds using the approved monitoring settings.

The main things to check are:

- Switch connectivity
- SNMPv3 username and security level
- Authentication and encryption settings
- ACL permissions
- Device status in SolarWinds

## Verification Commands

```cisco
show snmp user
show snmp group
show snmp
show access-lists
show logging
```

## Note

This is a documentation example only. The IP address is reserved for examples, and the passwords are placeholders. It has not been tested on a live switch.
