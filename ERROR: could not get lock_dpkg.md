### ERROR: apt-get install

<img src="./img/dpkg_err.png" title="dpkg_err"></img

해결 방법
```
sudo killall apt apt-get

sudo rm /var/lib/apt/lists/lock
sudo rm /var/cache/apt/archives/lock
sudo rm /var/lib/dpkg/lock*

sudo dpkg --configure -a

sudo apt update
```
