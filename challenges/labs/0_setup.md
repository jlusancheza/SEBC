
# Setup
##Cloud provider
```
AWS
```

##  List of instances
```
		Private IP			Private DNS			Public IP					Public DNS

Host 1	10.0.3.120	ip-10-0-3-120.ec2.internal	54.234.101.98	ec2-54-234-101-98.compute-1.amazonaws.com
Host 2	10.0.3.127	ip-10-0-3-127.ec2.internal	54.174.253.122	ec2-54-174-253-122.compute-1.amazonaws.com
Host 3	10.0.3.98	ip-10-0-3-98.ec2.internal	52.91.134.210	ec2-52-91-134-210.compute-1.amazonaws.com
Host 4	10.0.3.164	ip-10-0-3-164.ec2.internal	52.3.248.136	ec2-52-3-248-136.compute-1.amazonaws.com


```

## Linux Release 
```
sudo cat /etc/centos-release

CentOS release 6.9 (Final)
```

## System Capacity
```
[centos@ip-10-0-3-120 ~]$ sudo yum -y install epel-release
...
[centos@ip-10-0-3-120 ~]$ sudo yum -y install cloud-utils-growpart
...
[centos@ip-10-0-3-120 ~]$ df -h
Filesystem      Size  Used Avail Use% Mounted on
/dev/xvda1      7.8G  741M  6.7G  10% /
tmpfs            15G     0   15G   0% /dev/shm

[centos@ip-10-0-3-120 ~]$ sudo growpart /dev/xvda 1
CHANGED: partition=1 start=2048 old: size=16775168 end=16777216 new: size=167764747,end=167766795

[centos@ip-10-0-3-120 ~]$ df -h
Filesystem      Size  Used Avail Use% Mounted on
/dev/xvda1       79G  749M   74G   1% /
tmpfs            15G     0   15G   0% /dev/shm


```

## Execute yum repolist enabled
```
[centos@ip-10-0-3-120 ~]$ yum repolist enabled
Loaded plugins: fastestmirror, presto
Determining fastest mirrors
 * base: mirror.vcu.edu
 * epel: mirror.umd.edu
 * extras: linux.cc.lehigh.edu
 * updates: centos.mbni.med.umich.edu
repo id          repo name                                                status
base             CentOS-6 - Base                                           6,706
epel             Extra Packages for Enterprise Linux 6 - x86_64           12,461
extras           CentOS-6 - Extras                                            46
updates          CentOS-6 - Updates                                          826
repolist: 20,039

```

## Add Users
```

[centos@ip-10-0-3-120 ~]$ cat /etc/passwd | grep saturn
saturn:x:2800:2800::/home/saturn:/bin/bash
[centos@ip-10-0-3-120 ~]$ cat /etc/passwd | grep haley
haley:x:2900:2900::/home/haley:/bin/bash

[centos@ip-10-0-3-120 ~]$ cat /etc/group | grep comets
comets:x:2901:haley
[centos@ip-10-0-3-120 ~]$ cat /etc/group | grep planets
planets:x:2902:saturn

```

