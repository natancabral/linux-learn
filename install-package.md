## Install Package File

```
sudo dpkg ~/Downloads/filename.deb
sudo dpkg /home/<username>Downloads/filename.deb
sudo dpkg -i <file.deb> # -i --info
```

## APT or APT-GET

#### Refresh List
* pt: Para atualizar os repositórios de software, use o seguinte comando:
> $ sudo apt update
#### Install && Upgrade
> $ sudo apt install <package_name>
* pt: Para atualizar seus pacotes já instalados (softwares):
> * $ sudo apt upgrade
> * $ sudo apt dist-upgrade
> * $ sudo apt full-upgrade
#### Find
* pt: Para procurar um pacote a ser instalado, use o apt-cache ou apt search, assim:
> $ sudo apt search <word>
#### Remove
* > $ sudo apt list
* > $ sudo apt remove <package_name>
* pt: Ao remover software do seu sistema usando o comando apt-get remove, o Apt faz todo o trabalho de remoção de dependências não utilizados.
Algumas dependências podem permanecer no seu sistema. Se você ficar incomodado com isso, poderá então remover os pacotes que não estão sendo mais utilizados pelo Apt, é só utilizar a opção autoremove conforme abaixo:
> $ sudo apt autoremove

## SNAP

#### Refresh List
> Snaps update automatically, and by default, the snapd daemon checks for updates 4 times a day. Each update check is called a refresh
#### Install && Upgrade
> $ sudo snap install <package_name>
> $ sudo snap refresh <package_name> # upgrade
#### Find
> $ snap find <word>
> $ snap find | grep <word>
#### Remove
> $ snap list
> $ sudo snap remove <package_name>

## YUM, DEB, ETC

https://e-tinet.com/linux/7-gerenciadores-de-pacotes-linux/
