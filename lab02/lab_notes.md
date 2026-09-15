# Lab notes to prove I did something

## Commands:
 - Current User: `whoami`
 - System Hostname: `hostname`
 - Current Date & Time: `date`
 - Current Working Directory: `pwd`
 - Print the contents of the workind (or defined) directory: `ls`
    - Flag `-l` will give more info, such as permissions and ownership of the files listed
    - Flag `-a` will show hidden files (which start with a dot)
    - You can combine both flags with `-la` or `-al`, order doesn't matter

## Exercise 3
steps to take:
`pwd` displays your current directorie ->
`cd ..` moves to the parent dir ->
`ls -la` lists its contents ->
`cd ./lab02` moves back into the lab dir ->
`pwd` confirms my location

## Exercise 5
steps taken:
 - `touch system.txt` - To create the file (optional)
 - `whoami > system.txt` - Putting the username in the file
 - `hostname >> system.txt` - Appending the hostname to the file
 - `date >> system.txt` - appends the current date & time to the file
 - `pwd >> system.txt` - appends the current working dir to the file

(`(whoami && hostname && date && pwd) > system.txt` also works)

## Exercise 6
 - Flag `-h` or `--human-readable` displays human readable file sizes
 - Flag `-t` to sort by modification time
 - Flag `-p` or `--parents` allows it to create the parrent directories
 - the `cat` command concatenates files and prints on the std output

## Exercise 7
Here's each line that I used:

```bash 
name="Uriel"
course="IT Management"
year=2

echo "$name is studying $course in Year $year"
```
## Exercise 8

- `$USER` - value prints the current user ("codespace")
- `$HOME` - variable is the home (~) address ("/home/codespace")
- `$SHELL` - is the adress of the shell that is used (/bin/bash)
- `$PATH` - is all of the directories from which shell can get commands

$PATH is the variable with multiple directories listed
$PATH output:
```
/vscode/bin/linux-x64/645f29cc3176500b4b5762ba887cf2a7f0ffdf2c/bin/remote-cli:/home/codespace/.local/bin:/usr/local/rubies/current/bin:/home/codespace/.dotnet:/home/codespace/nvm/current/bin:/home/codespace/.php/current/bin:/home/codespace/.python/current/bin:/home/codespace/java/current/bin:/home/codespace/.ruby/current/bin:/home/codespace/.local/bin:/usr/local/python/current/bin:/usr/local/py-utils/bin:/usr/local/jupyter:/usr/local/oryx:/usr/local/go/bin:/go/bin:/usr/local/sdkman/bin:/usr/local/sdkman/candidates/java/current/bin:/usr/local/sdkman/candidates/gradle/current/bin:/usr/local/sdkman/candidates/maven/current/bin:/usr/local/sdkman/candidates/ant/current/bin:/usr/local/share/rbenv/shims:/usr/local/share/rbenv/bin:/usr/local/rubies/current/bin:/usr/local/php/current/bin:/opt/conda/bin:/usr/local/share/nvm/versions/node/v24.20.0/bin:/usr/local/hugo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/share/dotnet:/home/codespace/.dotnet/tools
```

## Exercise 9

Locations of commands:
 - `bash` - /usr/bin/bash
 - `python3` - /home/codespace/.python/current/bin/python3
 - `grep` - /usr/bin/grep
 - `cat` - /usr/bin/cat

## Exercise 10
double quotes allow for variable expantions and single quotes treat it literally

```bash
module="Scripting"

echo "Module is $module" # output produces "Module is Scripting"
echo 'Module is $module' # output produces "Module is $module"
```


## Exercise 11
Command substitution

```bash
name=$(whoami)
hostname=$(hostname)
curr_dir=$(pwd)

echo "$name is logged in on the $hostname machine and is currently in $curr_dir"
```

## Exercise 13
using wc and pipes

```bash
#This is done in the lab02 dir
ls | wc -l # produces 13
ls -la | wc -l # produces 16
env | wc -l # produces 87
```

This means that there are 13 files in the current directory, and 87 environmental variables on the system

