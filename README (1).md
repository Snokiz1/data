# OS Simulator - Java Console Application

This is a console-based Java application that simulates core operating system algorithms including:

- **CPU Scheduling** (FCFS, SJF Non-Preemptive, SJF Preemptive, Round Robin)
- **Banker's Algorithm** for deadlock avoidance
- **Page Replacement Algorithms** (FIFO, Optimal, LRU)

---

## How to Compile

Make sure you have Java installed. If not, download it from the [official site](https://www.oracle.com/java/technologies/javase-downloads.html).

Open a terminal or command prompt in the directory of the code and run:

```bash
javac main.java
```

This will compile the Java source file and generate a `main.class` file.

---

## How to Run

After compiling, run the program using:

```bash
java main
```

The main menu will appear:

```
==== OS Simulator ====
1. CPU Scheduling
2. Banker's Algorithm
3. Page Replacement Algorithms
4. Exit
```

Select the desired option by entering the corresponding number.

---

## Sample Output

### CPU Scheduling (FCFS)

```
Enter number of processes: 3
Enter arrival time for P1 : 0
Enter burst time for P1: 4
Enter arrival time for P2 : 2
Enter burst time for P2: 3
Enter arrival time for P3 : 3
Enter burst time for P3: 1

Process Arrival Burst Waiting Turnaround
P1      0       4     0        4
P2      2       3     2        5
P3      3       1     4        5

Average Waiting Time: 2.00
Average Turnaround Time: 4.67

Gantt Chart:
|  P1  |  P2  |  P3  |
0     4     7     8
```

### Banker's Algorithm

```
Enter number of processes (n): 3
Enter number of resource types (m): 3

Enter Allocation Matrix:
0 1 0
2 0 0
3 0 2
Enter Max Matrix:
7 5 3
3 2 2
9 0 2
Enter Available Vector:
3 3 2

Need Matrix:
P0: 7 4 3
P1: 1 2 2
P2: 6 0 0

System is in a SAFE state.
Safe sequence: P1 P2 P0
```

### Page Replacement Algorithms

```
Enter number of frames: 3
Enter number of pages in reference string: 12
Enter reference string:
7 0 1 2 0 3 0 4 2 3 0 3

==== Page Replacement Summary ====
Algorithm  Page Faults   Hit Ratio      Miss Ratio
FIFO       9             0.25           0.75
Optimal    6             0.50           0.50
LRU        7             0.42           0.58
```

---

## Notes

- Make sure to enter inputs exactly as prompted to avoid runtime errors.
- All user inputs are handled via the console.
- The code is modular and can be extended with more scheduling or memory algorithms.

---
