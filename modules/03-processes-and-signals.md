# 03 — Processes and Signals

## Topics

- [ ] Program vs process
- [ ] Process address space and process metadata
- [ ] PID, PPID, and process trees
- [ ] `fork()`, `execve()`, and `wait()`
- [ ] Process states: running, sleeping, stopped, zombie
- [ ] Foreground and background processes
- [ ] File descriptors: stdin, stdout, stderr
- [ ] Pipes and redirection
- [ ] `SIGTERM`, `SIGKILL`, `SIGINT`, and `SIGCHLD`
- [ ] Exit status and parent-child relationships
- [ ] Orphan processes and PID 1
- [ ] Processes vs threads

## Practical lab

```bash
ps -ef
pstree -p
cat /proc/self/status
ls -l /proc/self/fd
sleep 300 &
jobs
kill -TERM <PID>
```

Replace `<PID>` with the actual process ID. Stop only processes you started for the lab.

## Questions to answer

1. How is a new process created and how does it start another program?
2. What is the difference between sending `SIGTERM` and `SIGKILL`?
3. Why can a zombie process exist?
4. Why does a container commonly stop when its main process exits?

## Docker connection

Container lifecycle, entrypoint/CMD behavior, PID 1, signal handling, and graceful shutdown.
