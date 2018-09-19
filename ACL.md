# ACLs

Most common commands to configure ACLs using the Cisco CLI.

## Rules for applying ACLs

1. One ACL per protocol
2. One ACL per direction (IN or OUT)
3. One ACL per interface

## Where to place ACLs

* Extended ACLs are usually placed near the source
* Standard ACLs are usually placed near the destination

## Wildcard mask

(IP address) EXOR (wildcard mask) = allowed IP adress

### Examples

**Example 1:**
192.168.1.1 - 0.0.0.0 = 192.168.1.1

```
  1100 0000.0000 0000.0000 0001.0000 0001
  0000 0000.0000 0000.0000 0000.0000 0000
= 1100 0000.0000 0000.0000 0000.0000 0001
```

**Example 2:**
192.168.1.1 - 255.255.255.255.0 = 0.0.0.0

```
  1100 0000.0000 0000.0000 0001.0000 0001
  1111 1111.1111 1111.1111 1111.1111 1111
= 0000 0000.0000 0000.0000 0000.0000 0000
```

**Example 3:**
192.168.1.1 - 0.0.0.255 = 192.168.1.0

```
  1100 0000.0000 0000.0000 0001.0000 0001
  0000 0000.0000 0000.0000 0000.1111 1111
= 1100 0000.0000 0000.0000 0000.0000 0001
```

**Example 4:**
192.168.1.1 - 0.0.0.255 = 192.168.1.0

```
  255.255.255.255
- 255.255.255.0  (desired subnetmask)
= 0.0.0.255
```

## Configuration ACL

| Description       | Command       |
|:-----------------|:-------------|
| Permits all            | `access-list 1 permit 0.0.0.0 255.255.255.255`     |
| Same as above            | `access-list 1 permit any`     |
| Denies all            | `access-list 1 permit 192.168.10.10 0.0.0.0`     |
| Same as above            | `access-list 1 permit host 192.168.10.10`     |

## Configuration standard ACL

### Numbered

| Description       | Command       |
|:-----------------|:-------------|
| Blabla            | `access-list 1 permit 192.168.10.0 0.0.0.255`     |
| Blabla            | `access-list 1 deny 192.168.20.0 0.0.0.255`     |
| Blabla            | `access-list 1 remark Permit hosts from 192.168.10.0 and denies 192.168.20.0`     |
| Blabla            | `inteface g0/0`     |
| Blabla            | `ip access-group 1 in|out`     |

### Named

| Description       | Command       |
|:-----------------|:-------------|
| Blabla            | `ip access-list standard NO_ACCESS`     |
| Blabla            | `deny host 192.168.11.0`     |
| Blabla            | `permit any`     |
| Blabla            | `interface g0/0`     |
| Blabla            | `ip access-group NO_ACCESS in|out`     |

## Configuration extended ACL

| Description       | Command       |
|:-----------------|:-------------|
| Blabla            | `interface g0/0`     |
| Blabla            | `ip addr X.X.X.X X.X.X.X`     |
| Blabla            | `ip access-group in|out`     |
| Blabla            | `access-list 101 permit|deny protocol any 10.1.1.0 0.0.0.255`     |

## Troubleshooting

| Description       | Command       |
|:-----------------|:-------------|
| Shows all ACLs defined            | `show access-lists`     |