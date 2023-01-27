# A PPA repository for packages I use

## Usage (general for all packages)
```bash
curl -SsL https://bochinche.github.io/ppa/bochinche_KEY.gpg | sudo apt-key add -
sudo curl -SsL -o /etc/apt/sources.list.d/bochinche_ppa.list https://bochinche.github.io/ppa/bochinche_list_file.list
sudo apt update
```

## Packages
### asterisk16 for raspbian on raspberrypi (bullseye)
This package is based on the work of the people at http://www.raspberry-asterisk.org. According to this [page](http://www.raspberry-asterisk.org/downloads/), the project's contributors will not be able to use the latest Pi 4 HW. 

The dependencies of the asterisk16 package have been modified to support the latest raspbian release. Specifically, **libcodec2-0.8.1** has been replaced with **libcodec2-0.9**.

If needed, this [page](https://www.dslreports.com/forum/r30661088-PBX-FreePBX-for-the-Raspberry-Pi) contains information on how to build the project yourself. 

The project's original repository can be found at http://repo.raspbx.org/apt/debian/pool/main/a/. 

To install the deb of the project, use the following command
```bash
sudo apt install asterisk11-sounds asterisk16 asterisk16-chandongle asterisk16-codecg729 
```
You will need to copy and edit the init file yourself. 

# Sources & Documentation / Links
- original asterisk project these packages are based on http://www.raspberry-asterisk.org
- [Documentation on how to create your own local debian repository](https://rpmdeb.com/devops-articles/how-to-create-local-debian-repository/)
- [How to extract a .deb file without opening it on Debian or Ubuntu Linux](https://www.cyberciti.biz/faq/how-to-extract-a-deb-file-without-opening-it-on-debian-or-ubuntu-linux/)
- [How to easily unpack DEB, edit postinst and repack DEB](https://unix.stackexchange.com/questions/138188/easily-unpack-deb-edit-postinst-and-repack-deb)
- [dpkg: clean versus remove](https://linuxprograms.wordpress.com/2010/05/12/dpkg-purge-versus-remove/)
- [Changing the dependencies of a deb package](https://coderwall.com/p/hes3ha/change-the-dependencies-of-a-deb-package)
- [How to let `dpkg -i` install dependencies for me](https://askubuntu.com/questions/40011/how-to-let-dpkg-i-install-dependencies-for-me)
- [How to create a tar.xz in one command](https://stackoverflow.com/questions/18855850/create-a-tar-xz-in-one-command)
- [Hosting your own PPA repository on GitHub](https://assafmo.github.io/2019/05/02/ppa-repo-hosted-on-github.html)