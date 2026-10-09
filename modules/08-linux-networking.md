# 08 — Linux Networking

## Topics

- [ ] Network interfaces, MAC addresses, and IP addresses
- [ ] TCP/IP layers and packet flow
- [ ] TCP handshake, ports, and listening sockets
- [ ] UDP vs TCP
- [ ] DNS resolution
- [ ] Routing tables and default gateway
- [ ] Loopback and `localhost`
- [ ] Linux network stack overview
- [ ] Virtual Ethernet pairs
- [ ] Linux bridges and NAT
- [ ] Netfilter, `iptables`, and `nftables`

## Practical lab

```bash
ip addr
ip route
ip link
ss -lntup
cat /etc/resolv.conf
getent hosts example.com
```

## Questions to answer

1. What happens when an application connects to an IP address and port?
2. Why does `localhost` inside a container refer to that container's own network namespace?
3. What are a bridge and a virtual Ethernet pair?
4. What is the difference between port listening and port publishing?

## Docker connection

Bridge networks, container DNS, port publishing, NAT, and host-to-container connectivity.
