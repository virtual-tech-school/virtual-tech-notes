Contribute notes based on [this](https://www.youtube.com/watch?v=xVaC_G6aeH0&list=PL2kSRH_DmWVZp_cu6MMPWkgYh7GZVFS6i&index=3) video now!

# 3 standard streams.

What happens when we execute a command?
Linux by default has 3 standard streams.
## stdin (standard input)   code - 0
## stdout (standard output) code - 1
## stderr (standard error)  code - 2 
Streams job is to transfer data (simple text)
It takes input and gives output.
1. output can be in terminal.
2. in some file.
3. or in pipe -> which redirects it.
if you want to redirect > symbol is used.
eg. ls > output.txt
this command overwrites the data.
to append 
ls >> output.txt   is used.

## stderr
lg > output.txt
this command gives error.
to tackle this 
lg 2> output is used 
because error is denoted by 2.

lg 2> /dev/null --> to nullify error.

### less
opens output in seperate window.
eg. less /var/log/syslog.

To view large files without populating your terminal.

ls -la /etc | less

# pipe 
takes input of one command and feeds it to next command as standard input.

## environment variables 
stores and provides useful information that shells and processes can use.

pwd - gives present working directory.
Maintains a present working directory.
Path environment variable - contains all the path that your pc 
will search whenever you enter a command.
### Everything in linux is file even the commands.

# Some commands.
1. head -> prints first 10 lines of file 
eg head output.txt 
eg head -n 15 output.txt (prints first 15 lines of file)

2. tail -> prints last 10 lines of file 
eg tail output.txt 
eg tail -n 15 output.txt (prints last 15 lines of file)

3. sort gives sorted version of the file.
eg sort testing.txt
eg sort -r testing.txt (reverse sort)

4. translate 
eg cat testing.txt | tr a-z A-Z (from lowercase to uppercase)

5. uniq 
gives unique value in a file
eg uniq testing.txt
eg uniq -c testing.txt (gives no of occurance)

drawback -> only works wheb duplicates are next to each other.

6. wc (word count)
eg wc testing.txt (gives no of lines , words , letters in the file)
 
7. grep 
allows you to search file for characters 
eg. env | grep PWD
works with regular expression.



