# mikrotik-routeros-hands-on

Practical exercises and hands-on labs for MikroTik RouterOS, networking fundamentals, routing, and network configuration.


## Resources

- [pbxshop](https://pbxshop.co/free-courses/free-mikrotik-course/)

## First Steps

1. System -> Reset Factory
2. Account Creation: System -> Users
3. IP -> Services (Disable all unnecessary services)


## Take IP

- IP -> Address List
  ```yaml
  - address: "192.168.0.1/24"
    network: "192.168.0.0"
    interface: "ether1"
  ```

## Bridge

We can make a bridge between multiple ports, after than they work as a `layer2 switch`.

## Internet into router

1. VPN Client (pppoe)

```
ISP ---- [Bridged     Modem] ------- pppoe Client ------- Router
```

2. DHCP Client

```
ISP ---- [Non Bridged Modem] ------- DHCP Client -------- Router
```

3. IP Static

## Routing

1. Default Route
   Destination is not specefic, generally 0.0.0.0/0
2. Static Route
3. Connected Route


## NAT (Network Address Translation)

1. SRC NAT
   1. Static NAT  (Lan into Wan)
   2. Dynamic NAT (multiple Lans into multiple Wans)
   3. PAT         (Port Management)
2. DST NAT

Chain `srcnat` Actions:
   - masqureate: automatically converte a local ip into public (route) ip
   - src-name:   can define which pubic IP should be used