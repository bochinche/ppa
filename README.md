# A PPA repository for packages used by me

## Usage (General for all packages)
```bash
curl -SsL https://bochinche.github.io/ppa/bochinche_KEY.gpg | sudo apt-key add -
sudo curl -SsL -o /etc/apt/sources.list.d/bochinche_ppa.list https://bochinche.github.io/ppa/bochinche_list_file.list
sudo apt update
```

## Packages
### asterisk16 for raspbian on raspberrypi (bullseye)
This package is based on the works done by the people at http://www.raspberry-asterisk.org. According to this [page](http://www.raspberry-asterisk.org/downloads/), the project's contributors will not be able the latest Pi 4 HW. 

The asterisk16 package dependecie's have been edited in order to support the lastest raspbian edition. Specifically **libcodec2-0.8.1** has been replaced by **libcodec2-0.9**.

In case needed, this [site](https://www.dslreports.com/forum/r30661088-PBX-FreePBX-for-the-Raspberry-Pi) contains the information on how to build the project on your own. 

The projects original repository can be found at http://repo.raspbx.org/apt/debian/pool/main/a/ 

To install the project's deb, use the following command
```bash
sudo apt install asterisk11-sounds asterisk16 asterisk16-chandongle asterisk16-codecg729 
```
You will still need to copy and edit the init file by yourself. 

# Sources & Documentation

- original asterisk project on which these packages are based on http://www.raspberry-asterisk.org
- documentation on how to create you own local debian repository https://rpmdeb.com/devops-articles/how-to-create-local-debian-repository/
- [How to extract a .deb file without opening it on Debian or Ubuntu Linux](https://www.cyberciti.biz/faq/how-to-extract-a-deb-file-without-opening-it-on-debian-or-ubuntu-linux/)
- [Easily unpack DEB, edit postinst, and repack DEB](https://unix.stackexchange.com/questions/138188/easily-unpack-deb-edit-postinst-and-repack-deb)
- [dpkg: purge versus remove](https://linuxprograms.wordpress.com/2010/05/12/dpkg-purge-versus-remove/)
- [Change the dependencies of a deb package](https://coderwall.com/p/hes3ha/change-the-dependencies-of-a-deb-package)
- [How to let `dpkg -i` install dependencies for me?](https://askubuntu.com/questions/40011/how-to-let-dpkg-i-install-dependencies-for-me)
- [Create a tar.xz in one command](https://stackoverflow.com/questions/18855850/create-a-tar-xz-in-one-command)
- [Hosting your own PPA repository on GitHub](https://assafmo.github.io/2019/05/02/ppa-repo-hosted-on-github.html)
