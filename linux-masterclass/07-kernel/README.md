Contribute notes based on [this](https://www.youtube.com/watch?v=08SwnaMhL1k&list=PL2kSRH_DmWVZp_cu6MMPWkgYh7GZVFS6i&index=7) video now!

# Boot Process

## Stages of boot process
### 1. BIOS 
basic input output system. It initialises the hardware, it makes sures the hardware is good to go , by running self tests in which it checks , memory is good, hdd, ssd etc. 
Main job of Bios is to load the bootloader.

### 2. Bootloader 
loads the kernel into the memory. Whatever RAM you have , this bootloader is going to load the code of that kernel in the memory based on whatever kernel parameters you are having.
Commonly used boot loader --> GRUB bootloader

### 3. Kernel 
As soon as it is loaded, it immediately initialises the memory and the devices that are there in the system.
Main job is to load the init process or mother process.
Init process- starts and stops all the essential process; It is the very first process (mother process)

# Levels of abstraction of Linux OS
### 1. Hardware
CPU, memory ports, HDD, SSD etc. Physical layer which computes what our system is doing.
### 2. Kernel 
Responsible for handling processes, memory, device communication, setting up entire file system, also responsible for for system calls.
### 3. User Space
All we see in front of us, apps comes under user space.

## Privilege levels and protection rings

Kernel- operates kernel mode
User- operates on user mode

For security reasons whenever we do anything related to hardware , something as easy as reading/writing, controlling networking port it is done in kernel mode.

### System call 
Allows us to perform some privileged instruction in the kernel mode then it let's you get back to the user mode. (also known as syscalls)

System call API- provides user space application, processes, a way to request kernel to do something for us they make some services available to us this service is known as system callAPI.

# Implementation of init process

## 1. System V             2. upstart                   3. Systemd
      Traditional             used earlier in ubuntu       New Standard

## System V implementation
Start and stops process sequentially.
Disadvantage- performance is not great as processes are starting stopping one at a time.
### System V runlevels
0 - shutdown
1 - single user
2 - multiuser without networking
3 - multiuser with networking
4 - unused
5 - multiple users with networking & GUI
6 - Rebooting

### command To check all services  
service --status-all

To start stop restart service
sudo whoopsie start/stop/restart

## Upstart init implementation
Created to improve system V implementation
Upstart- events in jobs model

Jobs- actions performed
Events- messages received from other processes

## Systemd
Uses goals to get your system up and running.
Goals- targets which needs to be achieved.

## Targets

1 poweroff.target - shutdown
2 rescue.target - single user
3 multiuser.target - for multiusers with networking 
4 graphical.target - multiuser with networking & GUI
5 reboot.target - reboot

### Managing power status of the system
sudo shutdown -h now (to shutdown rightnow)
sudo reboot (to reboot)






