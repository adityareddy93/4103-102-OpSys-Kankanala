# chapter 2 review questions
Name: Aditya Reddy Kankanala

Course: 4103 Operating Systems

Date: 17 Oct 2016

##Multi-Tasking:
Multi-tasking more than one task are executed at the same time. In this technique the multiple tasks, also known as processes, share common
processing resources such as a CPU. In the case of a computer with single CPU, only one job can be processed at a time. Multitasking
solves the problem by scheduling and deciding which task should be the running task and when a waiting task should get turn.
### Example
Using excel or mediaplayer on the computer, accessing web browsers simultaneously.

##Multi-Programming:
Multi-programming is the technique of running several programs at a time using timesharing. It allows a computer to do several things at
the same time. Multiprogramming creates logical parallelism. The concept of multiprogramming is that the operating system keeps several
jobs in memory simultaneously.
### Example
Editing in word dcument, running a program and anti virus scanning your PC, all these can happen at a time.

##Multi-Processing:
Multi-processing refers to executing multiple processes (programs) at the same time. Multiprocessing operating systems enable several programs to run concurrently.
### Example
Multiple core processors like dual core processor.

##Multi-Threaded:
Multi-threading is an execution model that allows a single process to have multiple code segments run concurrently within the “context” of that process.
### Example
database 


##REVIEW QUESTIONS AND ANSWERS FOR CHAPTER 3

##1.What is a instruction trace?
An instruction trace for a program is the sequence of instructions that execute for
that process.        

##2.What common events lead to the creation of a process?
   There are four principal events led to creation of process:
       1.System initialization.
       2.Execution of a process Creation System calls by a running process
       3.A user request to create a new process
       4.Initialization of a batch job

##3.what does it mean to preempt a process?
    The ability of the operating system to pause or stop a currently scheduled task in favour of a higher priority
    task. The resource being scheduled may be the processor or I/O, among others.
    
##4.What is swapping and what is its purpose?
    Swapping is a simple memory/process management technique used by the operating system to increase the utilization of the
    processor. The purpose of swapping is moving some blocked process from the main memory to the secondary memory, thus forming a queue
    of temporarily suspended process and the execution continues with the newly arrived process.
    
##5.Why does figure 2.9 have two blocked states?
To know whether a process is waiting on an event and to obtain more memory so that it can be obtained by using secondary memory .

##6.List four characteristics of a suspended process?
    *The process is not immediately available for execution.
    *The process may or may not be waiting on an event. If it is, this blocked condition is independent of the suspend condition, and
     occurrence of the blocking event does not enable the process to execute immediately.
    *The process was placed in a suspended state by an agent: either itself, a parent process, or the OS, for the purpose of preventing
     its execution
    *The process may not be removed from this state until the agent explicitly orders the removal.
    
##7.List three general categories of information in a process control block?
    *Process identification data
    *process state data
    *process control data
 
##8.Why are two modes (user and kernel) needed?
    ###kernel:
              It can execute any CPU instruction and reference any memory address. Kernel mode is generally reserved for the lowest-level, most
    trusted functions of the operating system. Crashes in kernel mode are catastrophic, they will halt the entire PC.
    ###user:
            Code running in user mode must delegate to system APIs to access hardware or memory. Due to the protection afforded by this sort
      of isolation, crashes in user mode are always recoverable. Most of the code running on a computer will execute in user mode
      
##9.What is the difference between an interrupt and a trap?
    ###Interrupt:
       1.An interrupter is generated by hardware devices like hard disk,graphic card, i/o ports.
       2.Occurrences of hardware interrupts usually disable other hardware interrupts.
       3.These are asynchronous, They don't happen at predictable places in the user code.
    ###Trap:
       1.traps are software-invoked interrupts.
       2. It's caused by division by zero or invalid memory access.
       3.Handling is synchronous, the user code is suspended and continues afterwards.
       
##10.Give three examples of an interrupt?
 Clock interrupt, I/O interrupt, memory fault are three examples.

##11.What is the difference between a mode switch and a process switch?
     ###process switch:
        1.Process switch is the switch the process state between the status like read,blocked,suspend.
        2.it is more expensive compared to process mode switch.
     ###mode switch:
        1.mode switch is the switch the process previlege between the mode like user mode,kernel mode.
        2.mode switch is considered less expensive.
        
