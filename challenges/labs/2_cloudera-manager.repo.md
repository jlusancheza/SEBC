# list etc/yum.repos.d
 
```
[centos@ip-10-0-3-35 ~]$ ls /etc/yum.repos.d/
CentOS-Base.repo       CentOS-Media.repo   cloudera-manager.repo
CentOS-Debuginfo.repo  CentOS-Vault.repo   epel.repo
CentOS-fasttrack.repo  cloudera-cdh5.repo  epel-testing.repo

```
# Cloudera Manager Repo
```
[cloudera-manager]
# Packages for Cloudera Manager, Version 5, on RedHat or CentOS 6 x86_64         
name=Cloudera Manager
baseurl=https://archive.cloudera.com/cm5/redhat/6/x86_64/cm/5.11/
gpgkey =https://archive.cloudera.com/cm5/redhat/6/x86_64/cm/RPM-GPG-KEY-cloudera 
gpgcheck = 1

```