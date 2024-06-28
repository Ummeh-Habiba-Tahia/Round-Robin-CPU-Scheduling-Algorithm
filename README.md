# Round-Robin-CPU-Scheduling-Algorithm
##Description:
This C++ code implements the Round Robin scheduling algorithm, which is a preemptive scheduling algorithm used by operating systems for process scheduling. It ensures that all processes get a fair share of the CPU by allocating a fixed time slice (quantum) for each process.

Code Breakdown:

1.Include Statement and Namespace:

#include<iostream>: for input and output operations.
using namespace std; directive allows the use of standard library names without the std:: prefix.

2.Function findWaitingTime:

This function calculates the waiting time for each process.
Parameters:
    processes[]: array of process IDs.
    n: number of processes.
    bt[]: array of burst times.
    wt[]: array to store waiting times.
    quantum: time quantum.
It creates a temporary array rem_bt[] to store the remaining burst times.
A loop runs until all processes are done.
For each process, if the remaining burst time is greater than the quantum, it adds the quantum to the current time and reduces the remaining burst time. If the remaining burst time is less than or equal to the quantum, it adds the remaining burst time to the current time, calculates the waiting time, and sets the remaining burst time to zero.

3.Function findTurnAroundTime:

This function calculates the turnaround time for each process.
Parameters:
     processes[]: array of process IDs.
     n: number of processes.
     bt[]: array of burst times.
     wt[]: array of waiting times.
     tat[]: array to store turnaround times.
It calculates the turnaround time by adding the burst time and waiting time for each process.

4.Function findavgTime:

This function calculates and prints the average waiting time and turnaround time.
Parameters:
      processes[]: array of process IDs.
      n: number of processes.
      bt[]: array of burst times.
      quantum: time quantum.
It declares arrays wt[] and tat[] to store waiting times and turnaround times, respectively.
Calls findWaitingTime and findTurnAroundTime to calculate waiting times and turnaround times.
Prints the process details, waiting times, and turnaround times.
Calculates and prints the average waiting time and average turnaround time.

5.Main Function:

It prompts the user to enter the number of processes.
Initializes the processes[] array with process IDs.
Prompts the user to enter the burst time for each process.
Prompts the user to enter the time quantum.
Calls findavgTime to calculate and display the average waiting time and turnaround time.

Example Execution:

User is prompted to enter the number of processes.
User enters the burst time for each process.
User enters the time quantum.
The program calculates and prints the waiting time and turnaround time for each process, along with the average waiting time and average turnaround time.

Output:

Enter the number of processes: 3
Enter burst time for process 1: 10
Enter burst time for process 2: 5
Enter burst time for process 3: 8
Enter the time quantum: 2
PN              BT        WT            TAT
 1              10      13              23
 2              5       10              15
 3              8       13              21
Average waiting time = 12
Average turn around time = 19.6667
