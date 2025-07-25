# TryHackMe: MBR and GPT Analysis

## Room Link
[https://tryhackme.com/room/mbrgptanalysis](https://tryhackme.com/room/mbrgptanalysis)

## Room Description
This TryHackMe room focuses on the fundamentals of file system analysis, with a specific emphasis on the Master Boot Record (MBR) and GUID Partition Table (GPT). Participants learn about the system boot process, the structure of MBR and GPT, and common attacks targeting these critical areas. The module includes hands-on scenarios designed to help identify artifacts of boot process attacks.

## Objectives/Skills Exercised
* Understanding the system boot process.
* In-depth analysis of MBR structure.
* In-depth analysis of GPT structure.
* Identification and analysis of MBR/GPT attacks (e.g., bootkits).
* Practical application of disk and file system analysis tools.
* Problem-solving in the context of MBR/GPT forensics.

## Tools Used
* Standard disk analysis tools (e.g., `fdisk`, `gdisk`, hex editors)
* Forensics tools (e.g., Autopsy, FTK Imager - if used in the room)
* Linux Terminal (bash)

## My Insights/Lessons Learned

This room provided me with a solid foundation for understanding how operating systems initialise upon power-on, and the crucial role of MBR and GPT in this process.

* **MBR/GPT Significance for Security:** I gained a deeper appreciation for how critical these sectors are to system integrity. Their corruption or infection (by bootkits) can completely prevent a system from booting or allow malicious software to run with the highest privileges, undetected by traditional AV solutions.
* **Practical Analysis:** The hands-on exercises demonstrated how to manually analyse MBR and GPT structures, identifying partitions and potential anomalies. It was particularly insightful to differentiate how malware can modify these structures to maintain persistence.
* **MBR vs. GPT Differences:** I clearly understood the key distinctions between the older MBR scheme (limitations in disk size, number of partitions, single boot sector) and the newer, more resilient GPT (larger disks, more partitions, redundant copies of the partition table). This knowledge is crucial when performing analysis on different systems.
* **Challenges Encountered:** (Add specific challenges you faced, e.g.)
    * *Initially, I struggled with interpreting raw hexadecimal data, but with the aid of specific tools and a systematic approach, I was able to extract key information.*
    * *The task involving the identification of a specific bootkit type required precise analysis of signatures within the MBR, which was an excellent exercise in meticulousness.*
* **Real-World Application:** The knowledge gained in this room is directly applicable to digital forensics and incident response, especially when suspecting a low-level infection. Understanding the boot process is fundamental for effectively diagnosing system boot issues and detecting advanced threats.
