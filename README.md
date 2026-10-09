# Linux OS Internals to Docker Internals

A hands-on learning roadmap for understanding how Linux works underneath Docker. The goal is not to memorize commands, but to understand the mechanisms behind process execution, memory, filesystems, networking, isolation, and container runtimes.

## Learning goals

By the end of this project, I want to be able to:

- Explain how a command runs from userspace and interacts with the Linux kernel.
- Inspect and reason about Linux processes, signals, memory, filesystems, and networking.
- Explain how namespaces and cgroups provide isolation and resource controls.
- Understand Docker's architecture, image layers, container lifecycle, networking, storage, and security.
- Debug container behavior using Linux tools instead of treating Docker as a black box.

## Learning approach

For every topic:

1. Learn the underlying problem and mechanism.
2. Observe it using Linux commands.
3. Run a controlled experiment in a disposable Linux VM or safe development environment.
4. Write down what happened and why.
5. Connect the concept to Docker.

**Completion rule:** A module is complete when I can explain the mechanism in my own words and verify it with a practical experiment.

## Roadmap

| Phase | Module | Priority | Status |
|---|---|---:|---|
| Linux foundation | [01. OS Architecture and Kernel](modules/01-os-architecture-and-kernel.md) | High | Not started |
| Linux foundation | [02. Boot and Initialization](modules/02-boot-and-initialization.md) | Medium | Not started |
| Processes | [03. Processes and Signals](modules/03-processes-and-signals.md) | Very high | Not started |
| CPU and memory | [04. CPU Scheduling](modules/04-cpu-scheduling.md) | High | Not started |
| CPU and memory | [05. Memory Management](modules/05-memory-management.md) | Very high | Not started |
| Storage | [06. Filesystem and Storage](modules/06-filesystem-and-storage.md) | Very high | Not started |
| Kernel interface | [07. System Calls](modules/07-system-calls.md) | High | Not started |
| Networking | [08. Linux Networking](modules/08-linux-networking.md) | Very high | Not started |
| Communication | [09. IPC](modules/09-ipc.md) | Medium | Not started |
| Security | [10. Linux Security](modules/10-linux-security.md) | High | Not started |
| Isolation | [11. Namespaces, cgroups, and OverlayFS](modules/11-isolation-and-resource-control.md) | Very high | Not started |
| Container internals | [12. Docker Internals](modules/12-docker-internals.md) | Final phase | Not started |

## Suggested schedule

A suggested starting pace is 7 weeks at 45–90 minutes per day. Extend the schedule whenever a concept needs more practice.

| Week | Focus |
|---|---|
| 1 | OS architecture, kernel/userspace, boot, services |
| 2 | Processes, signals, file descriptors, system calls |
| 3 | CPU scheduling and memory |
| 4 | Filesystem, permissions, mounts, storage |
| 5 | Networking and IPC |
| 6 | Security, capabilities, namespaces |
| 7 | cgroups, OverlayFS, and review |
| After Linux foundation | Docker internals and end-to-end experiments |

## Environment

Recommended: Ubuntu in a disposable virtual machine for the main lab environment. WSL2 can be useful for many Linux user-space topics, but a full VM is preferable for boot, kernel configuration, and some low-level experiments.

Do not run destructive experiments on a production or shared machine. Some commands may require elevated privileges; understand the command before running it.

## Repository structure

```text
linux-os-docker-internals/
├── README.md
├── PROGRESS.md
├── modules/
│   ├── 01-os-architecture-and-kernel.md
│   ├── ...
│   └── 12-docker-internals.md
└── labs/
    └── README.md
```

## Primary resources

- [Operating Systems: Three Easy Pieces (free online book)](https://pages.cs.wisc.edu/~remzi/OSTEP/)
- [The Linux Programming Interface resources](https://man7.org/tlpi/)
- [Linux kernel documentation](https://docs.kernel.org/)
- [cgroups v2 documentation](https://docs.kernel.org/admin-guide/cgroup-v2.html)
- [Docker documentation](https://docs.docker.com/)
- [OCI Runtime Specification](https://github.com/opencontainers/runtime-spec)
- [containerd documentation](https://containerd.io/)

## Important correction

Docker is not limited to running directly on a Linux host. Linux containers rely on Linux kernel features. On Windows and macOS, Docker Desktop commonly runs Linux containers inside a Linux virtual machine.

## Progress tracking

Update [PROGRESS.md](PROGRESS.md) as modules are completed. Keep experiment notes under `labs/`.
