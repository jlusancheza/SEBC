# Preinstall
## VM.Swappiness
```
[centos@ip-10-0-3-96 ~]$ sysctl vm.swappiness
vm.swappiness = 60
[centos@ip-10-0-3-96 ~]$ sudo sysctl vm.swappiness=1
vm.swappiness = 1


pdsh> sudo sysctl vm.swappiness
10.0.3.126: vm.swappiness = 60
10.0.3.144: vm.swappiness = 60
10.0.3.79: vm.swappiness = 60
pdsh> sudo sysctl vm.swappiness=1
10.0.3.144: vm.swappiness = 1
10.0.3.79: vm.swappiness = 1
10.0.3.126: vm.swappiness = 1

```

## Mount Atributtes
```
[centos@ip-10-0-3-96 ~]$ df -h
Filesystem      Size  Used Avail Use% Mounted on
/dev/xvda1       79G  794M   74G   2% /
tmpfs            15G     0   15G   0% /dev/shm
/dev/xvdb        79G  184M   75G   1% /vol1
/dev/xvdc        79G  184M   75G   1% /vol2

[centos@ip-10-0-3-96 ~]$ mount -l
/dev/xvda1 on / type ext4 (rw)
proc on /proc type proc (rw)
sysfs on /sys type sysfs (rw)
devpts on /dev/pts type devpts (rw,gid=5,mode=620)
tmpfs on /dev/shm type tmpfs (rw,rootcontext="system_u:object_r:tmpfs_t:s0")
none on /proc/sys/fs/binfmt_misc type binfmt_misc (rw)
/dev/xvdb on /vol1 type ext3 (rw)
/dev/xvdc on /vol2 type ext3 (rw)

pdsh> df -h
10.0.3.79: Filesystem      Size  Used Avail Use% Mounted on
10.0.3.79: /dev/xvda1       79G  749M   74G   1% /
10.0.3.79: tmpfs            15G     0   15G   0% /dev/shm
10.0.3.79: /dev/xvdb        79G  184M   75G   1% /vol1
10.0.3.79: /dev/xvdc        79G  184M   75G   1% /vol2
10.0.3.126: Filesystem      Size  Used Avail Use% Mounted on
10.0.3.126: /dev/xvda1       79G  749M   74G   1% /
10.0.3.126: tmpfs            15G     0   15G   0% /dev/shm
10.0.3.126: /dev/xvdb        79G  184M   75G   1% /vol1
10.0.3.126: /dev/xvdc        79G  184M   75G   1% /vol2
10.0.3.144: Filesystem      Size  Used Avail Use% Mounted on
10.0.3.144: /dev/xvda1       79G  749M   74G   1% /
10.0.3.144: tmpfs            15G     0   15G   0% /dev/shm
10.0.3.144: /dev/xvdb        79G  184M   75G   1% /vol1
10.0.3.144: /dev/xvdc        79G  184M   75G   1% /vol2

pdsh> mount -l
10.0.3.144: /dev/xvda1 on / type ext4 (rw)
10.0.3.144: proc on /proc type proc (rw)
10.0.3.144: sysfs on /sys type sysfs (rw)
10.0.3.144: devpts on /dev/pts type devpts (rw,gid=5,mode=620)
10.0.3.144: tmpfs on /dev/shm type tmpfs (rw,rootcontext="system_u:object_r:tmpfs_t:s0")
10.0.3.144: none on /proc/sys/fs/binfmt_misc type binfmt_misc (rw)
10.0.3.144: /dev/xvdb on /vol1 type ext3 (rw)
10.0.3.144: /dev/xvdc on /vol2 type ext3 (rw)
10.0.3.126: /dev/xvda1 on / type ext4 (rw)
10.0.3.126: proc on /proc type proc (rw)
10.0.3.126: sysfs on /sys type sysfs (rw)
10.0.3.126: devpts on /dev/pts type devpts (rw,gid=5,mode=620)
10.0.3.126: tmpfs on /dev/shm type tmpfs (rw,rootcontext="system_u:object_r:tmpfs_t:s0")
10.0.3.126: none on /proc/sys/fs/binfmt_misc type binfmt_misc (rw)
10.0.3.126: /dev/xvdb on /vol1 type ext3 (rw)
10.0.3.126: /dev/xvdc on /vol2 type ext3 (rw)
10.0.3.79: /dev/xvda1 on / type ext4 (rw)
10.0.3.79: proc on /proc type proc (rw)
10.0.3.79: sysfs on /sys type sysfs (rw)
10.0.3.79: devpts on /dev/pts type devpts (rw,gid=5,mode=620)
10.0.3.79: tmpfs on /dev/shm type tmpfs (rw,rootcontext="system_u:object_r:tmpfs_t:s0")
10.0.3.79: none on /proc/sys/fs/binfmt_misc type binfmt_misc (rw)
10.0.3.79: /dev/xvdb on /vol1 type ext3 (rw)
10.0.3.79: /dev/xvdc on /vol2 type ext3 (rw)

```

