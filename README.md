# Raspberry Pi projects
Raspbian is based on Debian OS.
```
$ lsb_release -a
```

## Preparing OS

1. Create the removable disk has OS files
```
Manage disk parricions
$ sudo fdisk /dev/<removable disk name>

Copy OS files to removable disk
$ dd if=<OS file name>.img of=/dev/<removable disk name>
```

2. Enable SSH
Create empty ssh file at root direction of boot.

3. Setting Wi-Fi
```
$ cat usr/src/kernel/Documentation/networking/mac80211_hwsim/wpa_supplicant.conf 

ctrl_interface=/var/run/wpa_supplicant

network={
	ssid="mac80211 test"
	psk="12345678"
	key_mgmt=WPA-PSK
	proto=WPA2
	pairwise=CCMP
	group=CCMP
}
```

## Operation commands

```
$ ifconfig
Nmap scan report for <IP address>
Host is up (0.0057s latency).
Not shown: 998 closed ports
PORT   STATE SERVICE
22/tcp open  ssh
80/tcp open  http

$ ssh pi@<IP address>
$ ssh pi@raspberrypi.local

$ groups <user name>
$ cat /etc/passwd

$ nginx -t
```

## Network
Used DDNS (Dynamic DNS).


## Tools

### Nginx
An HTTP and reverse proxy server.

#### Dependencies
- nginx

#### Usage
Start the server with:
```
$ sudo /etc/init.d/nginx start
$ sudo service nginx start
```

Stop the server with:
```
$ sudo /etc/init.d/nginx stop
```

### Nagios
A monitor of networks and infrastructure.

#### Dependencies
- nagios3
- nagios-nrpe-plugin
- nagios-nrpe-server

### Usage
```
$ systemctl restart nagios3.service
```


### Docker
Install https://docs.docker.com/install/linux/docker-ce/debian/#install-using-the-repository


### Required
- Nginx
- Nagios
- Docker

### Refs
- https://olivertappin.com/command-line-tools/installing-nagios-nginx-php-fpm-nagiosgraph-ubuntu-16-04/
