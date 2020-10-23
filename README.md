# Linux Learn

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
```
