# 02 — Boot and Initialization

## Topics

- [ ] Power-on to firmware and bootloader
- [ ] Kernel loading and initialization
- [ ] `initramfs` / `initrd`
- [ ] Mounting the root filesystem
- [ ] PID 1 and `systemd`
- [ ] Service startup order and dependencies
- [ ] Boot logs and failure diagnosis
- [ ] Shutdown and reboot

## Practical lab

```bash
journalctl -b
journalctl -b -1
systemd-analyze time
systemd-analyze blame
systemctl status
```

`journalctl -b -1` works only when previous-boot logs are available.

## Questions to answer

1. How does Linux get from firmware execution to a running userspace?
2. Why is an initial RAM filesystem sometimes needed?
3. What is PID 1 responsible for?
4. What happens if a required service fails during boot?

## Docker connection

Understand how the Docker daemon is started and how daemon startup failure differs from a container process failure.
