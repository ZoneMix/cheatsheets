---
Title: Bash
Created: '2020-02-07T04:41:46.455Z'
Modified: '2020-02-07T07:17:07.127Z'
---

# Bash

## About
* Bourne Again Shell
  * Replaces Stephen Bourne's shell (sh)
* Serves two purposes
  * Runs other programs
  * Scripting language interpreter
<br/>

## Basic Linux Commands
Command                     | Description 
-------                     | -----------
pwd                         | Prints current path 
ls                          | Lists directory contents 
cd                          | Changes directory 
cat [file]                  | Prints contents of [file] 
cp [file] [file]            | Copy  ***works with directories*** 
mv [file] [file]            | Move ***works with directories*** 
rm [file]                   | Remove ***-r to remove directory*** 
mkdir [dirname]             | Makes new directory 
rmdir [dirname]             | Removes directory ***-r for directory with contents*** 
touch [filename]            | Creates new file 
ln [source] [destination]   | Creates a shortcut 
su [user]                   | Switch user   
sudo [command]              | Run with root privileges 
logout or exit              | Logout or exit shell 
head [filename]             | Prints first 10 lines of file by default 
tail [filename]             | Prints last 10 lines of file by default 
chmod                       | Can change permissions in filesystem ***see options with man chmod***
who                         | Shows users logged on 
md5sum [filename]           | Prints the md5 hash of a file 
sha1sum [filename]          | Prints the sha1 hash of a file
find [path] [expression]    | Search for files matching a provided pattern 
df                          | Display used and available disk space 
free                        | Display amount of free and used memory in the system 
du                          | Show how much space each file uses 
lsblk                       | Show volumes on the system  
mount                       | View and mount volumes  
ip addr or ifconfig         | Show ip address on system 
ip route add|check <route>  | Add a static route to your system, or check a route  
ip neigh                    | View ARP table  
uname                       | Print system information 
history                     | Prints .[shell] history for the user 
man [command]               | Shows the manual for a command 
shutdown [-h]               | Shuts the system down 
reboot                      | Reboot the system 
clear                       | Clear the current buffer of the screen 
less                        | Will show contents of large file, but will not print everything at once 
more                        | Opposite of less, does the same thing pretty much, <br/>less features than ***less*** *isn't that ironic* 
nano or vim                 | Text editors within the CLI ****do not ever use vi, <br/>please use vim, you will hate it***
date                        | Print or set system date and time  
cal                         | View a pretty calendar
passwd                      | Change user password  
apropos                     | To see what commands do what you need  
pwmake <garbage>            | Make a password  
pwscore                     | Check a password's quality  
nice -n [niceness] <command>| Change the priority of a command  
bg                          | Run a process in the background  
fg                          | Bring a background process to the foreground  
jobs                        | List background jobs  
kill <pid>                  | Kill a process  
pkill <process>             | Kill all related processes
journalctl -f -u <service>  | Follow the log of a systemd service  
modprobe                    | Add or remove kernel modules  
tar -xzvf <file>            | Unzip .tar.gz  
gunzip <file>               | Unzip .tar.gz  
xxd <file>                  | Make a hexdump of the file  
drill <URL>                 | Get information about a domain  
whois <URL>                 | Get whois information for a domain  
ss -ltp                     | See list of listening TCP sockets (s/t/u for udp)  
shred <file>                | Overwrite a file with gibberish  
mount -t tmpfs -o size=8G tmpfs /mnt | Mount 8G tmpfs in /mnt  
dd                          | Destroy a disk ;)  
chattr                      | Change file attributes  
lsattr                      | List file attributes  
ln                          | Make a link  
yes                         | yyyyyyyyyyyyyyyyyyyyyyyyyyyyyyyyyyyy...
rev                         | Reverse a line in place
 
## Cheat Sheet
### Tab Completion
```
- Tab to autocomplete
- Tab Tab to show options
```  

### Scrolling
```
- Shift+PageUp
- Shift+PageDown
# TMUX
- Meta+[  (q to quit)
```

***Note: 'clear' command will get rid of the buffer***

### Command History
```
- history (shows .bash_history)
- Up arrow (prev command)
- Down arrow (next command)
- CTRL+R (recall last command with characters provided)
- !! (run last command)
- !a (run last command with 'a', can be any character provided)
- echo $? (echo exit code of previous command)
```

### Special Characters
Character | Description
--------- | -----------
<code>\#</code>       | comment
<code>\|</code>       | Pipe, passes stdout of prev command into stdin of next one
<code>\>\|</code>      | Force redirection, overwrite existing file
<code>\|\|</code>      | OR logical operator
&       | Run job in background
&&      | AND logical operator
"-"       | Prefix, used for command options
"-"       | Suffix, redirection to stdin or stdout
"-"       | cd -, goes to prev working directory (corresponds with $OLDPWD)
--      | Prefixes long options to commands
~       | Home directory (corresponds with $HOME)
~+      | Current working directory
~-      | Previous working directory
;       | Command separator
;;      | Terminator in switch case option
.       | Can be used as the source command
.       | cd . is current directory
.       | . before filename hides file from ls
"       | Partial quoting, preserves most of the special chars in a string
'         | full quoting, preserves all special chars in a string
,       | Links together arithmetic operations
\       | Escape character
/       | Filename path separator
:       | NULL command, "NOP"
!       | Reverse test or exit status
!       | Invoke bash history
\*    | Wild card, matches everything
?       | Test condition



