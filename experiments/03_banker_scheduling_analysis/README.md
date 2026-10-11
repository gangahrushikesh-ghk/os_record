# Experiment 3 — Banker’s Algorithm and Scheduling Analysis

**Date:** 23-07-2026  
**Roll No.:** 25071A6230

## Scheduling Analysis

The record analyzes:

- FCFS scheduling without arrival times
- FCFS scheduling with arrival times
- SJF scheduling non-preemptive
- SJF scheduling preemptive / SRTF
- Priority scheduling non-preemptive
- Priority scheduling preemptive
- Round Robin scheduling, time quantum = 2
- Round Robin scheduling, time quantum = 10

![CPU Scheduling Analysis](outputs/cpu_scheduling_analysis_chart.png)

## Banker’s Algorithm

1. Input the number of processes, resource types, Allocation, Max and Available matrices.
2. Calculate `Need = Max − Allocation`.
3. Initialize `Work = Available` and mark all processes unfinished.
4. Select an unfinished process whose `Need ≤ Work`.
5. If found, update `Work = Work + Allocation`, mark it finished and add it to the safe sequence.
6. If no suitable process is found, stop.
7. If all processes finish, report a Safe State and display the safe sequence; otherwise report an Unsafe State.

## Source

[`bankers_algorithm.c`](src/bankers_algorithm.c)

## Output Snippets

![1](outputs/bankers_algorithm_01.png)
![2](outputs/bankers_algorithm_02.png)
![3](outputs/bankers_algorithm_03.png)
