# RIP

Most common commands to configure RIP using the Cisco CLI.

## Configuration

| Description       | Command       |
|:-----------------|:-------------|
| Enable RIP            | `router rip`     |
| Enable RIPv2            | `version2`     |
| Set network addresses            | `network 192.168.1.0`     |
| Disable auto summarization (no longer summarize networks to their classful address at boundary routers)            | `no auto-summary`     |
| Prevent propragation of unneeded updates            | `passive-interface g0/0`     |
| Propagates default routes            | `default-information originate`     |