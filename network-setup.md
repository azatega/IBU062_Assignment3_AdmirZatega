# Network Setup

### Routes and Switches

**Router Model**: ISR4331

**Switch0 Model**: 2960-24TT

**Switch1 Model**: 2960-24TT

### Hosts and IPs

**PC0**: 168.90.0.2

**PC1**: 168.90.0.3

**Laptop0**: 168.90.0.4

**PC3**: 168.90.0.5

**PC2**: 210.3.14.2

**Server0**: 210.3.14.3

**Server1**: 210.3.14.4

**PC4**: 210.3.14.5

### DHCP Commands

`enable`

`configure terminal`

`ip dhcp excluded-address 168.90.0.1`

`ip dhcp pool PoolOne`

`network 168.90.0.0 255.0.0.0`

`default-router 168.90.0.1`

`network 168.90.0.0 255.255.0.0`

`exit`

`ip dhcp excluded-address 210.3.14.1`

`ip dhcp pool PoolTwo`

`network 210.3.14.0 255.255.255.0`

`default-router 210.3.14.1`

`exit`

`interface Gig0/0/0`

`ip address 168.90.0.1 255.255.0.0`

`no shutdown`

`exit`

`interface Gig0/0/1`

`ip address 210.3.14.1 255.255.255.0`

`no shutdown`

`exit`
