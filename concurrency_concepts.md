# Table of Contents:
- [Table of Contents:](#table-of-contents)
- [What is Deadlock?](#what-is-deadlock)
- [When does Deadlock occur?](#when-does-deadlock-occur)
- [Prevention and Elimination: Deadlock](#prevention-and-elimination-deadlock)
- [What is Starvation?](#what-is-starvation)
- [When does Starvation occur?](#when-does-starvation-occur)
- [Solution: Starvation](#solution-starvation)
- [Differences: Deadlock and Starvation](#differences-deadlock-and-starvation)
- [Conclusion](#conclusion)
- [References](#references)


# What is Deadlock?
* Deadlock is a situation in Operating Systems where several processes compete for a limited amount of available resources.
* Each process holds a resource and wait to acquire a resource that is held by another process.
* It never ends as both processes are waiting for each other and waiting never ends. Therefore none of the processes can complete their tasks.
* Deadlock is a common problem in multi-processing OS, distributed systems, and parallel computing.

# When does Deadlock occur?
* There are four conditions which when fulfilled leads to a deadlock:
    - Mutual exclusion: Only one process can use a resource at any instant of time, other processes will have to wait.
    - Hold and Wait:    A process that holds a resource is waiting to acquire another resource held by another process.
    - No Preemption:    A resource can only be released after the completion of the process.
    - Circular Wait:    The process must wait for resources in a closed circular manner.
    
# Prevention and Elimination: Deadlock
* Some applications can detect programs that may get deadlocked.
* Prevention of deadlock is a responsibility for programmers and not the OS.

* Some mechanisms to eliminate a deadlock after it has occurred are:
    - Preemption:   Obtain a resource from a process and allocate it to another process.
    - Rollback:     Roll everything back to the last safe state and try allocation of resources differently.
It is also possible to terminate single or multiple processes. But, this is an expensive method.



# What is Starvation?
* Starvation is a situation where a process waits for a resource for a long duration of time.
* In starvation, a process ready to execute waits for the CPU to allocate the resource.
*  But the process has to wait indefinitely as the other processes continuously block the requested resources.

# When does Starvation occur?
* Starvation usually occurs in the priority scheduling algorithm.
* Resources are shared based on process priority. Here, low priority processes get blocked, and high priority processes proceed.

# Solution: Starvation
* Aging can resolve the problem of starvation.
* Aging gradually increases the priority of a process that has been waiting for a long duration of time.
* This ensures that the low priority process does not wait indefinitely for the resource.


# Differences: Deadlock and Starvation
* In a deadlock, none of the processes completes its execution whereas in starvation process with higher priority completes its execution.
* Deadlock occurs only when all the four conditions (Mutual exclusion, no preemption, hold and wait and circular wait) are met. Starvation occurs due to uncontrolled resource management or priority-based resource management.
* In a deadlock, the resources are being blocked by other processes whereas, in starvation, resources are being used by high priority processes.
* Deadlock can be prevented by avoiding the four mentioned conditions and starvation can be prevented by aging.


# Conclusion
* Multiple processes are running in an OS, deadlock and starvation are two situations that can occur and cause wastage of resources. Programmers should maintain and use the resources efficiently.


# References
* https://www.geeksforgeeks.org/difference-between-deadlock-and-starvation-in-os/
* https://www.tutorialspoint.com/starvation-and-deadlock
* https://www.baeldung.com/cs/deadlock-livelock-starvation
