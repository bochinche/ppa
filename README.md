A PPA repository for my packages:

- asterisk16 for rpi with raspbian 

# Usage

```bash
curl -SsL https://assafmo.github.io/ppa/ubuntu/KEY.gpg | sudo apt-key add -
sudo curl -SsL -o /etc/apt/sources.list.d/assafmo.list https://assafmo.github.io/ppa/ubuntu/assafmo.list
sudo apt update
sudo apt install joincap xioc sqlitequeryserver
```

# Sources

- http://www.raspberry-asterisk.org
- 
