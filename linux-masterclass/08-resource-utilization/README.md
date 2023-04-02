Improve notes based on [this](https://www.youtube.com/watch?v=m52OeR-mfYo&list=PL2kSRH_DmWVZp_cu6MMPWkgYh7GZVFS6i&index=8) video now!

# Resource utilization
```
top 
```
If we run the above command ,we can observe the resource utilization by process running currently.
![image](https://user-images.githubusercontent.com/120579608/229365335-210e7c1f-49b3-4985-8c2c-92b4aaf24893.png)

When we run this command , we can observe that how many tasks are running ,sleeping ,stopped and zombie process. And how much CPU memory used by system (sy) ,nice (ni), otherthan nice (us),
hardware (hi), software (si) , virtual machine (st) processes.

## List of files 
```
lsof
```
tells us about the files that are currently in use and associate process with them. 

## Threads
 It is an execution unit that is a part of process. A process can have multiple threads.
