![](../Images/Pasted%20image%2020230419174738.png)

Lets login to ssh first 

```ruby
> ssh quantumleaper@147.182.204.122
The authenticity of host '147.182.204.122 (147.182.204.122)' can't be established.
ECDSA key fingerprint is SHA256:P8ofSM/2+aKpqhRZF6qJCxhq8en7u9kS+nTWadp1LZE.
Are you sure you want to continue connecting (yes/no/[fingerprint])? yes
Warning: Permanently added '147.182.204.122' (ECDSA) to the list of known hosts.
quantumleaper@147.182.204.122's password:
Welcome to Ubuntu 22.10 (GNU/Linux 5.19.0-23-generic x86_64)

 * Documentation:  https://help.ubuntu.com
 * Management:     https://landscape.canonical.com
 * Support:        https://ubuntu.com/advantage

  System information as of Wed Apr 19 16:48:23 UTC 2023

  System load:  0.0                Users logged in:       0
  Usage of /:   10.6% of 24.06GB   IPv4 address for eth0: 147.182.204.122
  Memory usage: 19%                IPv4 address for eth0: 10.48.0.5
  Swap usage:   0%                 IPv4 address for eth1: 192.168.25.2
  Processes:    91

0 updates can be applied immediately.


The list of available updates is more than a week old.
To check for new updates run: sudo apt update

Last login: Mon Apr 17 17:18:56 2023 from 68.40.169.30
quantumleaper@using-the-map-1:~$
```

Now, lets look for other hosts on the local network

```ruby
> quantumleaper@using-the-map-1:~$ nmap 192.168.25.0/28 -T5 -sV
Starting Nmap 7.92 ( https://nmap.org ) at 2023-04-19 16:50 UTC
Nmap scan report for 192.168.25.2
Host is up (0.000069s latency).
Not shown: 999 closed tcp ports (conn-refused)
PORT   STATE SERVICE VERSION
22/tcp open  ssh     OpenSSH 9.0p1 Ubuntu 1ubuntu7 (Ubuntu Linux; protocol 2.0)
Service Info: OS: Linux; CPE: cpe:/o:linux:linux_kernel

Nmap scan report for 192.168.25.3
Host is up (0.018s latency).
Not shown: 998 closed tcp ports (conn-refused)
PORT    STATE SERVICE VERSION
22/tcp  open  ssh     OpenSSH 7.4 (protocol 2.0)
111/tcp open  rpcbind 2-4 (RPC #100000)

Service detection performed. Please report any incorrect results at https://nmap.org/submit/ .
Nmap done: 16 IP addresses (2 hosts up) scanned in 19.10 seconds
quantumleaper@using-the-map-1:~$
```

```ruby
FLAG : jctf{#100000}
```
