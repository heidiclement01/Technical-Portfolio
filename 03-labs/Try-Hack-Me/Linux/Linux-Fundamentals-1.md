
# Linux Fundamentals I

## Platform:  TryHackMe

## Learning Objectives:

- Understand the Linux filesystem.
- Navigate directories from the command line.
- Use common Linux commands.
- Search for files.
- Redirect command output.

## Technical Notes:

- Similiar to how you have different versions of Windows (7, 8, 10, and 11), there are many different versions/distributions of Linux.
- No native GUI, though can be added or downloaded
- Command line is known as terminal
  - EX:  Looks like tryhackme@linux1.~$

| Command | Description |
| ------- | ------------- |
| echo | Output any text that we provide;  use double quotes if there are spaces or multiple words, Ex:  echo Hello vs echo "Hello Friends!" |
| whoami | Find out what user you're logged in as. |

| Command | Full Name | Description | Examples |
| ------- | ---------- | ------------- | ---------- |
| ls | listing | Lists contents of current directory | |
| cd | change directory | Changes directory you are in | EX:  cd folder1 (takes you to folder 1 directory);  EX 2:  cd .. (takes you to the next directory up_.) |
| cat | concatenate | Displays contents of files;  WARNING:  May be unruly so better to use grep | |
| pwd | print working directory | prints the absolute path of your current folder from the root directory | |
| find | find | Search style function used to find items | EX:  find -name bob.txt;  EX 2:  find -name *.txt (* is a wildcard) |
| grep | Global Regular Expression Print | Searches plantext for matching entries |  EX:  grep "THM" access.log |

| Symbol/Operator | Description | Example |
| --------- | -------- | -----------|
| & | Allows you to run commands in the background of your terminal. | |
| && | Allows you to combine multiple commands together in one line of your terminal | EX: Command1 && Command2 - Command2 will only run if Command1 is successful |
| > | Redirector that takes output from a command, such as using cat to output a file, and direct it elsewhere. | EX:  echo hey > Welcome;  Will create Welcome if not already there;  Will overwrite Welcome with 'hey' if it already exists |
| >> | Does the same function of the > operator, but appends the output rather than replacing (meaning nothing is overwritten) | EX:  echo hey >> Welcome |

## Important Takeaways

- Linux is an OS, like Windwos.  There are many different versions of Linux that serve different purposes.
- Linux is based off the UNIX system.
- Linux is open-sourced with Debian and Ubuntu extremely common due to being more extensible, such as Ubuntu being able to be used as server or desktop
- Linux systems rely more heavily on command line to do tasks like navigate the file system.
- Some basic commands while working with files are ls, cd, cat, and pwd.  
