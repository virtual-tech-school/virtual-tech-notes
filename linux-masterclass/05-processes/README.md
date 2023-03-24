# Processes
Processes are just programs that are running on linux machine. This processes are generally managed by kernel and each process have a **PID**(process id).Process
are closes when terminal associated with it is closed.

## General commands of processes

| command | description | |
| ------------- | ------------- |---------------------- |
| `ps`  |  list current process of shell | ![2](https://user-images.githubusercontent.com/120579608/227507812-9acd8fbe-23ad-4187-ab05-99064b00b8b8.PNG) |
| `ps aux`  |  list all process | ![Capture 2](https://user-images.githubusercontent.com/120579608/227507591-6a53a541-11e3-499b-aceb-f19372d684cd.PNG) |
| `top`  | list all real time process  | ![Capture 3](https://user-images.githubusercontent.com/120579608/227507703-4f7e9dd7-4f5b-468a-89dc-35a769707a94.PNG) |

## How process starts


---
General example
---
```mermaid
graph TD;
    init-->|fork system call|gnemeProcess
    gnemeProcess-->|fork system call|BashProcess;
    BashProcess-->|fork system call| p5;
```
### Mother Process

 Mother Process is the **first process** initiated by the kernel when system **boast up** which has PID of **1**.Mother process is also known as **init** and this process runs on **root** previledge.
 

 

### Demon Process
```mermaid
graph TD;
    init-->DemonProcess1;
    init-->DeomonProcess2;
    init-->DeomonProcess3;
    init-->DeomonProcess4;
```

## How process terminates
 Termination of process is by **exit system call**. Kernel known whether the process is terminated or not by **termination status**. For the successfull process termination status is **0**.



### Orphan Process

```mermaid
graph TD;
    ParentX-->Child;
    Child-->init;
    init-->|wait system call|D;
```

### Zombie Process


# Signals
|  Signal |  Description |
| ------------- | ------------- |
|  `SIGNHUP/HUP/1` |  HangUp |
| `SIGINT/INT/2`  | Interput  |
| `SIGNKILL/KILL/9`  |  Kill | 
|  `SIGSEGV/SEGV/11` | Segmentation fault  |
| `SIGTER/TERM/15`  | Terminate  |
| `SIGSTOP/STOP/19`  |  Stop | 


### Nice & Renice
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



