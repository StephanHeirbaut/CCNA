# Link aggregation

Most common commands to configure a link aggregation using the Cisco CLI.

## PAgP (Port Aggregation Protocol)

| S1       | S2       | Connection?|
|:-----------------|:-------------|:-------------|
| On            | On    |Yes         |
| Auto/Desirable            | Desirable    |Yes         |
| On/Auto/Desirable             | Not configured    |No         |
| On            | Desirable     |No         |
| Auto/On            | Auto    |No         |

## LACP (Link Aggregation Control Protocol)

| S1       | S2       | Connection?|
|:-----------------|:-------------|:-------------|
| On            | On    |Yes         |
| Active/Passive            | Active    |Yes         |
| On/Active/Passive             | Not configured    |No         |
| On            | Active     |No         |
| Passive/On            | Passive    |No         |

## EtherChannel

| Description       | Command       |
|:-----------------|:-------------|
| Blabla            | `interface range fa0/1-4`     |
| Blabla            | `channel-group 1 mode active`     |
| Blabla            | `interface port-channel 1`     |
| Blabla            | `switchport mode trunk`     |
| Blabla            | `switchport trunk allowed vlan 1,2,20`     |