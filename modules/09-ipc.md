# 09 — Inter-Process Communication (IPC)

## Topics

- [ ] Anonymous pipes and named pipes
- [ ] Signals
- [ ] Shared memory
- [ ] Message queues
- [ ] Unix domain sockets
- [ ] TCP sockets
- [ ] Basic synchronization concepts
- [ ] IPC resource permissions

## Practical lab

```bash
ls -l /proc/self/fd
ss -lx
ipcs -a
```

## Questions to answer

1. How can two processes exchange data?
2. When is a Unix domain socket preferable to TCP?
3. What is the difference between shared memory and message passing?
4. How can namespaces affect IPC visibility?

## Docker connection

Docker CLI-to-daemon communication, Unix sockets, and communication between containerized services.
