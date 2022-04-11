TASK5.3

Part1

1. How many states could has a process in Linux?

Processes in Linux have 5 states:

Running or Runnable (R);

Uninterruptible Sleeo (D);

Interruptable Sleep (S)

Stopped (T);

Zombie (Z).

2. Examine the pstree command. Make output (highlight) the chain (ancestors) of the current process.

![image](https://user-images.githubusercontent.com/97533533/162698862-2ba2c516-a36d-49e4-b0aa-b39b222638f5.png)

PSTREE - this utitite allow us to seeing tree of the proceses in system.

3. What is a proc file system?

![image](https://user-images.githubusercontent.com/97533533/162699348-3e7ea6d3-8c38-44ab-bf50-9a2ada95f539.png)

ROCFS - it's a specific virtual filesystem (does't take up disk space). In GNU/Linux processes can't access the system kernel directly and use "/proc" directory, where is concentrated all information about system, RAM, CPU, loaded modules, etc. in readeble for human format.

4. Print information about the processor (its type, supported technologies, etc.).

![image](https://user-images.githubusercontent.com/97533533/162700511-bdfbc96b-d0b3-4dcf-ae55-b5c07ca8f9d5.png)

5. Use the ps command to get information about the process. The information should be as follows: the owner of the process, the arguments with which the process was launched for execution, the group owner of this process, etc.

![image](https://user-images.githubusercontent.com/97533533/162700828-32fd52e1-c740-4b0b-9ddc-a863128a7eb3.png)

6. How to define kernel processes and user processes?

Kernek processes - is a system processes born by "kthreadd" who have id 2 and all children of this process - the kernel processes. We can seeing these processes with following command:

sudo pstree 2

![image](https://user-images.githubusercontent.com/97533533/162701203-683d2737-c3eb-4a6f-8647-cff59a5d13e3.png)

7. Print the list of processes to the terminal. Briefly describe the statuses of the processes. What condition are they in, or can they be arriving in?

![image](https://user-images.githubusercontent.com/97533533/162701760-05b0a020-f396-40b8-8158-e2267bfdf40a.png)

![image](https://user-images.githubusercontent.com/97533533/162701905-4726c907-3337-4967-b8dc-c73bd15de893.png)

8. Display only the processes of a specific user.

![image](https://user-images.githubusercontent.com/97533533/162702134-a503ecd2-2346-4d56-9d3a-ea5a6319edce.png)

9. What utilities can be used to analyze existing running tasks (by analyzing the help for the ps command)?

How we see in manual for ps (man ps), for viewing processes info we can use pgrep, pstree, top and proc.

![image](https://user-images.githubusercontent.com/97533533/162702786-eb8df4b9-1b80-462e-8362-f28e375afa42.png)

10. What information does top command display?

![image](https://user-images.githubusercontent.com/97533533/162703016-8fa8f27f-58d6-4a54-9f59-ac23eb371788.png)

11. Display the processes of the specific user using the top command.

I use command TOP with "-u" key:

![image](https://user-images.githubusercontent.com/97533533/162703372-c6111636-678d-4414-b169-4df0edc5693e.png)

12. What interactive commands can be used to control the top command? Give a couple of examples.

![image](https://user-images.githubusercontent.com/97533533/162703549-eaa6eab9-ff91-4633-977a-5ee11762e790.png)

13. Sort the contents of the processes window using various parameters (for example, the amount of processor time taken up, etc.)

Sort by CPU using:

![image](https://user-images.githubusercontent.com/97533533/162704569-63c82ce3-df9d-4f00-84ac-e80a1e5c0955.png)

Sort by Memory using:

![image](https://user-images.githubusercontent.com/97533533/162704331-5290673a-11fd-460c-8b03-cc0bfb915e3c.png)

Sort by PID using:

![image](https://user-images.githubusercontent.com/97533533/162704947-7527e894-d492-49f1-9f37-ce7859cefce1.png)

Sort by SWAP using:

![image](https://user-images.githubusercontent.com/97533533/162705283-2cd60a1b-dfac-4f9f-8e7a-bca385621c2c.png)

14. Concept of priority, what commands are used to set priority?

Process priority, like in an others OS, in Linux - is how many CPU time will be given for process compared to others. Priority have a value from 19 (the lowest priority) to -20 (the highest priority), moreover for decrease the priority you can use a regular user, but for increase - must have a superuser rights.
For control process priority we can use following commands:

set priority for launched process; nice Example - nice -n 17 apt update; renice - set priority for existing process, to indicate the process we must use PID; Example - sudo renice -n -2 -p 858.

![image](https://user-images.githubusercontent.com/97533533/162707362-cb0977e1-0453-4100-a934-f207df25bb8b.png)

15. Can I change the priority of a process using the top command? If so, how?

We can chenge pritoty in TOP with a "r" key:

![image](https://user-images.githubusercontent.com/97533533/162708424-edb941d6-274f-4cc9-9d32-44112bda94e3.png)

![image](https://user-images.githubusercontent.com/97533533/162708508-3a9170bf-87aa-4413-b76b-ae80b1a3ddde.png)

16. Examine the kill command. How to send with the kill command process control signal? Give an example of commonly used signals.

![image](https://user-images.githubusercontent.com/97533533/162708905-e39c978a-47c6-4de5-b36a-d366beeb7f21.png)

![image](https://user-images.githubusercontent.com/97533533/162708981-79aa9d2c-3734-408e-b7b9-79f9e1388111.png)
























