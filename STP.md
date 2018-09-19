# STP (Spanning Tree Protocols)

Most common commands to configure (Rapid)PVST+ using the Cisco CLI.

## Configuration PVST+

| Description       | Command       |
|:-----------------|:-------------|
| Blabla            | `spanning-tree VLAN vlanid root primary`     |
| Blabla            | `spanning-tree VLAN vlanid root secondary`     |
| Blabla            | `spanning-tree VLAN vlanid priority 24576`     |

## Configuration Rapid PVST+

| Description       | Command       |
|:-----------------|:-------------|
| Blabla            | `spanning-tree mode rapid-pvst`     |
| Blabla            | `interface g0/0`     |
| Blabla            | `spanning-tree link-type point-to-point`     |

## Configuration PortFast

| Description       | Command       |
|:-----------------|:-------------|
| Blabla            | `interface g0/0`     |
| Blabla            | `spanning-tree portfast`     |

## Configuration PortFast

| Description       | Command       |
|:-----------------|:-------------|
| Blabla            | `interface g0/0`     |
| Blabla            | `spanning-tree bpduguard enable`     |

## Troubleshooting

| Description       | Command       |
|:-----------------|:-------------|
| Blabla            | `show spanning-tree active`     |
| Blabla            | `clear spanning-tree detected-protocols`     |