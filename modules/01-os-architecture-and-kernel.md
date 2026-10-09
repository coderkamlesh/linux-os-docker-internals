# 01 — OS Architecture and Kernel

## Objective

Understand the main OS components and how userspace programs request services from the Linux kernel.

## Topics

- [ ] Hardware basics: CPU, RAM, storage, and I/O devices
- [ ] Firmware, BIOS/UEFI, and bootloader overview
- [ ] Kernel vs userspace
- [ ] User mode vs kernel mode
- [ ] System calls and the kernel boundary
- [ ] Monolithic kernel vs microkernel: conceptual comparison
- [ ] Linux kernel vs GNU utilities vs Linux distribution
- [ ] Shell, terminal, terminal emulator, and command execution
- [ ] `systemd`, services, and daemons

## Practical lab

```bash
uname -a
uname -r
cat /etc/os-release
ps -p 1 -o pid,comm,args
systemctl --type=service --state=running
```

## Questions to answer

1. What happens between pressing Enter on a command and seeing its output?
2. Why can an ordinary process not directly perform every hardware operation?
3. What is the difference between Linux, the Linux kernel, and a Linux distribution?
4. What role do system calls play?

## Docker connection

Understand which responsibilities belong to the host kernel and which belong to Docker's userspace components.
