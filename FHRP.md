# FHRP (First Hop Redudancy Protocols)

Most common commands to configure FHRP using the Cisco CLI.

## Configuration HSRP

| Description       | Command       |
|:-----------------|:-------------|
| Blabla            | `standby version 2`     |
| Blabla            | `interface g0/0`     |
| Blabla            | `ip addr 10.1.1.1 255.255.255.0`     |
| Blabla            | `no shutdown`     |
| Blabla            | `standy 123 ip 10.1.1.100`     |
| Blabla            | `standby 123 preempt`     |
| Blabla            | `interface g0/1`     |
| Blabla            | `ip addr 10.1.1.2 255.255.255.0`     |
| Blabla            | `no shutdown`     |
| Blabla            | `standy 123 ip 10.1.1.100`     |
| Blabla            | `standby 123 priority 90`     |

## Configuration VRRPv3

| Description       | Command       |
|:-----------------|:-------------|
| Blabla            | `fhrp version vrrp v3`     |
| Blabla            | `interface g0/0`     |
| Blabla            | `vrrp group-id address-family {ipv4 or ipv6}`     |
| Blabla            | `address 10.1.1.1 [primary or secondary]`     |
| Blabla            | `description group-description`     |
| Blabla            | `match-address`     |
| Blabla            | `preempt delay minimum seconds`     |
| Blabla            | `priority priority-level`     |
| Blabla            | `timers advertise interval`     |
| Enable support for VRRPv2 (optional)            | `vvrpv2`     |
| Blabla            | `vrrs leader leader-name`     |

## Configuration GLBP

| Description       | Command       |
|:-----------------|:-------------|
| Blabla            | `interface g0/0`     |
| Blabla            | `ip addr 10.1.1.1 255.255.255.0`     |
| Blabla            | `glbp 1 ip 10.1.1.250`     |
| Blabla            | `glbp 1 priority 120`     |
| Blabla            | `glbp 1 preempt`     |
| Blabla            | `interface g0/1`     |
| Blabla            | `ip addr 10.1.1.2 255.255.255.0`     |
| Blabla            | `glbp 1 priority 100`     |
| Blabla            | `glbp 1 ip 10.0.254`     |
| Blabla            | `glbp 1 preempt`     |

## Troubleshooting

| Description       | Command       |
|:-----------------|:-------------|
| Blabla            | `show standby`     |
| Blabla            | `show glbp`     |
| Blabla            | `show vrrp`     |
| Blabla            | `show hsrp`     |