Improve notes based on [this](https://www.youtube.com/watch?v=m52OeR-mfYo&list=PL2kSRH_DmWVZp_cu6MMPWkgYh7GZVFS6i&index=8) video now!

# Resource utilization
```
top 
```
If we run the above command ,we can observe the resource utilization by process running currently.
![image](https://user-images.githubusercontent.com/120579608/229365335-210e7c1f-49b3-4985-8c2c-92b4aaf24893.png)

When we run this command , we can observe that how many tasks are running ,sleeping ,stopped and zombie process. And how much CPU memory used by system (sy) ,nice (ni), otherthan nice (us),hardware (hi), software (si) , virtual machine (st) processes , waiting for system calls (ws).
```
top -p PID 
```
This commands list resourse utilization of specific process . Here PID stands for process id.

## List of files 
```
lsof
```
![image](https://user-images.githubusercontent.com/120579608/229370180-75b39970-d309-4bf0-919c-e6e6ae04b827.png)

tells us about the files that are currently in use and associate process with them. 

## Threads

 It is an execution unit that is a part of process. A process can have multiple threads all executing at same time.
 ```
 ps -m 
 ```
 The above command to check the threads of process.

 ## Load Average
 Load Average in Linux takes into account the waiting threads and tasks along with processes being executed. Also, it is an average value instead of being an instantaneous value.
![image](https://user-images.githubusercontent.com/120579608/230596431-bfc86736-d074-4bcf-95ea-e5aa96220a6e.png)

 ### CPU load
 Average number of processes waiting to be executed by CPU.
 ## Logging
 
Whatever happening in our system is getting saved as logs in `/var` directory .
 ```
 ls /var/log
 ```
 ![image](https://user-images.githubusercontent.com/120579608/229372683-0d7f2c3a-2cc3-4657-b11a-d2ba5380109b.png)

  logs are created via service `syslog` which is implemented by syslogd daemon and sends all info to system logger.

## Logrotate
Designed to ease administration of system that generates large no.of log files by allowing removal ,rotation ,compression and maling of log files.

```
ls /etc/logrotate.log
```
This directory contains the configuration for log rotation of files.

```
cat /etc/logrotate.log/apt
```
![image](https://user-images.githubusercontent.com/120579608/229374379-ee6beaf2-7c23-4382-a9ef-5c30fe69535d.png)

![image](https://user-images.githubusercontent.com/120579608/229374626-9ae0285f-05a2-4788-ae40-6e2ee05ad8f2.png)

 In the above example when we observe the apt log file ,we can observe configuration settings. 