### Regular Expressions
Character | Description
--------- | -----------
'{a..d}'  | Brace expansion, in this case it will echo 'a b c d', can pad with extra characters too
'=~'      | Regular expression match
'^'       | Beginning of line
'^,^^'    | First char uppercase
'^^'      | All chars uppercase
','       | First char lowercase
',,'      | All chars lowercase
'.'       | Character match
'?'       | Wildcard, match any character

### Redirection
Character | Description
--------- | -----------
<code>></code> | Redirect output to file
<code>>></code> | Append output to file
<code>>&</code> | Redirect output of one file to another
<code><</code> | Input file to command
<code><<</code> | Input to command until condition, like EOF
<code><<<</code> | Input to command as a string


### File Descriptors
Character | Description
--------- | -----------
<code>0</code> | STDIN
<code>1</code> | STDOUT
<code>2</code> | STDERR

### Keyboard Shorcuts
#### CTRL+ Commands
Key       | Description
--------- | -----------
C         | kill (SIGINT)
L         | clear screen
D         | logout (EOF)
Z         | suspend current foreground process return using fg 'process number'
S         | stop output to screen
Q         | resume output
A or Home | go beginning of line
E or End  | go end of line
B         | go back one character
F         | go forward one character
K         | cuts everything forward of cursor to clipboard
X         | cuts highlighted text to clipboard
XX        | move between beginning of line and the current positions
D         | delete charcter under cursor
U         | delete everything behind cursor
Y         | paste last thing yanked
_         | undo last key press
W         | cut word before cursor
P         | prev command
N         | next command
R         | recall last command with characters provided
O         | Run command you found with R
G         | leave R
I         | horizontal tab
J         | newline or enter
M         | enter
O         | newline on cli



#### ALT+ Commands
Key | Description
--- | -----------
B   | back one word
F   | forward one word
D   | delete word after cursor
H   | delete charcter before cursor
T   | swap current word with prev word
U   | capitalize word after cursor
L   | lowercase word after cursor
C   | capitalize character on cursor
R   | revert changes from command if pulled from history


## Running Commands
* command1
  * run command1
* command1 && command2
  * runs if command1 succeeds
* command1 || command2
  * runs command2 if command1 fails
* command1; command2
  * run command1 then command2
* command1 | command2
  * run command1 and pipe output to command2


## Useful random things
```bash

find /[path] -name [filename]                                           #finds every file in path with the name
find /[path] -name [filename] -exec grep [condition] {};                #finds files that meet condition
find /[path] -name [filename] -exec grep -A [number] '^[condition]' {}' #finds lines in file that start with specific [condition] and will print [number] lines after where it is true
find /[path] -name [filename] 2>&1 | grep -v "Permission denied"        #will not print permission denied output, annoying to look at

cat [filename] | cut -d [delimiter] -f [field]                          #finds specific field based on delimiter
cat [filename] | cut -d [delimiter] -f [field] | grep -v [condition]    #finds field but then will filter out the condition

# for [filename], escape characters are legal
#     \*.c  will grab all c files, etc.

ls [path]/*.c  #list all c files 

```

<br/>

## Scripting
### Built-In
* #### Variables
  * Assignment DOES NOT need the $
    * NAME=value
  * Usage DOES need the $ or optional{}
    * echo $NAME
    * echo ${NAME}
  * Make the variable available to sub-processes
    * export NAME=value
  
#### If/Else

``` if [ condition ]; then ... ; fi ```
``` if [ condition ]; then ... ; else ... ; fi ```
  <br/>

##### Conditions

* Numerical Conditions
```bash
if [ a -eq b ]; then ...
if [ a -ne b ]; then ...
if [ a -lt b ]; then ...
if [ a -gt b ]; then ...
if [ a -le b ]; then ...
if [ a -ge b ]; then ...
```
* String Conditions
```bash
if [ condition ]
   && for and
   || for or
   == for equal
   != for not equal
```
<br/>

***Note: Remember spaces before and after condition***

<br/>
<br/>

#### Loops
```bash
for VAR in 1 2 3; do ... ; done


for VAR in 1 2 3
do
	...
done

while true; do ... ; done

while true
do
	...
done

```

#### Switch/Case


## Command Substitution
* Commands can be run in 'sub-shells'
* Output will be used in their place, like variables
* Two ways:
  * \`cmd\` (deprecated)
  * $(cmd)

### Examples
```bash

printf "Kernel Version: $(uname -v)\n\n"
printf "Number of users on the machine: $(cat /etc/passwd | wc -l)\n\n"
printf "   === Accounts === \n$(cut -d ':' -f 1 /etc/passwd)\n\n"
printf "\nRoot User has ran $(cat /root/.bash_history | wc -l) commands\n\n"

```

## Math
$((equation))

Character | Description
--------- | -----------
'='       | equals, assignment operator
'+'       | plus operator or option flag for certain commands (enable with plus,disable with '-')
'%'       | modulo operator
'-'       | minus in arithmetic operations
<code>*</code>       | multiplication operator
<code>**</code>      | exponential operator



```bash
SUM=$((10 + 20 + 30 + 40))
echo $SUM
```


















