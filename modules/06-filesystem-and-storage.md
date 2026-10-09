# 06 — Filesystem and Storage

## Topics

- [ ] Filesystem hierarchy: `/`, `/etc`, `/usr`, `/var`, `/tmp`
- [ ] Paths, directory entries, and inodes
- [ ] File metadata, ownership, and permissions
- [ ] UID, GID, users, and groups
- [ ] Symbolic links vs hard links
- [ ] File descriptors and open files
- [ ] Mount points and filesystem mounts
- [ ] Block devices, partitions, and filesystems
- [ ] Disk-space exhaustion vs inode exhaustion
- [ ] Virtual filesystems: `/proc` and `/sys`
- [ ] Read-only filesystems and temporary storage

## Practical lab

```bash
ls -li
stat /etc/passwd
df -h
df -i
findmnt
ls -l /proc/self
```

## Questions to answer

1. What does an inode represent?
2. Why is a path not the same thing as a file's underlying inode?
3. What does mounting a filesystem do?
4. Why can a disk have free bytes but still run out of inodes?
5. How do file ownership and permissions affect processes?

## Docker connection

Image layers, writable container layers, bind mounts, volumes, and container filesystem behavior.
