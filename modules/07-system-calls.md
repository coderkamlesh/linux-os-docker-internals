# 07 — System Calls

## Topics

- [ ] Library function vs system call
- [ ] `open`, `read`, `write`, and `close`
- [ ] `fork`, `execve`, and `wait`
- [ ] `clone` and process creation concepts
- [ ] `mmap` and `brk`
- [ ] `socket`, `bind`, `listen`, `accept`, and `connect`
- [ ] `mount` and namespace-related system calls
- [ ] Observing calls with `strace`
- [ ] `errno` and common system errors

## Practical lab

```bash
strace -f -o trace.log ls /tmp
grep -E 'openat|read|write|close' trace.log
```

## Questions to answer

1. Why do programs need system calls?
2. What is the difference between a library wrapper and a kernel system call?
3. How can `strace` help diagnose a failed command?
4. Which system calls are involved in opening a file or creating a network connection?

## Docker connection

Understand that container runtimes use Linux kernel APIs to configure process isolation and start container processes.
