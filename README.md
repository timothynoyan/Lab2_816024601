## Question 2b Discussion

In this application, three tasks were created in app_main:
* task 1 - Turns LED on
* task 2 - Turns LED off
* task 3 - Prints a status message of the pin state

For the output file q2b_123, the priority levels were assigned as follows:
	-Task 1 - 3
	-Task 2 - 2
	-Task 3 - 1
	
For the output file q2b_132, the priority levels were assigned as follows:
	-Task 1 - 3
	-Task 2 - 1
	-Task 3 - 2
	
For the output file q2b_213, the priority levels were assigned as follows:
	-Task 1 - 2
	-Task 2 - 1
	-Task 3 - 3
	
For "*q2b_123*", task 1 ran first, actively waited for 0.5 seconds, then it was task delayed for 1 second. Then, task 2 ran, actively waited for 0.5 seconds and was task delayed for one second. Lastly, task 3 ran and task delayed for one second. This was expected since priority inheritance never occurred because the task with the highest priority always ran before the task with the lowest priority.

For "*q2b_132*", task 1 ran first, actively waited for 0.5 seconds, then it was task delayed for 1 second. Then, task 3 ran and task delayed for one second. Lastly, task 2 ran, actively waited for 0.5 seconds and was task delayed for one second. This was expected since priority inheritance never occurred because the task with the highest priority always ran before the task with the lowest priority.

For "*q2b_213*", in the output file, we can see that priority inheritance is taking place from lines 33-55. When priority inheritance occurs, the lower priority tasks runs before the higher priority tasks. In the output file, task 1 runs first, the  task 2, and lastly, task 3 runs. In the cases of priority inheritance, task 1 inherited the priority of task 3 and task 2 inherited the priority of task 1. This only occured initally and then it worked as expected where task 2 runs, then task 1 runs and lastly, task 3 runs. Even though there were occurrences of priority inheritance, the length of time each task took was not affected. Only the order at which the tasks ran was affected.
