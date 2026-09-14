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

