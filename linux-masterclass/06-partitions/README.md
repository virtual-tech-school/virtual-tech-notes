No notes available. Contribute notes based on [this](https://www.youtube.com/watch?v=PbMT53jaUaU&list=PL2kSRH_DmWVZp_cu6MMPWkgYh7GZVFS6i&index=6) video now!
# File System
## Type Characteristics

| Symbol  | Type Characteristic |  description |
| ------------- | ------------- |-----------|
| d | directory  | collection of files|
| l |  link | link to a directory of file |
| - | file  | stream of data |
| c | character |a character device which passes/shares data char by char|
| b |  block | a block device transfer data in big size of blocks |
| p | pipe |transfer one process input to another process output|
| s |  socket |same as a pipe but handles more than one process |

### Common commands
```
ls -l /dev
```
## Filesystem Hierarchy
* / -> root directory
* /bin -> contains essential & ready to run binaries
* /boot -> contains bootloader files
* /dev -> contains device files
* /etc -> contains configuration files
* /home -> home directory
* /lib -> contains libraries
* /mnt -> temp mounted FS
* /opt -> optional software packages
* /proc -> process info
* /root -> home directory for root
* /sbin -> system binaries which are run by the root
## Journaling
Used to repair any inconsistencies that occur as the result of an improper shutdown of the computer
Suppose you were copying a file, if the system then also we can able to identify the currupt file by using *journaling*.

## Desktop file types
|Destop file types| Description|
|---|---|
| ext 4 | latest & standard choice of file system which support disk space of 1exabyte of file sixe 16 TB|
| Btrfs| Butter/Better file system and it is not stable than other|
| XFS |  high performance journaling file system generally good for servers|
| NTFS & FAT| windows file system|
