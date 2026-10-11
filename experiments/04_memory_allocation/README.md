# Experiment 4 — Fixed-Partition Memory Allocation

**Date:** 27-08-2026  
**Roll No.:** 25071A6230

## First Fit

Search partitions from the first partition. Allocate the first unallocated partition large enough for the process. Internal fragmentation is `Partition Size − Process Size`.

[`first_fit.c`](src/first_fit.c)

![1](outputs/first_fit_01.png)
![2](outputs/first_fit_02.png)
![3](outputs/first_fit_03.png)

## Worst Fit

Search all unallocated partitions and select the largest partition that is large enough. Internal fragmentation is `Partition Size − Process Size`.

[`worst_fit.c`](src/worst_fit.c)

![1](outputs/worst_fit_01.png)
![2](outputs/worst_fit_02.png)
![3](outputs/worst_fit_03.png)

## Best Fit

Search all unallocated partitions and select the smallest partition that is large enough. Internal fragmentation is `Partition Size − Process Size`.

[`best_fit.c`](src/best_fit.c)

![1](outputs/best_fit_01.png)
![2](outputs/best_fit_02.png)
![3](outputs/best_fit_03.png)
