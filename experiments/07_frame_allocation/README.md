# Experiment 7 — Frame Allocation Methods

**Date:** 03-09-2026  
**Roll No.:** 25071A6230

## Minimum Number of Frames

Input total frames, minimum frames required per process, process count and page requirements. Check whether the available frames are sufficient, allocate the minimum frames, and display remaining unallocated frames.

[`minimum_frame_allocation.c`](src/minimum_frame_allocation.c)

![1](outputs/minimum_frame_allocation_01.png)
![2](outputs/minimum_frame_allocation_02.png)
![3](outputs/minimum_frame_allocation_03.png)

## Equal Allocation

The record uses `Frames per Process = Total Frames / m` and `Leftover = Total Frames % m`.

[`equal_frame_allocation.c`](src/equal_frame_allocation.c)

![1](outputs/equal_frame_allocation_01.png)
![2](outputs/equal_frame_allocation_02.png)
![3](outputs/equal_frame_allocation_03.png)

## Proportional Allocation

The record calculates total requirement `S` and uses `Allocation[i] = (s[i] / S) × m`, followed by total allocated and unallocated frames.

[`proportional_frame_allocation.c`](src/proportional_frame_allocation.c)

![1](outputs/proportional_frame_allocation_01.png)
![2](outputs/proportional_frame_allocation_02.png)
![3](outputs/proportional_frame_allocation_03.png)
