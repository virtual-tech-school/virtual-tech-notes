Contribute notes based on [this](https://www.youtube.com/watch?v=xVaC_G6aeH0&list=PL2kSRH_DmWVZp_cu6MMPWkgYh7GZVFS6i&index=3) video now!

## **3 standard streams.** ## 

What happens when we execute a command? Linux by default has 3 standard streams:
<ul>
 <li> stdin (standard input)   code - 0</li>
 <li>stdout (standard output) code - 1</li>
 <li> stderr (standard error)  code - 2</li> 
</ul>
Stream's job is to transfer data (simple text), takes input and gives output.<br>
<ul>
<li> output can be in terminal.</li>
<li> in some file.</li>
<li> or in pipe which redirects it.</li>
</ul>
If you want to redirect, (>) this symbol is used.
Eg : <code>ls > output.txt</code>
this command overwrites the data.<br> To append the data, 
<code>ls >> output.txt</code> is used.

## **stderr**
Now the <code>lg > output.txt</code> command gives an error, to tackle this 
<code>lg 2> output.txt</code> is used because error is denoted by 2.

> lg 2> /dev/null : to nullify error.

## **less**
Opens output in seperate window.
Eg: <code>less /var/log/syslog</code>

To view large files without populating your terminal. Do <code>ls -la /etc | less</code>
to close the seperate window press "q"

## **pipe** 
Takes standard output of one command and feeds it to the next command as standard input.

## **Environment Variables**
It store and provide useful information that shells and processes can use.

**pwd** - gives present working directory.
Maintains a present working directory.<br>
**Path environment variable** - contains all the path that your pc 
will search whenever you enter a command.
> Everything in linux is file even the commands.

## **Some commands.**
<ol>
    <li> <strong>head</strong> : prints first 10 lines of file. <br>
eg : <code>head output.txt</code>. <br>
eg : <code>head -n 15 output.txt</code> (prints first 15 lines of file)</li>

<li> <b>tail</b> : prints last 10 lines of file .<br>
eg : <code>tail output.txt</code> <br> 
eg : <code>tail -n 15 output.txt</code> (prints last 15 lines of file)</li>

<li> <b>sort</b> gives sorted version of the file.<br>
eg : <code>sort testing.txt</code><br>
eg : <code>sort -r testing.txt</code> is for reverse sorting.</li>

<li> <b>translate</b> <br>
eg : <code>cat testing.txt | tr a-z A-Z</code> (from lowercase to uppercase)</li>

<li> <b>uniq</b> gives unique value in a file.<br>
eg : <code>uniq testing.txt</code><br>
eg : <code>uniq -c testing.txt</code> (gives number of occurances).</li>

>Drawback: only works when the duplicate words are next to each other.

<li><b> wc</b> (word count)<br>
eg : <code>wc testing.txt</code> (gives no of lines, words, letters in the file)</li>
 
<li> <b>grep</b> used in searching and matching text files contained in the regular expressions. <br>
eg : <code>env | grep PWD</code>
</ol>


