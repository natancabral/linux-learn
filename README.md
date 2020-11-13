# Linux Learn

en: The Linux command line is a text interface to your computer. Often referred to as the shell, terminal, console, prompt or various other names, it can give the appearance of being complex and confusing to use. Yet the ability to copy and paste commands from a website, combined with the power and flexibility the command line offers.

This tutorial will teach you a little more about commands line on Linux.

pt: A linha de comando do Linux é uma interface de texto para o seu computador. Freqüentemente referido como shell, terminal, console, prompt ou vários outros nomes, pode dar a aparência de ser complexo e confuso de usar. Ainda assim, a capacidade de copiar e colar comandos de um site, combinada com o poder e flexibilidade que a linha de comando oferece.

Este tutorial vai te ensinar um pouco mais sobre linha de comando no Linux.

---

## Simples Commands

* en: Create folder
```bash
mkdir /tmp/tutorial
```
* en: Enter folder
```bash
cd /tmp/tutorial
```
* en: Back folder
```bash
cd .. # go back
cd / # go root drive
```
* en: List folder
```bash
ls
ls -a # show all hidden files
ls -la # show all hidden files on listing format
ls -ld .?* # show all hidden directory on listing format
# Explain:
# -a                show all files (ALL)
# -l                use a long listing format
# -d, --directory   list  directory entries instead of contents, and do not dereference /media/natancabral/FILES/developer/olic links
# .?*               will only state hidden files 
```
* en: Write output list
```bash
ls > output.txt
```
* en: Displayed Text on screen
```bash
echo "Hello Word"
```
* en: Writer Text in file
```bash
echo "Hello Word" > savefile.txt
```
* en: Add text on end file 
```bash
echo "Final Line" >> savefile.txt  
```
* en: Move file
```bash
mv myfile.txt dir1
ls dir1
```
* en: Move all files on "dir1" foder into "current" folder (single dot (.) can be used to represent the current working)
```bash
mv dir1/* .
```
* en: Copy Files
> font: https://www.linuxtechi.com/cp-command-examples-linux-beginners/
```bash
cp
cp /etc/passwd /mnt/backup/
cp /etc/passwd /etc/group /etc/shadow /mnt/backup/ # multiple copys file to /mnt/backup/
cp -i # interactively (show copy process)
cp -n # do not overwrite
```
* en: Copy Directory or Folder
```bash
cp -r 
cp -r /etc/passwd /mnt/backup/
cp -ir # interactively (show copy process)
cp -n # do not overwrite
```
* en: Move Files
```bash
mv
```
* en: Backup file
```bash
mv backup_combined.txt combined_backup.txt
mv "folder1" "folder1_back"
```
* en: Remove Files and Folders
```bash
rm file.ext
rm folder
rmdir folder* # delete folder1,folder2,folder_,folder... 
rmdir folder1/* # delete into folder1/
rm -r folder_name # very dangers (delete files and folders names)
```
* en: Show tree folder (install: $ sudo apt install tree)
```bash
tree
tree -a
```
* en: Creating Symbolic Link | Symlink
```bash
# ln -s <source_file_directory> <link_file_directory>
# -s stands for symbolic link (make symbolic links instead of hard links)
sudo ln -s /home/<username>/Downloads /Downloads
sudo ln -s /home/<username>/Downloads Downloads
sudo ln -s /media/<username>/<HD>/files/local/developer/ Dev
# remove Symlink
unlink <link>
rm <link>
unlink Dev
# --------------------------------------------
# To acess Symlink:
cd Dev
cd /Downloads
cd Downloads
```
* en: User access
```bash
sudo su -nameuserhere # to access your username
sudo su -- # root user
```
* en: Find in /Home (~/) size files > 1GB and list then
* pt: Busque por arquivos em /Home de tamanho maior que 1GB e liste
```bash
find ./ -name "*gnnc*" -type f # f files | d directories
find ~ -size +1G -ls
find ~ -maxdepth 2 -ls -name *.ini
find ./folder_name -maxdepth 1 -name *.php
find -maxdepth 3 -name "*.ini" -not -path ~ -ls
find -name "*.ini" -path ~ -ls
find -name "*.ini" ! -name "*config.*" -ls # AND ! not have
find -name "*.php" -o -name "*.js" -ls # -o OR have
find . –user maria # on user path
# -type f - only files
# -type d - only directories
# -ls - show list
# -maxdepth - max depth find 
# -name - have filename
# ! -name - not have filename
# -not -name - not have filename
# -o - OR
# -path - local path
# -user - nameuser
# font: https://e-tinet.com/linux/comando-find-linux/
```

## System Commands

* en: Displays all of your previous commands up to the history limit.
```bash
history
```
* en: Print Working Directory. Ubuntu command displays the full pathname 
```bash
pwd
```
* en: Display System storage
```bash
df
```
* en: Free space avaliable
```bash
free
```
* en: Display Process
```bash
top
```
* en: Change Password User
```bash
passwd <user>
```
* en: Knolege: WHAT IS (command)
```bash
whatis <command>
whatis cp
whatis su
whatis passwd
```
* en: Manual: MAN (command)
```bash
man <command>
man ls
man su
man ssh
```
* en: Where program was installed
```bash
which
which calendar
which nano
which gedit
```
* en: Used to examine or control the kernel ring buffer.
```bash
dmesg
```

## Advanced Commands

* [Install Package](install-package.md)
* [Update & Upgrade](update-and-upgrade.md)
* [Shotcut Terminal](create-personal-shotcut-terminal.md)

