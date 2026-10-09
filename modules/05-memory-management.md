# 05 — Memory Management

## Topics

- [ ] Physical RAM and virtual memory
- [ ] Process virtual address space
- [ ] Stack, heap, and memory-mapped regions
- [ ] Page tables and address translation
- [ ] Demand paging and page faults
- [ ] Anonymous memory and file-backed memory
- [ ] Page cache and buffers
- [ ] Swap and memory pressure
- [ ] RSS vs virtual size
- [ ] Memory leaks vs legitimate high memory usage
- [ ] Out-of-memory conditions and Linux OOM killer

## Practical lab

```bash
free -h
cat /proc/meminfo
cat /proc/<PID>/status
pmap -x <PID>
vmstat 1
```

## Questions to answer

1. Why does a process use virtual addresses rather than directly managing physical RAM?
2. Why can virtual memory size be much larger than resident memory?
3. What is the difference between page cache and anonymous memory?
4. What happens under memory pressure?
5. How do a JVM heap limit and a container memory limit differ?

## Docker connection

Container memory limits, OOM kills, memory accounting, and JVM sizing in containers.
