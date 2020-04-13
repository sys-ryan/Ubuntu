# Ubuntu TFTP 

### 설치 
```
sudo apt-get install tftp tftpd xinetd 
````

### 설정 파일 
```
sudo vi /etc/xinetd.d/tftp 
```

```
service tftp
{
  socket_type = dgram
  protocol = udp
  wait = yes
  user = root
  server = /usr/sbin/in.tftpd
  server_args = -s /tftpboot
  disable = no
  per_source = 11
  cps = 100 2
  flags = IPv4
}

### TFTP 디렉터리 설정 
```
sudo mkdir /tftpdir
sudo chmod 777 /tftpdir
```

### 정상 동작 테스트 
```
$ cd /tftpdir
$ vi test 
$ tftp localhost 
tftp> get test
received ?? bytes in ?? seconds
tftp>quit
$ cat test
test의 내용
```