## Disable Transparent Hugepages
```
[root@ip-10-0-3-96 centos]# echo never > /sys/kernel/mm/redhat_transparent_hugepage/enabled
[root@ip-10-0-3-96 centos]# echo never > /sys/kernel/mm/transparent_hugepage/enabled

[root@ip-10-0-3-126 centos]# echo never > /sys/kernel/mm/redhat_transparent_hugepage/enabled
[root@ip-10-0-3-126 centos]# echo never > /sys/kernel/mm/transparent_hugepage/enabled

[root@ip-10-0-3-144 centos]# echo never > /sys/kernel/mm/redhat_transparent_hugepage/enabled
[root@ip-10-0-3-144 centos]# echo never > /sys/kernel/mm/transparent_hugepage/enabled

[root@ip-10-0-3-79 centos]# echo never > /sys/kernel/mm/redhat_transparent_hugepage/enabled
[root@ip-10-0-3-79 centos]# echo never > /sys/kernel/mm/transparent_hugepage/enabled

```

## List your network interface configuration
```
[centos@ip-10-0-3-96 ~]$ ifconfig
eth0      Link encap:Ethernet  HWaddr 06:91:36:AA:16:9A
          inet addr:10.0.3.96  Bcast:10.0.3.255  Mask:255.255.255.0
          inet6 addr: fe80::491:36ff:feaa:169a/64 Scope:Link
          UP BROADCAST RUNNING MULTICAST  MTU:9001  Metric:1
          RX packets:12182 errors:0 dropped:0 overruns:0 frame:0
          TX packets:5169 errors:0 dropped:0 overruns:0 carrier:0
          collisions:0 txqueuelen:1000
          RX bytes:12658653 (12.0 MiB)  TX bytes:745182 (727.7 KiB)
          Interrupt:123

lo        Link encap:Local Loopback
          inet addr:127.0.0.1  Mask:255.0.0.0
          inet6 addr: ::1/128 Scope:Host
          UP LOOPBACK RUNNING  MTU:65536  Metric:1
          RX packets:0 errors:0 dropped:0 overruns:0 frame:0
          TX packets:0 errors:0 dropped:0 overruns:0 carrier:0
          collisions:0 txqueuelen:0
          RX bytes:0 (0.0 b)  TX bytes:0 (0.0 b)

[centos@ip-10-0-3-126 ~]$ ifconfig
eth0      Link encap:Ethernet  HWaddr 06:1B:8B:FF:12:D4
          inet addr:10.0.3.126  Bcast:10.0.3.255  Mask:255.255.255.0
          inet6 addr: fe80::41b:8bff:feff:12d4/64 Scope:Link
          UP BROADCAST RUNNING MULTICAST  MTU:9001  Metric:1
          RX packets:6702 errors:0 dropped:0 overruns:0 frame:0
          TX packets:5740 errors:0 dropped:0 overruns:0 carrier:0
          collisions:0 txqueuelen:1000
          RX bytes:627956 (613.2 KiB)  TX bytes:827459 (808.0 KiB)
          Interrupt:123

lo        Link encap:Local Loopback
          inet addr:127.0.0.1  Mask:255.0.0.0
          inet6 addr: ::1/128 Scope:Host
          UP LOOPBACK RUNNING  MTU:65536  Metric:1
          RX packets:0 errors:0 dropped:0 overruns:0 frame:0
          TX packets:0 errors:0 dropped:0 overruns:0 carrier:0
          collisions:0 txqueuelen:0
          RX bytes:0 (0.0 b)  TX bytes:0 (0.0 b)


[centos@ip-10-0-3-144 ~]$ ifconfig
eth0      Link encap:Ethernet  HWaddr 06:67:75:4A:F4:54
          inet addr:10.0.3.144  Bcast:10.0.3.255  Mask:255.255.255.0
          inet6 addr: fe80::467:75ff:fe4a:f454/64 Scope:Link
          UP BROADCAST RUNNING MULTICAST  MTU:9001  Metric:1
          RX packets:1313 errors:0 dropped:0 overruns:0 frame:0
          TX packets:1381 errors:0 dropped:0 overruns:0 carrier:0
          collisions:0 txqueuelen:1000
          RX bytes:148823 (145.3 KiB)  TX bytes:265405 (259.1 KiB)
          Interrupt:123

lo        Link encap:Local Loopback
          inet addr:127.0.0.1  Mask:255.0.0.0
          inet6 addr: ::1/128 Scope:Host
          UP LOOPBACK RUNNING  MTU:65536  Metric:1
          RX packets:0 errors:0 dropped:0 overruns:0 frame:0
          TX packets:0 errors:0 dropped:0 overruns:0 carrier:0
          collisions:0 txqueuelen:0
          RX bytes:0 (0.0 b)  TX bytes:0 (0.0 b)

[centos@ip-10-0-3-79 ~]$ ifconfig
eth0      Link encap:Ethernet  HWaddr 06:73:6C:F2:14:F4
          inet addr:10.0.3.79  Bcast:10.0.3.255  Mask:255.255.255.0
          inet6 addr: fe80::473:6cff:fef2:14f4/64 Scope:Link
          UP BROADCAST RUNNING MULTICAST  MTU:9001  Metric:1
          RX packets:2213 errors:0 dropped:0 overruns:0 frame:0
          TX packets:2206 errors:0 dropped:0 overruns:0 carrier:0
          collisions:0 txqueuelen:1000
          RX bytes:231824 (226.3 KiB)  TX bytes:431595 (421.4 KiB)
          Interrupt:123

lo        Link encap:Local Loopback
          inet addr:127.0.0.1  Mask:255.0.0.0
          inet6 addr: ::1/128 Scope:Host
          UP LOOPBACK RUNNING  MTU:65536  Metric:1
          RX packets:0 errors:0 dropped:0 overruns:0 frame:0
          TX packets:0 errors:0 dropped:0 overruns:0 carrier:0
          collisions:0 txqueuelen:0
          RX bytes:0 (0.0 b)  TX bytes:0 (0.0 b)



```

