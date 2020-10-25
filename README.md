# Linux Learn

en: The Linux command line is a text interface to your computer. Often referred to as the shell, terminal, console, prompt or various other names, it can give the appearance of being complex and confusing to use. Yet the ability to copy and paste commands from a website, combined with the power and flexibility the command line offers.

This tutorial will teach you a little more about commands line on Linux.

pt: A linha de comando do Linux é uma interface de texto para o seu computador. Freqüentemente referido como shell, terminal, console, prompt ou vários outros nomes, pode dar a aparência de ser complexo e confuso de usar. Ainda assim, a capacidade de copiar e colar comandos de um site, combinada com o poder e flexibilidade que a linha de comando oferece.

Este tutorial vai te ensinar um pouco mais sobre linha de comando no Linux.

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

---

## Finder

* en: Find in /Home size files > 1GB and list then
* pt: Busque por arquivos em /Home de tamanho maior que 1GB e liste

> Ubuntu
```
find ~ -size +1G -ls
```

## Update & Upgrade

**apt update**
* en: To install the latest versions of all the previously installed packages on your system, apt-get upgrade is used. This command only upgrades the packages which have a new release available as stated in the sources.list file in the “/etc/apt” folder. It does not attempt to install a new package or remove any installed package on its own. http://linux.die.net/man/8/apt-get
* pt: Baixa as listas de pacotes dos repositórios e as "atualiza" para obter informações sobre as versões mais recentes dos pacotes e suas dependências. Isso será feito para todos os repositórios e PPAs. Usado para sincronizar novamente os arquivos de índice de pacotes de suas fontes. Os índices dos pacotes disponíveis são buscados no (s) local (is) especificado (s) em /etc/apt/sources.list(5). Uma atualização sempre deve ser realizada antes de uma atualização ou dist-upgrade.
```
sudo apt update
```
**apt upgrade**
* en: To upgrade or install the latest versions, run the following command as sudo as an only privilege user can check for and install updates on the Linux system.
* pt: Buscará novas versões de pacotes existentes na máquina se o APT souber dessas novas versões por meio de apt-get update. 
```
sudo apt --fix-broken install --yes
sudo apt list --upgradable
sudo apt upgrade
```
**apt upgrade <PACKAGE>**
* en: To upgrade a specific package, command is as follows:
* pt: Para atualizar pacotes específicos:
```
sudo apt-get upgrade <package_name>
```
#### upgrade, dist-upgrade, full-upgrade

* upgrade

>  upgrade is used to install the newest versions of all packages
   currently installed on the system from the sources enumerated in
   /etc/apt/sources.list. Packages currently installed with new
   versions available are retrieved and upgraded; under no
   circumstances are currently installed packages removed, or packages
   not already installed retrieved and installed. New versions of
   currently installed packages that cannot be upgraded without
   changing the install status of another package will be left at
   their current version. An update must be performed first so that
   apt-get knows that new versions of packages are available.

* dist-upgrade

>  dist-upgrade in addition to performing the function of upgrade,
   also intelligently handles changing dependencies with new versions
   of packages; apt-get has a "smart" conflict resolution system, and
   it will attempt to upgrade the most important packages at the
   expense of less important ones if necessary. So, dist-upgrade
   command may remove some packages. The /etc/apt/sources.list file
   contains a list of locations from which to retrieve desired package
   files. See also apt_preferences(5) for a mechanism for overriding
   the general settings for individual packages.

***And with the newer apt tool available from 14.04 onwards:***

> full-upgrade
   full-upgrade performs the function of upgrade but may also remove
   installed packages if that is required in order to resolve a
   package conflict.



