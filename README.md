# Course: Introduction to Terminal and Command Line

Within this README you will find a list of basic and useful commands that work in a Bash Shell.

# Sections
>[Path descriptors](#path-descriptors)\
>[Keyboard shortcuts](#keyboard-shortcuts)\
>[Operations with directories](#operations-with-directories)\
>["ls" Operations](#ls-operations)\
>[File manipulation and directories](#file-manipulation-and-directories)\
>[Text files manipulation](#text-files-manipulation)\
>[Command exploration and help](#command-exploration-and-help)\
>[Classes inside Wildcards](#classes-inside-wildcards)\
>[I/O redirects and control operators](#i/o-redirects-and-control-operators)
>[Permissions and users](#permissions-and-users)\
>[Environment variables](#environment-variables)\
>[Search commands](#search-commands)\
>[Network utilities](#network-utilities)\
>[File compression and decompression](#file-compression-and-decompression)

## Path descriptors
```bash
/     # System's root path
.     # Current directory
..    # Previous directory
~     # User's home dir
```

## Keyboard Shortcuts
```bash
CTRL-C     # Quits a command's process
CTRL-D     # Quits a command's input
CTRL-A     # Brings cursor to beginning of line
CTRL-E     # Brings cursor to end of line
CTRL-L     # Clears terminal
```

## Operations with directories
```bash
pwd            # Prints current dir
mkdir dir1     # Creates a dir named 'dir1'
cd dir1        # Switches dir to 'dir1'
cd ../..       # Goes 2 dirs backwards
ls             # Shows files and directories
tree /route    # Displays dirs and files nested at all levels in a '/route'
tree -L 2      # Same as previous but within 2 levels
```

## "ls" Operations
```bash
-a     # Shows everything (including hidden files and folders)
-R     # Shows a list in a recursive way
-r     # Shows a list in a reverse way
-t     # Shows latest modified
-S     # Shows a list ordered by Size
-l     # Shows as a list format with extended description
```

## File manipulation and directories
```bash
touch newFile         # Creates a file named 'newFile'
file my_file          # Displays 
cp file1 /destiny     # Copies 'file1' to a '/destiny'
cp -r dir1 dir1_cp    # Copies 'dir1' and its content to a copy 'dir1_cp'
mv file1 /destiny     # Moves 'file1' to a '/destiny'
mv file1 ok_file      # Renames 'file1' to 'ok_file'
rm file1              # Removes file1
rm -ri dir1           # Removes 'dir1' content in an interactive way
rm - r dir1           # Removes 'dir1' and its content in a recursive way
ln -s file link_name  # Creates a symbolic link with name 'link_name' to a 'file'
open filename         # Opens file with default program (MacOS)
xdg-open filename     # Opens file with default program (Linux)
```

## Text files manipulation
```bash
head file.txt        # Shows the first 10 lines in 'file.txt'
head -n 20 file.txt  # Shows the first 20 lines
tail file.txt        # Shows the last 10 lines in 'file.txt'
tail -n 20 file.txt  # Shows the last 20 lines
less file.txt        # Explores the file content with Pager
cat file1 file2      # Appends the content of 'file1' and 'file2' and displays it 
```

## Command exploration and help
```bash
man command               # Displays manual for a command
help command              # Displays help for a command
which command             # Shows the Dir that stores the command executable
alias aliasname="command" # Creates an 'aliasname' for a specified command
alias l="ls -la"          # Creates an alias 'l' for the command 'ls -la'
```

## Classes inside Wildcards
```bash
# Wildcards
*              # Matches any character
?              # Matches any individual character
[characters]   # Matches any character included in []
[!characters]  # Matches any character NOT included in []
[[:class:]]    # Matches any character in the 'class'
[:alnum:]      # Alphanumeric chars
[:alpha:]      # Alphabet chars
[:digit:]      # Matches any digit number
[:lower:]      # Matches any lower case letter
[:upper:]      # Matches any upper case letter
```

## I/O redirects and control operators
```bash
command < file        # Redirects input from command to a file
command > file        # Redirects output of a command to a file (use with caution, it overwrites system)
command >> file       # Appends the output of a command to a file. If it doesn't exist, it creates it.
command 2> error.txt  # Redirects the error output of a command to a file 'error.txt'
command1 | comand2    # Redirects the output of command1 to the input of command2
command1 ; command2   # Consecutive execution
command1 & command2   # Asynchronous execution
command1 && command2  # Executes command2 if and only if command1 is executed
command1 || command2  # Executes command1 or command2, which ever is posible.
```

## Permissions and users
- Owner
- Group
- World

read | write | execute

#### Symbolic
* u: User
* g: Group
* o: Others
* a: All

```bash
chmod 755 myFile         # Changes permissions for 'myFile'
chmod u-r myFile         # Removes user read permission for 'myFile'
chmod u=rwx,go=r myFile  # Gives rwx permissions to user, and r to group and others
id                       # Shows user id
whoami                   # Displays logged in username
su username              # Switches user to 'username'
sudo command             # Executes command as superuser
```

## Environment variables
```bash
env              # Prints current env variables
echo $VAR        # Prints the env variable 'VAR'
$PATH            # Variable that stores the routes of the executables
$HOME            # Variable that stores the user home dir
export $VAR=val  # Assigns variable '$VAR' with the value 'val' 
```

## Search commands
```bash
find <route> -name <name>  # Finds a 'name' file in 'route'
find . -name agenda        # Finds the fie named 'agenda' within current dir
grep <regex> file          # Finds with regular expression within a file or terminal output
grep -i hello message.txt  # Finds the word 'hello' in the file 'message.txt'
```

## Network utilities
```bash
ifconfig        # Displays network information
ping ip_domain  # Attemps to ping an 'ip_domain' to check availability
curl ip_domain  # Consults a resource/domain and displays it in terminal
wget ip_domain  # Downloads a resouce (could be by domain or IP)
traceroute ip_domain # Displays all the traveled route to reach a certain domain
netstat -i      # Displays the network interfaces and their status
 ```

## File compression and decompression
```bash
tar -czvf my_files.tar.gz Documents  # Compress a resource named 'my_files.tar.gz' to 'Documents'
tar -xzvf my_files.tar.gz <dir>      # Decompresses a resource named 'my_files.tar.gz' to a 'dir' 
```

### Elaborated by
[Eduardo Benitez](https://github.com/EduardoBtz)
