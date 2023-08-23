Those who would like to make improvements in the future - You can help us improve notes based on [this](https://www.youtube.com/watch?v=cnbvsWKf-qM&list=PL2kSRH_DmWVZp_cu6MMPWkgYh7GZVFS6i&index=5) video.
# Processes
Processes are just programs that are running on linux machine. This processes are generally managed by kernel and each process have a **PID**(process id). Process
are terminated when terminal associated with it is closed.

## General commands of processes

| command | description | |
| ------------- | ------------- |---------------------- |
| `ps`  |  list current processes of shell | ![2](https://user-images.githubusercontent.com/120579608/227507812-9acd8fbe-23ad-4187-ab05-99064b00b8b8.PNG) |
| `ps aux`  |  list all processes | ![Capture 2](https://user-images.githubusercontent.com/120579608/227507591-6a53a541-11e3-499b-aceb-f19372d684cd.PNG) |
| `top`  | list all real time processes  | ![Capture 3](https://user-images.githubusercontent.com/120579608/227507703-4f7e9dd7-4f5b-468a-89dc-35a769707a94.PNG) |

## How process starts

New process in the linux system starts by mechanism know as **Fork System Call**. In this the new process(child) **clone** the **present process**(parent 
process) by requesting the kernel. Kernel decides the resources to the process.

```mermaid
graph TD;
    init-->|fork system call|gnomeProcess
    gnomeProcess-->|fork system call|BashProcess;
    BashProcess-->|fork system call| process;
```
### Mother Process

 Mother Process is the **first process** initiated by the kernel when system **boot up** which has PID of **1**. Mother process is also known as **init** and this process runs on **root** privileges.
 
### Daemon Process

Daemon process are the **child process** of mother. This are responsible for keeping the system running.
    
```mermaid
graph TD;
    init-->DaemonProcess1;
    init-->DaemonProcess2;
    init-->DaemonProcess3;
    init-->DaemonProcess4;
```

## How process terminates
 Termination of process is done by **exit system call** and **wait system call** . Kernel knows whether the process is terminated or not by **termination status**. For the successful process termination status is **0**. Termination process includes the cleaning of resources utilized by the process.
 
### Wait system call
 Parent process should acknowledge the kernel by **wait system call** for completion of termination process of child. The wait system call is used by a parent process to wait for its child process to terminate and obtain its termination status.
 
### Orphan Process
  If parent process dies,then the child process of it is adopted to the **mother**(init) by the kernel for termination of the process. So, that mother can able to acknowledge the termination process by wait system call. In this case, the child process is known as **orphan process**.

```mermaid
graph TD;
    Parent-->|X|Child;
    Child-->init;
    init-->|wait system call|Child;
```

### Zombie Process
 When the child process termination is not acknowledge by the parent ,then the child process is treated as **zombie process** by the kernel. Further,if parent process acknowledge the zombie process termination then this is known as **reaping**. If reaping didn't occurs then the **wait system call** is done by mother to terminate **zombie process**.

# Signals
 It is a notification to the process that something has happened.

### Common signals

|  Signal |  Description |
| ------------- | ------------- |
|  `SIGHUP/HUP/1` |  HangUp |
| `SIGINT/INT/2`  | Interrupt  |
| `SIGKILL/KILL/9`  |  Kill | 
|  `SIGSEGV/SEGV/11` | Segmentation fault  |
| `SIGTER/TERM/15`  | Terminate  |
| `SIGSTOP/STOP/19`  |  Stop | 


### Nice & Renice

Processes aren't continously run by the system. They are divided in timeslots known as time slice in CPU and as cyclic as shown in below example. So, the process will take almost same time. But, we can prioritize the process by **nice & renice** command. And every process has nice which indicates priority value. If the nice value is less,the system will prioritize more or vice versa.

---
Process cycle in CPU
---
```mermaid
flowchart LR
   P1 -->|t1| P2
   P2 -->|t2| P3
   P3 -->|t3| P4
   P4 -->|t4| P1
```
| Command |  Description |
| ------------- | ------------- |
|  `nice -n priorityValue newProcess` | for new process |
|  `renice priorityValue -p processId` | for already exit process |

### Signal Mask

Signal mask is used to block signals but there are some signals like *kill* can't be blocked.

# States of process

| State of process |  Description |
| ------------- | ------------- |
|  `R` | The process is running |
|  `S` | Interruptable sleep |
|  `D` | Uninterruptable sleep |
|  `Z` | Zombie |
|  `T` | Stopped |