## Show nslookup
```
[centos@ip-10-0-3-96 ~]$ nslookup 10.0.3.96
Server:         10.0.0.2
Address:        10.0.0.2#53

Non-authoritative answer:
96.3.0.10.in-addr.arpa  name = ip-10-0-3-96.ec2.internal.

[centos@ip-10-0-3-96 ~]$ nslookup ip-10-0-3-96.ec2.internal
Server:         10.0.0.2
Address:        10.0.0.2#53

Non-authoritative answer:
Name:   ip-10-0-3-96.ec2.internal
Address: 10.0.3.96

[centos@ip-10-0-3-96 ~]$ nslookup 10.0.3.126
Server:         10.0.0.2
Address:        10.0.0.2#53

Non-authoritative answer:
126.3.0.10.in-addr.arpa name = ip-10-0-3-126.ec2.internal.

Authoritative answers can be found from:

[centos@ip-10-0-3-96 ~]$ nslookup  ip-10-0-3-126.ec2.internal.
Server:         10.0.0.2
Address:        10.0.0.2#53

Non-authoritative answer:
Name:   ip-10-0-3-126.ec2.internal
Address: 10.0.3.126

[centos@ip-10-0-3-96 ~]$ nslookup 10.0.3.144
Server:         10.0.0.2
Address:        10.0.0.2#53

Non-authoritative answer:
144.3.0.10.in-addr.arpa name = ip-10-0-3-144.ec2.internal.

Authoritative answers can be found from:

[centos@ip-10-0-3-96 ~]$ nslookup  ip-10-0-3-144.ec2.internal
Server:         10.0.0.2
Address:        10.0.0.2#53

Non-authoritative answer:
Name:   ip-10-0-3-144.ec2.internal
Address: 10.0.3.144

[centos@ip-10-0-3-96 ~]$ nslookup 10.0.3.79
Server:         10.0.0.2
Address:        10.0.0.2#53

Non-authoritative answer:
79.3.0.10.in-addr.arpa  name = ip-10-0-3-79.ec2.internal.

Authoritative answers can be found from:

[centos@ip-10-0-3-96 ~]$ nslookup  ip-10-0-3-79.ec2.internal
Server:         10.0.0.2
Address:        10.0.0.2#53

Non-authoritative answer:
Name:   ip-10-0-3-79.ec2.internal
Address: 10.0.3.79


```

## Show ntpd y nscd running

```

[centos@ip-10-0-3-96 ~]$ sudo service ntpd status
ntpd (pid  7317) is running...
[centos@ip-10-0-3-96 ~]$ sudo service nscd status
nscd (pid 7231) is running...

pdsh> sudo service ntpd status
10.0.3.126: ntpd (pid  2058) is running...
10.0.3.144: ntpd (pid  5577) is running...
10.0.3.79: ntpd (pid  5624) is running...
pdsh> sudo service nscd status
10.0.3.79: nscd (pid 5651) is running...
10.0.3.126: nscd (pid 2085) is running...
10.0.3.144: nscd (pid 5604) is running...



```