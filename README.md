
Example for how to deploy qemu from bootable iso ->
https://gist.github.com/zg/38a3afa112ddf7de4912aafc249ec82f

Download NetBSD v10.0 boot media from:
http://nycdn.netbsd.org/pub/NetBSD-daily/netbsd-10/202404140340Z/images/

alter to NetBSD

0. create persistent storage - a.k.a disk image
```
qemu-img create -f raw VM10G.raw 10G
```


1. boot from CD: 
```
qemu-system-x86_64 -m 256 -hda VM10G.raw -cdrom NetBSD-10.0-amd64.iso
```

2. boot only from hd disk imange - a.k.a persistent storage
```
qemu-system-x86_64 -m 256 -hda VM10G.raw`
```

