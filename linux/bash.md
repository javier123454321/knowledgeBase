# The Bourne Again Shell BASH

linux redirects all outputs to a file called stdout

This is a temporary file that gets printed on the command line and then destroyed. 
ls actually writes the contents of a directory to the stdout file

> is called a redirect, and it tells it where to put the contents that result from the program just inputed

so ls == ls > stdout
and ls > ls-output.txt just creates a new file ls-output.txt with  what would have been shown to the screen.
if you make an error like `$ ls nonexitentDirectory > ls-output.txt` the output would still be No such file or directory on the shell. That is because there was an error, so the output was not sent to stdout, but to stderr. 
Likewise stdin listens to the inputs from the keyboard. 

input is labeled as 0, output as 1, and error as 2

So to redirect the error, you use a 2 operator 
`$ ls -l /bin/usr 2> ls-error.txt` 

`$ ls -l /bin/usr > ls-output.txt 2>&1` redirects both
