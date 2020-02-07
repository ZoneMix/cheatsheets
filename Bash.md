---
title: Bash
created: '2020-02-07T04:41:46.455Z'
modified: '2020-02-07T07:17:07.127Z'
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
<details open>
<summary>Details</summary>
<markdown>
| Command                   | Description 
| -------                   | -----------
| pwd                       | Prints current path 
| ls                        | Lists directory contents 
| cd                        | Changes directory 
| cat [file]                | Prints contents of [file] 
| cp [file] [file]          | Copy  ***works with directories*** 
| mv [file] [file]          | Move ***works with directories*** 
| rm [file]                 | Remove ***-r to remove directory*** 
| mkdir [dirname]           | Makes new directory 
| rmdir [dirname]           | Removes directory ***-r for directory with contents*** 
| touch [filename]          | Creates new file 
| ln [source] [destination] | Creates a shortcut 
| su [user]                 | Switch user   
| sudo [command]            | Run with root privileges 
| logout or exit            | Logout or exit shell 
| head [filename]           | Prints first 10 lines of file by default 
| tail [filename]           | Prints last 10 lines of file by default 
| chmod                     | Can change permissions in filesystem ***see options with man chmod***
| who                       | Shows users logged on 
| md5sum [filename]         | Prints the md5 hash of a file 
| find [path] [expression]  | Search for files matching a provided pattern 
| df                        | Display used and available disk space 
| free                      | Display amount of free and used memory in the system 
| du                        | Show how much space each file uses 
| ip addr or ifconfig       | Show ip address on system 
| uname                     | Print system information 
| history                   | Prints .[shell]_history for the user 
| man [command]             | Shows the manual for a command 
| shutdown                  | Shuts the system down 
| reboot                    | Reboot the system 
| clear                     | Clear the current buffer of the screen 
| less                      | Will show contents of large file, but will not print everything at once 
| more                      | Opposite of less, does the same thing pretty much, <br/>less features than ***less*** *isn't that ironic* 
| nano or vim               | Text editors within the CLI ****do not ever use vi, <br/>please use vim, you will hate it***
| date                      | Print or set system date and time  
| passwd                    | Change user password 
</markdown>
</details>

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
```

### Directories
```
- '.' is current directory
-  '..' is previous directory
```

### Keyboard Shorcuts

<details close>
  <summary>CTRL+ Commands</summary>
  <markdown>
* C (kill)
* L (clear screen)
* D (logout)
* Z (suspend current foreground process)
  * return using fg 'process number'
* S (stop output to screen)
* Q (resume output)
* A or Home (go beginning of line)
* E or End (go end of line)
* B (go back one character)
* F (go forward one character)
* K (cuts everything forward of cursor to clipboard)
* XX (move between beginning of line and the current positions)
* D (delete charcter under cursor)
* U (delete everything behind cursor)
* Y (paste last thing yanked)
* _ (undo last key press)
* W (cut word before cursor)
* P (prev command)
* N (next command)
* R (recall last command with characters provided)
* O (Run command you found with R)
* G (leave R)
  </markdown>
</details>

<details close>
  <summary>ALT+ Commands</summary>
  <markdown>
* B (back one word)
* F (forward one word)
* D (delete word after cursor)
* H (delete charcter before cursor)
* T (swap current word with prev word)
* U (capitalize word after cursor)
* L (lowercase word after cursor)
* C (capitalize character on cursor)
* R (revert changes from command if pulled from history)
  </markdown>
</details>

***
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
  
* #### If/Else
  * if [condition]; then ... ; fi
  * if [condition]; then ... ; else ... ; fi
  <br/>
  * **Conditions**
    * if [ a -eq b]; then ...
    * if [ a -ne b]; then ...
    * if [ a -lt b]; then ...
    * if [ a -gt b]; then ...
    * if [ a -le b]; then ...
    * if [ a -ge b]; then ...
<br/>
* #### Loops
 * 
* #### Command Substitution


















