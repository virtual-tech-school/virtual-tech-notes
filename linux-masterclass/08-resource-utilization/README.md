Improve notes based on [this](https://www.youtube.com/watch?v=m52OeR-mfYo&list=PL2kSRH_DmWVZp_cu6MMPWkgYh7GZVFS6i&index=8) video now!

# Resource utilization
```
top 
```
If we run the above command ,we can observe the resource utilization by process running currently.
![image](https://user-images.githubusercontent.com/120579608/229365335-210e7c1f-49b3-4985-8c2c-92b4aaf24893.png)

When we run this command , we can observe that how many tasks are running ,sleeping ,stopped and zombie process. And how much CPU memory used by system (sy) ,nice (ni), otherthan nice (us),hardware (hi), software (si) , virtual machine (st) processes , waiting for system calls (ws).

## List of files 
```
lsof
```
![image](https://user-images.githubusercontent.com/120579608/229370180-75b39970-d309-4bf0-919c-e6e6ae04b827.png)

tells us about the files that are currently in use and associate process with them. 

## Threads

 It is an execution unit that is a part of process. A process can have multiple threads.
 
 ## Load Average
 
 ## Logging
 
Whatever happening in our system is getting saved as logs in `/var` directory .
 ```
 ls /var/log
 ```
 ![image](https://user-images.githubusercontent.com/120579608/229372683-0d7f2c3a-2cc3-4657-b11a-d2ba5380109b.png)

  logs are created via service `syslog` and sens all info to system logger.
