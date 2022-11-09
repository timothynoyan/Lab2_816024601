## Question 2a Discussion

Round Robin Scheduling is a CPU scheduling algorithm that executes each process for a fixed time slot. Round robin is preemptive because the resources are snatched after the time slot.

In this application, three tasks were created in app_main:
* task 1 - Turns LED on
* task 2 - Turns LED off
* task 3 - Prints a status message of the pin state

All tasks were set to the same priority level of 1 for round robin scheduling. As seen in the output file, Task 1 runs first, however, Task 3 runs at the same time and completes before Task 1 is finished. Then, Task 2 runs and Task 3 also runs at the same time and finishes. At another instance, Task 1 runs, then Task 3 and then Task 2. The reason for this may be that the task which is running may still have the mutex key. This results in a variation of task run time. The expected run time for Task 1 and Task 2 should be similar and a bit longer than Task 3. This is because Task 3 has a smaller execution time than Task 1 and Task 2.
