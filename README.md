# Operating Systems Lab Record — VNRVJIET

A GitHub-ready repository containing the Operating Systems laboratory record programs, algorithms, and output/test-case snippets from the supplied OS record.

**Roll No.:** `25071A6230`  
**Laboratory:** Operating Systems  
**Institution:** VNRVJIET  
**Language:** C  

> **Source preservation:** The repository is organized from the supplied OS record. Program logic, terminology, experiment numbering, and record output snippets are preserved rather than silently replaced with a different implementation.

## Repository Structure

```text
OS-Lab-Record/
├── README.md
├── .gitignore
├── record/
│   ├── os_record.pdf
│   └── os_record.docx
└── experiments/
    ├── 01_cpu_scheduling/
    │   ├── README.md
    │   ├── src/
    │   └── outputs/
    ├── 02_priority_round_robin/
    │   ├── README.md
    │   ├── src/
    │   └── outputs/
    ├── 03_banker_scheduling_analysis/
    │   ├── README.md
    │   ├── src/
    │   └── outputs/
    ├── 04_memory_allocation/
    │   ├── README.md
    │   ├── src/
    │   └── outputs/
    ├── 05_paging/
    │   ├── README.md
    │   ├── src/
    │   └── outputs/
    ├── 07_frame_allocation/
    │   ├── README.md
    │   ├── src/
    │   └── outputs/
    ├── 08_disk_scheduling/
    │   ├── README.md
    │   ├── src/
    │   └── outputs/
    └── 09_disk_scheduling/
        ├── README.md
        ├── src/
        └── outputs/
```

## Experiments Included

| Experiment | Topic | Programs |
|---|---|---:|
| 1 | FCFS and SJF Scheduling | 4 |
| 2 | Priority and Round Robin Scheduling | 4 |
| 3 | Banker’s Algorithm and Scheduling Analysis | 1 + analysis chart |
| 4 | Fixed-Partition Memory Allocation | 3 |
| 5 | Paging Technique | 1 |
| 7 | Frame Allocation Methods | 3 |
| 8 | Disk Scheduling: FCFS, SSTF, SCAN | 3 |
| 9 | Disk Scheduling: C-SCAN, LOOK, C-LOOK | 3 |
| | **Total C programs** | **22** |

The supplied record moves from **Experiment 5 directly to Experiment 7**. No Experiment 6 section was present in the supplied source, so it is intentionally not invented here.

---

# Experiment 1 — FCFS and SJF Scheduling Algorithms

**Date in record:** 23-07-2026

## Aim

Write C programs for FCFS scheduling without arrival times and with arrival times, followed by SJF scheduling in non-preemptive and preemptive forms.

## FCFS — Without Arrival Times

The record specifies calculation of completion time, turnaround time and waiting time, followed by average waiting time and average turnaround time.

### Program

[`fcfs_without_arrival.c`](experiments/01_cpu_scheduling/src/fcfs_without_arrival.c)

### Output / Test-case Snippets

![FCFS without arrival — output 1](experiments/01_cpu_scheduling/outputs/fcfs_without_arrival_01.png)

![FCFS without arrival — output 2](experiments/01_cpu_scheduling/outputs/fcfs_without_arrival_02.png)

![FCFS without arrival — output 3](experiments/01_cpu_scheduling/outputs/fcfs_without_arrival_03.png)

## FCFS — With Arrival Times

The program uses arrival time and burst time and calculates CT, TAT and WT for each process.

### Program

[`fcfs_with_arrival.c`](experiments/01_cpu_scheduling/src/fcfs_with_arrival.c)

### Output / Test-case Snippets

![FCFS with arrival — output 1](experiments/01_cpu_scheduling/outputs/fcfs_with_arrival_01.png)

![FCFS with arrival — output 2](experiments/01_cpu_scheduling/outputs/fcfs_with_arrival_02.png)

![FCFS with arrival — output 3](experiments/01_cpu_scheduling/outputs/fcfs_with_arrival_03.png)

## SJF — Non-Preemptive

The record selects an arrived process with the smallest burst time, executes it completely, and calculates CT, TAT and WT.

### Program

[`sjf_non_preemptive.c`](experiments/01_cpu_scheduling/src/sjf_non_preemptive.c)

### Output / Test-case Snippets

![SJF non-preemptive — output 1](experiments/01_cpu_scheduling/outputs/sjf_non_preemptive_01.png)

![SJF non-preemptive — output 2](experiments/01_cpu_scheduling/outputs/sjf_non_preemptive_02.png)

![SJF non-preemptive — output 3](experiments/01_cpu_scheduling/outputs/sjf_non_preemptive_03.png)

