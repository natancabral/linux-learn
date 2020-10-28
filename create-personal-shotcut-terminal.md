## Create Personal Shotcut Terminal

#### Edit File

The shortcuts for commands are known as aliases. 

* en: Open file on text editor:
```bash
gedit ~/.bashrc 
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

### Username Grenn
#### My username in the terminal usually green.

en: Basically you change ~/.bashrc file for setting the prompt color, append lines code bellow:
en: Open file in terminal *** $ gedit ~/.bashrc *** or *** $ <text_editor> ~/.bashrc ***

```bash
# uncomment for a colored prompt, if the terminal has the capability; turned
# off by default to not distract the user: the focus in a terminal window
# should be on the output of commands, not on the prompt
force_color_prompt=yes

if [ -n "$force_color_prompt" ]; then
    if [ -x /usr/bin/tput ] && tput setaf 1 >&/dev/null; then
        # We have color support; assume it's compliant with Ecma-48
        # (ISO/IEC-6429). (Lack of such support is extremely rare, and such
        # a case would tend to support setf rather than setaf.)
        color_prompt=yes
    else
        color_prompt=
    fi
fi

if [ "$color_prompt" = yes ]; then
    PS1='${debian_chroot:+($debian_chroot)}\[\033[01;32m\]\u@\h\[\033[00m\]:\[\033[01;34m\]\w \$\[\033[00m\] '
else
    PS1='${debian_chroot:+($debian_chroot)}\u@\h:\w\$ '
fi
unset color_prompt force_color_prompt
```
