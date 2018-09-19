# Basic configuration

## Template 

| Description       | Command       |
|:-----------------|:-------------|
| Blabla            | `command`     |

## Switch

| Description       | Command       |
|:-----------------|:-------------|
| Enter privileged EXEC mode            | `enable`     |
| Secure privileged EXEC mode (better then enable password)           | `enable secret`     |
| Encrypt plaintext            | `service password-encryption`     |
| Enter configuration mode            | `configure terminal`     |
| Set device name            | `hostname SXXXXX`     |
| Change login message            | `banner motd #`     |
| Enter console port configuration            | `line console 0`     |
| Secure console port            | `password XXXXX`     |
| Enable login            | `login`     |
| Enter telnet/SSH access            | `line vty 0 X`     |
| Secure telnet/SSH access            | `password XXXXX`     |
| Enable password prompt            | `login`     |
| Save configuration            | `copy running-config startup-config`     |


## Router

| Description       | Command       |
|:-----------------|:-------------|
| Enter privileged EXEC mode            | `enable`     |
| Secure privileged EXEC mode (better then enable password)           | `enable secret`     |
| Encrypt plaintext            | `service password-encryption`     |
| Enter configuration mode            | `configure terminal`     |
| Set device name            | `hostname RXXXXX`     |
| Change login message            | `banner motd #`     |
| Enter console port configuration            | `line console 0`     |
| Secure console port            | `password XXXXX`     |
| Enable login            | `login`     |
| Enter telnet/SSH access            | `line vty 0 X`     |
| Secure telnet/SSH access            | `password XXXXX`     |
| Enable password prompt            | `login`     |
| Save configuration            | `copy running-config startup-config`     |

## Interface

| Description       | Command       |
|:-----------------|:-------------|
| Enter interface configuration            | `interface g0/0`     |
| Set IPv4 address            | `ip addr 192.168.1.1 255.255.255.0`     |
| Set IPv6 address            | `ipv6 addr fa80::1 link-local`     |
| Set description            | `description Link to internal network`     |
| Enable interface            | `no shutdown`     |
| Disable interface           | `shutdown`     |


## Security

| Description       | Command       |
|:-----------------|:-------------|
| Enable Cisco auto-secure features            | `auto secure`     |
| Secure login attempts            | `login block-for 120 attempts 3 within 60`     |
| Secure VTY (config-vty required)            | `exec-timeout 10`     |

## SSH

| Description       | Command       |
|:-----------------|:-------------|
| Set domain-name            | `ip domain-name name`     |
| Generate one-way secret RSA key            | `crypto key generate rsa general-keys modulus 1024`     |
| Set username            | `username name`     |
| Enter VTY configuration            | `line vty 0 4`     |
| Enable login local            | `login local`     |
| Enable VTY inbound SSH            | `transport input ssh`     |

## Troubleshooting

| Description       | Command       |
|:-----------------|:-------------|
| Shows the complete configuration            | `show running-config`     |
| Shows configuration of all interfaces            | `show interfaces`     |
| Shows configuration of the IPv4 interface            | `show ip interface brief`     |
| Shows configuration of IPv4 routes            | `show ip route`     |
| Shows configuration of the IPv6 interface            | `show ipv6 interface brief`     |
| Shows configuration of IPv4 routes            | `show ip route`     |
| Shows ARP table            | `show arp`     |
| Shows MAC information            | `show mac-address-table`     |
| Shows active protocols (best practise to add option between show and protocol for better results)          | `show protocols`     |
| Shows version Cisco OS            | `show version`     |
| Ping to destination to check response            | `ping X.X.X.X`     |
| Check route to destination            | `tracert X.X.X.X`     |