# 12 — Docker Internals

Start this module after the Linux foundation is understood. Use the official Docker and OCI documentation alongside practical experiments.

## Topics

- [ ] Docker architecture: CLI, API, and `dockerd`
- [ ] Docker Engine vs Docker Desktop
- [ ] `containerd`, shim, `runc`, and OCI runtime concepts
- [ ] OCI image and runtime specifications
- [ ] End-to-end flow of `docker run`
- [ ] Image manifests, layers, and content-addressed storage concepts
- [ ] OverlayFS and writable container layer
- [ ] Container lifecycle and main process
- [ ] Namespaces and cgroups in container setup
- [ ] Bridge networking, DNS, NAT, and port publishing
- [ ] Volumes and bind mounts
- [ ] Container users, capabilities, seccomp, and rootless mode
- [ ] Logs, health checks, resource monitoring, and debugging

## Suggested experiments

1. Start a container and inspect its process tree.
2. Compare host and container views of `/proc`.
3. Inspect the container's namespaces and cgroup membership.
4. Compare a container's writable layer with a bind mount or volume.
5. Inspect listening ports and test container-to-container DNS.
6. Apply CPU and memory limits, then observe the results.
7. Stop a container gracefully and inspect signal behavior.
8. Investigate a deliberately misconfigured container and document the root cause.

## Questions to answer

1. What work happens in the CLI, daemon, container manager, and runtime?
2. Which operations are handled by Docker userspace components and which by the Linux kernel?
3. What is created when a container starts?
4. Why is a container not the same thing as a virtual machine?
5. What persists when a container is removed, and what does not?

## Primary references

- [Docker documentation](https://docs.docker.com/)
- [OCI Runtime Specification](https://github.com/opencontainers/runtime-spec)
- [OCI Image Specification](https://github.com/opencontainers/image-spec)
- [containerd](https://containerd.io/)
- [Linux kernel documentation](https://docs.kernel.org/)
