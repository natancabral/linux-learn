## Shotcut Terminal

#### Edit File

The shortcuts for commands are known as aliases. 

* en: Open file on text editor:
```
grdit ~/.bashrc 
# or
nano ~/.bashrc
```
> Maybe file: ~/.bash_aliases

* en: Append text on opened file. The syntax to create an alias is: 
```bash
alias <ALIAS_NAME>='<COMMAND_BASH>'  
```
---

#### Samples

* en: Access another HD/DRIVE 
```bash
alias link_mydrive='cd /media/<USER_NAME>/<DRIVER>/'  
```
* en: Echo 
```bash
alias link_myname='echo "My Name Is"'  
```
* en: SSH Access
```bash
alias user='ssh user@123.45.7.123'
```
* en: Ubuntu Version
```bash
alias ubuntu_version='lsb_release -a'
```

#### Testing Alias (shotcut)

Open new Terminal (Cntl+Alt+T) and typping yout ALIAS below:
```bash
$ ubuntu_version
```
