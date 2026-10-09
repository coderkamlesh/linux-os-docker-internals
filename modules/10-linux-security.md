# 10 — Linux Security

## Topics

- [ ] Users, groups, UID, and GID
- [ ] Root and privilege boundaries
- [ ] Linux capabilities
- [ ] Namespace isolation and its limits
- [ ] `sudo` and privilege escalation
- [ ] Discretionary access control (DAC) and ACLs
- [ ] Linux Security Modules overview
- [ ] SELinux and AppArmor purpose
- [ ] Seccomp and system-call filtering
- [ ] Principle of least privilege

## Practical lab

```bash
id
getent passwd
getent group
capsh --print
```

Some tools may need to be installed. Do not run privilege-escalation or security-bypass experiments on systems you do not own or administer.

## Questions to answer

1. What does root privilege allow, and what does it not automatically bypass?
2. Why are Linux capabilities more granular than a single all-powerful root privilege?
3. Why are namespaces not a complete security boundary on their own?
4. What does seccomp restrict?

## Docker connection

Container users, dropped capabilities, `--privileged`, rootless containers, seccomp, and AppArmor/SELinux.
