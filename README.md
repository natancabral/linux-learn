# Linux Learn

The Linux command line is a text interface to your computer. Often referred to as the shell, terminal, console, prompt or various other names, it can give the appearance of being complex and confusing to use. Yet the ability to copy and paste commands from a website, combined with the power and flexibility the command line offers.

This tutorial will teach you a little more about commands line on Linux.

## Finder

* en: Find in /Home size files > 1GB and list then
* pt: Busque por arquivos em /Home de tamanho maior que 1GB e liste

> Ubuntu
```
find ~ -size +1G -ls
```
---

## Simples Commands

* en: Create folder
```
mkdir /tmp/tutorial
```
* en: Enter folder
```
cd /tmp/tutorial
```
* en: Remove folder
```
rm /tmp/tutorial
```
* en: List folder
```
ls
ls -a (show all hidden files)
```
* en: Write output list
```
ls > output.txt
```
* en: Displayed Text on screen
```
echo "Hello Word"
```
* en: Writer Text in file
```
echo "Hello Word" > savefile.txt
```
* en: Move file
```
mv myfile.txt dir1
ls dir1
```
* en: Move all files on "dir1" foder into "current" folder (single dot (.) can be used to represent the current working)
```
mv dir1/* .
```
en: Backup file
```
mv backup_combined.txt combined_backup.txt
mv "folder1" "folder1_back"
```
en: Remove Files and Folders
```
rm file.ext
rm folder
rmdir folder* # delete folder1,folder2,folder_,folder... 
rmdir folder1/* # delete into folder1/
rm -r folder_name # very dangers (delete files and folders names)
```
en: Show tree folder (install: $ sudo apt install tree)
```
tree
tree -a
```
en: User access
```
sudo su -- # root user
sudo su -nameuserhere # to access your username
```