## SJF — Preemptive / SRTF

The record sets remaining time equal to burst time and executes the arrived process with the smallest remaining time one time unit at a time.

### Program

[`sjf_preemptive_srtf.c`](experiments/01_cpu_scheduling/src/sjf_preemptive_srtf.c)

### Output / Test-case Snippets

![SJF preemptive — output 1](experiments/01_cpu_scheduling/outputs/sjf_preemptive_srtf_01.png)

![SJF preemptive — output 2](experiments/01_cpu_scheduling/outputs/sjf_preemptive_srtf_02.png)

![SJF preemptive — output 3](experiments/01_cpu_scheduling/outputs/sjf_preemptive_srtf_03.png)

[Open Experiment 1 README](experiments/01_cpu_scheduling/README.md)

---

# Experiment 2 — Priority and Round Robin Scheduling

**Date in record:** 30-07-2026

## Priority Scheduling — Non-Preemptive

The record treats the **lowest priority number as the highest priority**, selects an arrived process, executes it, and calculates CT, TAT and WT.

### Program

[`priority_non_preemptive.c`](experiments/02_priority_round_robin/src/priority_non_preemptive.c)

### Output / Test-case Snippets

![Priority non-preemptive — output 1](experiments/02_priority_round_robin/outputs/priority_non_preemptive_01.png)

![Priority non-preemptive — output 2](experiments/02_priority_round_robin/outputs/priority_non_preemptive_02.png)

![Priority non-preemptive — output 3](experiments/02_priority_round_robin/outputs/priority_non_preemptive_03.png)

## Priority Scheduling — Preemptive

The program selects the arrived process with the lowest priority value and executes it for one time unit before reevaluating.

### Program

[`priority_preemptive.c`](experiments/02_priority_round_robin/src/priority_preemptive.c)

### Output / Test-case Snippets

![Priority preemptive — output 1](experiments/02_priority_round_robin/outputs/priority_preemptive_01.png)

![Priority preemptive — output 2](experiments/02_priority_round_robin/outputs/priority_preemptive_02.png)

![Priority preemptive — output 3](experiments/02_priority_round_robin/outputs/priority_preemptive_03.png)

## Round Robin — Time Quantum 2

The record uses TQ = 2, remaining time, ready-queue processing, completion time, turnaround time and waiting time.

### Program

[`round_robin_tq2.c`](experiments/02_priority_round_robin/src/round_robin_tq2.c)

### Output / Test-case Snippets

![Round Robin TQ 2 — output 1](experiments/02_priority_round_robin/outputs/round_robin_tq2_01.png)

![Round Robin TQ 2 — output 2](experiments/02_priority_round_robin/outputs/round_robin_tq2_02.png)

![Round Robin TQ 2 — output 3](experiments/02_priority_round_robin/outputs/round_robin_tq2_03.png)

## Round Robin — Time Quantum 10

The same record structure is used with TQ = 10.

### Program

[`round_robin_tq10.c`](experiments/02_priority_round_robin/src/round_robin_tq10.c)

### Output / Test-case Snippets

![Round Robin TQ 10 — output 1](experiments/02_priority_round_robin/outputs/round_robin_tq10_01.png)

![Round Robin TQ 10 — output 2](experiments/02_priority_round_robin/outputs/round_robin_tq10_02.png)

![Round Robin TQ 10 — output 3](experiments/02_priority_round_robin/outputs/round_robin_tq10_03.png)

[Open Experiment 2 README](experiments/02_priority_round_robin/README.md)

---

# Experiment 3 — Banker’s Algorithm and Scheduling Analysis

**Date in record:** 23-07-2026

## Scheduling Analysis

The record includes an analysis of:

- FCFS — No Arrival
- FCFS — With Arrival
- SJF — Non-Preemptive
- SRTF — Preemptive
- Priority — Non-Preemptive
- Priority — Preemptive
- Round Robin — Q1
- Round Robin — Q2

### Analysis Chart Snippet

![CPU scheduling analysis chart from record](experiments/03_banker_scheduling_analysis/outputs/cpu_scheduling_analysis_chart.png)

## Banker’s Algorithm

The record calculates `Need = Max − Allocation`, initializes `Work = Available`, repeatedly finds an unfinished process whose `Need ≤ Work`, adds its allocation back to Work, builds a safe sequence, and reports a safe or unsafe state.

### Program

[`bankers_algorithm.c`](experiments/03_banker_scheduling_analysis/src/bankers_algorithm.c)

### Output / Test-case Snippets

