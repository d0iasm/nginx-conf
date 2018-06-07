# Raspberry Pi projects
```
$ lsb_release -a
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
```


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


### Refs
- https://olivertappin.com/command-line-tools/installing-nagios-nginx-php-fpm-nagiosgraph-ubuntu-16-04/
