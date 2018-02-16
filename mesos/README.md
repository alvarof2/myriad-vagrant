# Plain Apache Mesos Environment

This is the Vagrant-libvirt based environment for testing Apache Myriad
project in a Mesos cluster.

```
$ source setup-env 

This Vagrant environment is ready for the following settings:                         

- MESOS_ARCH: 1m4a                         
- HADOOP_VERSION: 2.7.0                    
- ZOOKEEPER_VERSION: 3.4.11                

'vagrant up --provider=libvirt' and happy hacking!  
``` 


```
$ vagrant up  --provider=libvirt
[...]
PLAY RECAP
*********************************************************************
build                      : ok=36   changed=28   unreachable=0    failed=0   
mesos-a1                   : ok=28   changed=25   unreachable=0    failed=0   
mesos-a2                   : ok=31   changed=28   unreachable=0    failed=0   
mesos-a3                   : ok=31   changed=28   unreachable=0    failed=0   
mesos-a4                   : ok=31   changed=28   unreachable=0    failed=0   
mesos-m1                   : ok=41   changed=38   unreachable=0    failed=0 

$ vagrant status   
Current machine states:

build                     running (libvirt)
mesos-m1                  running (libvirt)
mesos-a1                  running (libvirt)
mesos-a2                  running (libvirt)
mesos-a3                  running (libvirt)
mesos-a4                  running (libvirt)
```


```
$ vagrant ssh build
[vagrant@build ~]$ tree -d -L 1 /opt/
/opt/
├── hadoop
├── mesos
└── myriad