![Banker's algorithm — output 1](experiments/03_banker_scheduling_analysis/outputs/bankers_algorithm_01.png)

![Banker's algorithm — output 2](experiments/03_banker_scheduling_analysis/outputs/bankers_algorithm_02.png)

![Banker's algorithm — output 3](experiments/03_banker_scheduling_analysis/outputs/bankers_algorithm_03.png)

[Open Experiment 3 README](experiments/03_banker_scheduling_analysis/README.md)

---

# Experiment 4 — Fixed-Partition Memory Allocation

**Date in record:** 27-08-2026

The record covers First Fit, Worst Fit and Best Fit for fixed-partition memory allocation. Internal fragmentation is calculated as partition/block size minus process size.

## First Fit

[`first_fit.c`](experiments/04_memory_allocation/src/first_fit.c)

![First Fit — output 1](experiments/04_memory_allocation/outputs/first_fit_01.png)

![First Fit — output 2](experiments/04_memory_allocation/outputs/first_fit_02.png)

![First Fit — output 3](experiments/04_memory_allocation/outputs/first_fit_03.png)

## Worst Fit

[`worst_fit.c`](experiments/04_memory_allocation/src/worst_fit.c)

![Worst Fit — output 1](experiments/04_memory_allocation/outputs/worst_fit_01.png)

![Worst Fit — output 2](experiments/04_memory_allocation/outputs/worst_fit_02.png)

![Worst Fit — output 3](experiments/04_memory_allocation/outputs/worst_fit_03.png)

## Best Fit

[`best_fit.c`](experiments/04_memory_allocation/src/best_fit.c)

![Best Fit — output 1](experiments/04_memory_allocation/outputs/best_fit_01.png)

![Best Fit — output 2](experiments/04_memory_allocation/outputs/best_fit_02.png)

![Best Fit — output 3](experiments/04_memory_allocation/outputs/best_fit_03.png)

[Open Experiment 4 README](experiments/04_memory_allocation/README.md)

---

# Experiment 5 — Paging Technique of Memory Management

**Date in record:** 27-08-2026

The record calculates total frames, total pages, constructs a page table, splits a logical address into page number and offset, and calculates the physical address using the allocated frame.

### Program

[`paging_address_translation.c`](experiments/05_paging/src/paging_address_translation.c)

### Output / Test-case Snippets

![Paging — output 1](experiments/05_paging/outputs/paging_address_translation_01.png)

![Paging — output 2](experiments/05_paging/outputs/paging_address_translation_02.png)

![Paging — output 3](experiments/05_paging/outputs/paging_address_translation_03.png)

[Open Experiment 5 README](experiments/05_paging/README.md)

---

# Experiment 6 — Page Replacement Algorithms

**Date in record:** 08-10-2026

Aim: FIFO, LRU and Optimal page replacement.

- [`fifo.c`](experiments/06_page_replacement/src/fifo.c)
- [`lru.c`](experiments/06_page_replacement/src/lru.c)
- [`optimal.c`](experiments/06_page_replacement/src/optimal.c)
- [Experiment 6 README](experiments/06_page_replacement/README.md)

The supplied record has blank Testcases sections for these programs, so no output screenshots have been fabricated.

---

# Experiment 7 — Frame Allocation Methods

**Date in record:** 03-09-2026

The record contains minimum-number, equal, and proportional frame allocation methods.

## Minimum Number of Frames

[`minimum_frame_allocation.c`](experiments/07_frame_allocation/src/minimum_frame_allocation.c)

![Minimum frame allocation — output 1](experiments/07_frame_allocation/outputs/minimum_frame_allocation_01.png)

![Minimum frame allocation — output 2](experiments/07_frame_allocation/outputs/minimum_frame_allocation_02.png)

![Minimum frame allocation — output 3](experiments/07_frame_allocation/outputs/minimum_frame_allocation_03.png)

## Equal Allocation

[`equal_frame_allocation.c`](experiments/07_frame_allocation/src/equal_frame_allocation.c)

![Equal allocation — output 1](experiments/07_frame_allocation/outputs/equal_frame_allocation_01.png)

![Equal allocation — output 2](experiments/07_frame_allocation/outputs/equal_frame_allocation_02.png)

![Equal allocation — output 3](experiments/07_frame_allocation/outputs/equal_frame_allocation_03.png)

## Proportional Allocation

[`proportional_frame_allocation.c`](experiments/07_frame_allocation/src/proportional_frame_allocation.c)

![Proportional allocation — output 1](experiments/07_frame_allocation/outputs/proportional_frame_allocation_01.png)

![Proportional allocation — output 2](experiments/07_frame_allocation/outputs/proportional_frame_allocation_02.png)

![Proportional allocation — output 3](experiments/07_frame_allocation/outputs/proportional_frame_allocation_03.png)

[Open Experiment 7 README](experiments/07_frame_allocation/README.md)

---

# Experiment 8 — Disk Scheduling: FCFS, SSTF and SCAN

**Date in record:** 10-09-2026

The record measures Total Head Movement (THM) and Average Seek Time.

## FCFS

[`disk_fcfs.c`](experiments/08_disk_scheduling/src/disk_fcfs.c)

![Disk FCFS — output 1](experiments/08_disk_scheduling/outputs/disk_fcfs_01.png)

![Disk FCFS — output 2](experiments/08_disk_scheduling/outputs/disk_fcfs_02.png)

![Disk FCFS — output 3](experiments/08_disk_scheduling/outputs/disk_fcfs_03.png)

## SSTF

[`disk_sstf.c`](experiments/08_disk_scheduling/src/disk_sstf.c)

![Disk SSTF — output 1](experiments/08_disk_scheduling/outputs/disk_sstf_01.png)

![Disk SSTF — output 2](experiments/08_disk_scheduling/outputs/disk_sstf_02.png)

![Disk SSTF — output 3](experiments/08_disk_scheduling/outputs/disk_sstf_03.png)

## SCAN

[`disk_scan.c`](experiments/08_disk_scheduling/src/disk_scan.c)

![Disk SCAN — output 1](experiments/08_disk_scheduling/outputs/disk_scan_01.png)

![Disk SCAN — output 2](experiments/08_disk_scheduling/outputs/disk_scan_02.png)

![Disk SCAN — output 3](experiments/08_disk_scheduling/outputs/disk_scan_03.png)

[Open Experiment 8 README](experiments/08_disk_scheduling/README.md)

---

# Experiment 9 — Disk Scheduling: C-SCAN, LOOK and C-LOOK

**Date in record:** 17-09-2026

The record covers circular SCAN, LOOK and C-LOOK style disk scheduling.

> **Record label note:** The supplied program pages are labeled `C) C-SCAN`, `C) LOOK`, and `C) C-LOOK`, even though the experiment aim lists C-SCAN, LOOK and C-LOOK as A/B/C items. The repository uses the algorithm names as filenames and preserves the source program text.

## C-SCAN

[`disk_cscan.c`](experiments/09_disk_scheduling/src/disk_cscan.c)

![C-SCAN — output 1](experiments/09_disk_scheduling/outputs/disk_cscan_01.png)

![C-SCAN — output 2](experiments/09_disk_scheduling/outputs/disk_cscan_02.png)

![C-SCAN — output 3](experiments/09_disk_scheduling/outputs/disk_cscan_03.png)

## LOOK

[`disk_look.c`](experiments/09_disk_scheduling/src/disk_look.c)

![LOOK — output 1](experiments/09_disk_scheduling/outputs/disk_look_01.png)

![LOOK — output 2](experiments/09_disk_scheduling/outputs/disk_look_02.png)

![LOOK — output 3](experiments/09_disk_scheduling/outputs/disk_look_03.png)

## C-LOOK

[`disk_clook.c`](experiments/09_disk_scheduling/src/disk_clook.c)

![C-LOOK — output 1](experiments/09_disk_scheduling/outputs/disk_clook_01.png)

![C-LOOK — output 2](experiments/09_disk_scheduling/outputs/disk_clook_02.png)

![C-LOOK — output 3](experiments/09_disk_scheduling/outputs/disk_clook_03.png)

[Open Experiment 9 README](experiments/09_disk_scheduling/README.md)

---

# Running the Programs

The programs are standard C programs and can be compiled with GCC.

```bash
gcc -std=c11 program.c -o program
./program
```

On Windows with MinGW/GCC:

```powershell
gcc -std=c11 program.c -o program.exe
.\program.exe
```

Each source file retains the interactive input style shown in the laboratory record.

# Source Record

The original supplied files are retained under [`record/`](record/):

- [`os_record.pdf`](record/os_record.pdf)
- [`os_record.docx`](record/os_record.docx)

# Repository Notes

- All 25 C programs extracted from the supplied record are placed in `src/` folders.
- Output/test-case screenshots from the supplied record are preserved under `outputs/`.
- The scheduling-analysis chart is preserved as a page-rendered snippet under Experiment 3.
- The source record is included so the GitHub repository remains traceable to the original laboratory document.
- Experiment 6 is included from the latest supplied record; its three C programs are transcribed from the FIFO, LRU and Optimal program snippets.
