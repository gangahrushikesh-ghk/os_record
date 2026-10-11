# Experiment 5 — Paging Technique of Memory Management

**Date:** 27-08-2026  
**Roll No.:** 25071A6230

## Algorithm from the Record

1. Input main memory size and page size and calculate total frames.
2. Input process size and calculate total pages required.
3. If total pages exceed total frames, display the memory-allocation failure message and stop.
4. Input frame numbers for each page and create the page table.
5. For a logical address, calculate `Page Number = LA / PS` and `Offset = LA % PS`.
6. If the page number is valid, find the frame number and calculate `Physical Address = (Frame Number × PS) + Offset`.
7. Display page number, offset, frame number and physical address.
8. Otherwise display invalid logical address.

## Source

[`paging_address_translation.c`](src/paging_address_translation.c)

## Output Snippets

![1](outputs/paging_address_translation_01.png)
![2](outputs/paging_address_translation_02.png)
![3](outputs/paging_address_translation_03.png)
