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



