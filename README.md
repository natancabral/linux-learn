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
* en: List folder
```bash
ls
ls -a (show all hidden files)
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
* en: User access
```bash
sudo su -- # root user
sudo su -nameuserhere # to access your username
```
* en: Find in /Home size files > 1GB and list then
* pt: Busque por arquivos em /Home de tamanho maior que 1GB e liste
```bash
find ~ -size +1G -ls
```

## Advanced commands

* [Install Package](install-package.md)
* [Update & Upgrade](update-and-upgrade.md)
* [Shotcut Terminal](create-personal-shotcut-terminal.md)

