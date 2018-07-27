# Linux system how to store our passwd

As we all know ,the passwd files always store on the /etc/passwd or /etc/shadows. In the /etc/passwd ,always store the name of user ,group,privilege and so on. In below ,the sentence show the lines of a '/etc/passwd'.


```
daemon:x:1:1:daemon:/usr/sbin:/usr/sbin/nologin
bin:x:2:2:bin:/bin:/usr/sbin/nologin
```

## CTF chanllenge demo

In the Privilge Escalation ctf chanllenges, a universal method is to use the SUID flag to abuse some command tools. If you found a command has a SUID flag, you could handle it to change some configurations of the linux system.Eg, getcwd()/mksquanfs, One way is to rewrite the '/etc/passwd' file ,but you have to build your own passwd file .

you could use some tools in below :


## method 1: openssl 

USAGE: openssl passwd [option] passwd

eg: 
[root@localhost ~]$ openssl passwd -1 -salt '12345678'   # 12345678 not a target string we wanna crypto, just the length of string

-1 stand for md5 

-2 ,-3 .... stand for other cryto algorithm


## method2 :grub-crypt --sha-512


[root@localhost ~]grub-crypt --sha-512


how to install grub-crypt 

link: https://github.com/voidint/dockerfile/tree/master/grub-crypt

using docker to build the grub-crypt

## write your own key generate python

[references](http://blog.51cto.com/axe999/1386832)



[Not End]