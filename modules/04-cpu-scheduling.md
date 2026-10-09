# 04 — CPU Scheduling

## Topics

- [ ] CPU cores vs hardware threads
- [ ] Process scheduling and context switching
- [ ] Time slicing and preemption
- [ ] Scheduling priority and nice values
- [ ] CPU-bound vs I/O-bound workloads
- [ ] Load average
- [ ] CPU affinity
- [ ] CPU time and reported utilization
- [ ] CPU quotas and throttling

## Practical lab

```bash
top
htop
ps -eo pid,ni,stat,pcpu,comm
uptime
taskset -pc <PID>
```

## Questions to answer

1. Why can many processes run on a machine with fewer CPU cores?
2. What does a context switch cost?
3. What does load average measure, and why is it not the same as CPU percentage?
4. How can CPU throttling slow an application even when the host does not look fully utilized?

## Docker connection

CPU quotas, CPU shares/weights, cpusets, and container performance debugging.
