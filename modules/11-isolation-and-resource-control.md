# 11 — Namespaces, cgroups, and OverlayFS

## Topics

- [ ] The problem of resource and view isolation
- [ ] Linux namespaces overview
- [ ] PID namespace
- [ ] Mount namespace
- [ ] Network namespace
- [ ] UTS namespace
- [ ] IPC namespace
- [ ] User namespace
- [ ] Cgroup namespace
- [ ] cgroups v1 vs cgroups v2
- [ ] CPU, memory, and I/O controllers
- [ ] Memory limits and OOM behavior
- [ ] `unshare` and `nsenter`
- [ ] Inspecting `/proc` and `/sys/fs/cgroup`
- [ ] OverlayFS: lower, upper, and merged layers

## Practical lab

```bash
lsns
ls -l /proc/self/ns
cat /proc/self/cgroup
findmnt -t overlay
unshare --pid --fork --mount-proc sh
```

Run isolation experiments in a disposable Linux VM. Commands and results vary by kernel, distribution, privileges, and enabled features.

## Questions to answer

1. What does each namespace isolate?
2. Why do namespaces and cgroups solve different problems?
3. How are resource limits enforced?
4. What is the difference between an image's read-only layers and a container's writable layer?
5. How can a process inspect its own namespaces and cgroup membership?

## Docker connection

This module provides the core Linux foundation for understanding container isolation, resource limits, and layered filesystems.
