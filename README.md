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