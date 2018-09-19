# VLANs

Most common commands to configure VLANs using the Cisco CLI.

## Configuration ACCESS (SWITCH)

| Description       | Command       |
|:-----------------|:-------------|
| Blabla            | `vlan vlanid`     |
| Blabla            | `name vlanname`     |
| Blabla            | `inteface g0/0`     |
| Blabla            | `switchport mode access`     |
| Blabla            | `switchport access vlan vlanid`     |

## Configuration TRUNK (SWITCH)

| Description       | Command       |
|:-----------------|:-------------|
| Blabla            | `vlan vlanid`     |
| Blabla            | `name vlanname`     |
| Blabla            | `inteface g0/0`     |
| Blabla            | `switchport mode trunk`     |
| Blabla            | `switchport trunk native vlan vlanid`     |
| Blabla            | `switchport trunk allowed vlan vlanid`     |

## Configuration ROUTER-ON-A-STICK (ROUTER)

| Description       | Command       |
|:-----------------|:-------------|
| Blabla            | `vlan vlanid`     |
| Blabla            | `interface g0/0`     |
| Blabla            | `encapsulation dot1q vlanid`     |
| Blabla            | `ip addr X.X.X.X X.X.X.X`     |
| Blabla            | `interface g0/0`     |
| Blabla            | `no shutdown`     |

**memo: switchport mode needs to be trunk**

## Troubleshooting

| Description       | Command       |
|:-----------------|:-------------|
| Show VLAN configuration full           | `show vlan summary`     |
| Show VLAN configuration            | `show vlan brief`     |
