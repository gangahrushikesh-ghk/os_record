# Experiment 8 — Disk Scheduling: FCFS, SSTF and SCAN

**Date:** 10-09-2026  
**Roll No.:** 25071A6230

## FCFS

Calculate the distance from the current head to every request in sequence, add each distance to Total Head Movement, and calculate `Average Seek Time = THM / n`.

[`disk_fcfs.c`](src/disk_fcfs.c)

![1](outputs/disk_fcfs_01.png)
![2](outputs/disk_fcfs_02.png)
![3](outputs/disk_fcfs_03.png)

## SSTF

Repeatedly find the unvisited request closest to the current head, mark it visited, add the distance to THM, and move the head to that request.

[`disk_sstf.c`](src/disk_sstf.c)

![1](outputs/disk_sstf_01.png)
![2](outputs/disk_sstf_02.png)
![3](outputs/disk_sstf_03.png)

## SCAN

Sort requests and service them according to the selected direction. The record moves the head to the corresponding disk boundary, reverses direction, and services remaining requests.

[`disk_scan.c`](src/disk_scan.c)

![1](outputs/disk_scan_01.png)
![2](outputs/disk_scan_02.png)
![3](outputs/disk_scan_03.png)
