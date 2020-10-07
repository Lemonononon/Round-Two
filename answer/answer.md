# problem-set-1







### 1-1

C语言能做到编译成不依赖操作系统的二进制代码，脱离系统之外C语言的库最丰富、完整。

### 1-2

异：unix几乎整个系统以 C 编写，对于硬件的兼容性比windows要高
	   unix是以文本为基础处理信息的，而windows以二进制内容

同：windows和unix都是多用户、多进程的操作系统

### 1-3

我支持unix哲学，小而精巧的东西值得被欣赏。

大型的程序难以维护、纠错，可能会出现为了微小收益而使整个程序变得冗杂的现象。

对程序扩展性的限制就像是人为给项目设置了上限，可扩展性增加了我对unix的好感。

### 1-4

GPL/MIT/APACHE/BSD 

GPL: “传染性”——只要在一个软件中使用GPL 协议的产品，则该软件产品必须也采用GPL协议，既必须也是开源和免费。

MIT: 无论以二进制发布还是源码发布，都需要在发行版里包含原许可协议的声明。

APACHE: 需要给代码的用户一份Apache Licence。

BSD: 如果再发布的产品中包含源代码，则在源代码中必须带有原来代码中的BSD协议。所以如果开发出的游戏含有源代码，则需要附上许可证。

### 1-5

Git

使用的是GPL协议

### 1-7

个人感觉Linux不能算是一个操作系统，只是为了沟通方便，大家在日常交流时会把这一系列以Linux为kernel的操作系统统称为Linux系统。Linux过于精简，为了能让这个内核拥有更多功能、完善的用户界面和更佳的使用体验，许多开发人员便开始把各种组件添加到这个内核之上，这才构建成了一个完整的 Linux 操作系统，通常称之为“Linux发行版”。

### 1-8

虚拟机通过模拟出系统运行所需要的硬件环境，构建出一整套虚拟硬件平台（CPU/Memory/Storge等）使用户可以在虚拟的平台去安装新的操作系统和需要的软件。



虚拟机是基于Hypervisor（虚拟机管理器）建立的，Hypervisor是一种运行在物理服务器和操作系统之间的中间软件层，可以直接运行在物理设备上、或者运行在宿主操作系统中，允许多个操作系统和应用共享一套基础物理硬件。在运行虚拟机客户端挂载的操作系统时，它负责加载所有虚拟机客户端的操作系统，同时对每一台虚拟机进行内存、网络等资源的分配。



### 2-1

两个MY_VALUE的值不一样，在shell中直接定义的MY_VALUE是临时环境变量，只在当前shell中有效。

### 2-2

根据/etc/profile中定义（.bashrc或者.bash_profile）对应添加该用户的永久生效环境变量，作用范围为当前用户的bash

### 2-4

` sudo visudo`或者`sudoedit /etc/sudoers`

然后添加dino ALL=(ALL:ALL) ALL

### 2-5

用户名 口令 UID GID 备注 主目录 登录shell

```
root:x:0:0:root:/root:/bin/zsh
daemon:x:1:1:daemon:/usr/sbin:/usr/sbin/nologin
bin:x:2:2:bin:/bin:/usr/sbin/nologin
sys:x:3:3:sys:/dev:/usr/sbin/nologin
sync:x:4:65534:sync:/bin:/bin/sync
games:x:5:60:games:/usr/games:/usr/sbin/nologin
man:x:6:12:man:/var/cache/man:/usr/sbin/nologin
lp:x:7:7:lp:/var/spool/lpd:/usr/sbin/nologin
mail:x:8:8:mail:/var/mail:/usr/sbin/nologin
news:x:9:9:news:/var/spool/news:/usr/sbin/nologin
uucp:x:10:10:uucp:/var/spool/uucp:/usr/sbin/nologin
proxy:x:13:13:proxy:/bin:/usr/sbin/nologin
www-data:x:33:33:www-data:/var/www:/usr/sbin/nologin
backup:x:34:34:backup:/var/backups:/usr/sbin/nologin
list:x:38:38:Mailing List Manager:/var/list:/usr/sbin/nologin
irc:x:39:39:ircd:/var/run/ircd:/usr/sbin/nologin
gnats:x:41:41:Gnats Bug-Reporting System (admin):/var/lib/gnats:/usr/sbin/nologin
nobody:x:65534:65534:nobody:/nonexistent:/usr/sbin/nologin
systemd-network:x:100:102:systemd Network Management,,,:/run/systemd/netif:/usr/sbin/nologin
systemd-resolve:x:101:103:systemd Resolver,,,:/run/systemd/resolve:/usr/sbin/nologin
syslog:x:102:106::/home/syslog:/usr/sbin/nologin
messagebus:x:103:107::/nonexistent:/usr/sbin/nologin
_apt:x:104:65534::/nonexistent:/usr/sbin/nologin
uuidd:x:105:111::/run/uuidd:/usr/sbin/nologin
avahi-autoipd:x:106:112:Avahi autoip daemon,,,:/var/lib/avahi-autoipd:/usr/sbin/nologin
usbmux:x:107:46:usbmux daemon,,,:/var/lib/usbmux:/usr/sbin/nologin
dnsmasq:x:108:65534:dnsmasq,,,:/var/lib/misc:/usr/sbin/nologin
rtkit:x:109:114:RealtimeKit,,,:/proc:/usr/sbin/nologin
cups-pk-helper:x:110:116:user for cups-pk-helper service,,,:/home/cups-pk-helper:/usr/sbin/nologin
speech-dispatcher:x:111:29:Speech Dispatcher,,,:/var/run/speech-dispatcher:/bin/false
whoopsie:x:112:117::/nonexistent:/bin/false
kernoops:x:113:65534:Kernel Oops Tracking Daemon,,,:/:/usr/sbin/nologin
saned:x:114:119::/var/lib/saned:/usr/sbin/nologin
pulse:x:115:120:PulseAudio daemon,,,:/var/run/pulse:/usr/sbin/nologin
avahi:x:116:122:Avahi mDNS daemon,,,:/var/run/avahi-daemon:/usr/sbin/nologin
colord:x:117:123:colord colour management daemon,,,:/var/lib/colord:/usr/sbin/nologin
hplip:x:118:7:HPLIP system user,,,:/var/run/hplip:/bin/false
geoclue:x:119:124::/var/lib/geoclue:/usr/sbin/nologin
gnome-initial-setup:x:120:65534::/run/gnome-initial-setup/:/bin/false
gdm:x:121:125:Gnome Display Manager:/var/lib/gdm3:/bin/false
lemonon:x:1000:1000:Ubuntu,,,:/home/lemonon:/usr/bin/zsh
mysql:x:122:127:MySQL Server,,,:/nonexistent:/bin/false
dino:x:1001:1001::/home/dino:/bin/sh
```





###  2-6

XTerm是一个X Window System上的终端模拟器，用来提供多个独立的SHELL输入输出。

depends

- libc6 (>= 2.15) [amd64, s390x]
      GNU C Library: Shared libraries
      also a virtual package provided by libc6-udeb 

- libc6 (>= 2.17) [arm64, ppc64el]


- libc6 (>= 2.28) [armhf, i386]


- libfontconfig1 (>= 2.12.6)
      generic font configuration library - runtime 
- libfreetype6 (>= 2.2.1)
      FreeType 2 font engine, shared library files 

- libice6 (>= 1:1.0.0)
      X11 Inter-Client Exchange library 

- libtinfo6 (>= 6)
      shared low-level terminfo library for terminal handling 
- libutempter0 (>= 1.1.5)
      privileged helper for utmp/wtmp updates (runtime) 

- libx11-6
      X11 client-side library 

- libxaw7
      X11 Athena Widget library 

- libxext6
      X11 miscellaneous extension library 
- libxft2 (>> 2.1.1)
      FreeType-based font drawing library for X 

- libxinerama1
      X11 Xinerama extension library 

- libxmu6
      X11 miscellaneous utility library 

- libxpm4
      X11 pixmap library 
- libxt6
      X11 toolkit intrinsics library 

- xbitmaps
      Base X bitmaps 

### 2-7

很多商业软件如Matlab、Mathematica等软件不是开源的。

Main是安装ubuntu时默认启用的存储库，仅包含FOSS，在用户使用发行版的停用之前，ubuntu会一直提供Main中软件的安全更新。

Universe中的软件由社区打包维护，有大量的开源软件。

Multiverse包含的不是FOSS的软件，而且ubuntu默认无法启用此存储库。

Restricted受限制的存储库由专有驱动程序组成。

Partner该存储库由Ubuntu为其合作伙伴打包的专有软件组成。

### 2-8

`cd ../../../..`根据需要添加`..`

### 2-9

只显示隐藏文件 ：`ls -AF |grep '^\'`      `ls -d .*`

### 2-10

`find /etc/ -name "*.conf"` 

### 2-11

首字母为`b`：块设备文件，设备文件是普通文件和程序访问硬件设备的入口

首字母为`c`：字符设备文件，一次传输一个字节的设备被称为字符设备，传输数据的最小单位为一个字节

首字母为`d`：目录（dirtectory）

首字母为`l`：链接文件（link）



```
crw-------  1 root    root     10, 175 Oct  7 06:32 agpgart
crw-r--r--  1 root    root     10, 235 Oct  7 06:32 autofs
drwxr-xr-x  2 root    root         460 Oct  7 06:32 block
drwxr-xr-x  2 root    root          80 Oct  7 06:31 bsg
crw-------  1 root    root     10, 234 Oct  7 06:31 btrfs-control
drwxr-xr-x  3 root    root          60 Oct  7 06:31 bus
lrwxrwxrwx  1 root    root           3 Oct  7 06:32 cdrom -> sr0
lrwxrwxrwx  1 root    root           3 Oct  7 06:32 cdrw -> sr0
drwxr-xr-x  2 root    root        3700 Oct  7 06:32 char
crw-------  1 root    root      5,   1 Oct  7 06:32 console
lrwxrwxrwx  1 root    root          11 Oct  7 06:31 core -> /proc/kcore
crw-------  1 root    root     10,  59 Oct  7 06:32 cpu_dma_latency
crw-------  1 root    root     10, 203 Oct  7 06:31 cuse
drwxr-xr-x  6 root    root         120 Oct  7 06:31 disk
crw-rw----+ 1 root    audio    14,   9 Oct  7 06:32 dmmidi
drwxr-xr-x  3 root    root         100 Oct  7 06:32 dri
lrwxrwxrwx  1 root    root           3 Oct  7 06:32 dvd -> sr0
crw-------  1 root    root     10,  62 Oct  7 06:32 ecryptfs
crw-rw----  1 root    video    29,   0 Oct  7 06:32 fb0
lrwxrwxrwx  1 root    root          13 Oct  7 06:31 fd -> /proc/self/fd
crw-rw-rw-  1 root    root      1,   7 Oct  7 06:32 full
crw-rw-rw-  1 root    root     10, 229 Oct  7 06:32 fuse
crw-------  1 root    root    242,   0 Oct  7 06:32 hidraw0
crw-------  1 root    root     10, 228 Oct  7 06:32 hpet
drwxr-xr-x  2 root    root           0 Oct  7 06:31 hugepages
crw-------  1 root    root     10, 183 Oct  7 06:32 hwrng
lrwxrwxrwx  1 root    root          25 Oct  7 06:31 initctl -> /run/systemd/initctl/fifo
drwxr-xr-x  4 root    root         260 Oct  7 06:32 input
crw-r--r--  1 root    root      1,  11 Oct  7 06:32 kmsg
drwxr-xr-x  2 root    root          60 Oct  7 06:31 lightnvm
lrwxrwxrwx  1 root    root          28 Oct  7 06:31 log -> /run/systemd/journal/dev-log
brw-rw----  1 root    disk      7,   0 Oct  7 06:32 loop0
brw-rw----  1 root    disk      7,   1 Oct  7 06:32 loop1
brw-rw----  1 root    disk      7,  10 Oct  7 06:32 loop10
brw-rw----  1 root    disk      7,  11 Oct  7 06:32 loop11
brw-rw----  1 root    disk      7,  12 Oct  7 06:32 loop12
brw-rw----  1 root    disk      7,  13 Oct  7 06:32 loop13
brw-rw----  1 root    disk      7,  14 Oct  7 06:32 loop14
brw-rw----  1 root    disk      7,  15 Oct  7 06:32 loop15
brw-rw----  1 root    disk      7,  16 Oct  7 06:32 loop16
brw-rw----  1 root    disk      7,  17 Oct  7 06:32 loop17
brw-rw----  1 root    disk      7,   2 Oct  7 06:32 loop2
brw-rw----  1 root    disk      7,   3 Oct  7 06:32 loop3
brw-rw----  1 root    disk      7,   4 Oct  7 06:32 loop4
brw-rw----  1 root    disk      7,   5 Oct  7 06:32 loop5
brw-rw----  1 root    disk      7,   6 Oct  7 06:32 loop6
brw-rw----  1 root    disk      7,   7 Oct  7 06:32 loop7
brw-rw----  1 root    disk      7,   8 Oct  7 06:32 loop8
brw-rw----  1 root    disk      7,   9 Oct  7 06:32 loop9
crw-rw----  1 root    disk     10, 237 Oct  7 06:32 loop-control
drwxr-xr-x  2 root    root          60 Oct  7 06:31 mapper
crw-------  1 root    root     10, 227 Oct  7 06:32 mcelog
crw-r-----  1 root    kmem      1,   1 Oct  7 06:32 mem
crw-rw----+ 1 root    audio    14,   2 Oct  7 06:32 midi
drwxrwxrwt  2 root    root          40 Oct  7 06:31 mqueue
drwxr-xr-x  2 root    root          60 Oct  7 06:31 net
crw-rw-rw-  1 root    root      1,   3 Oct  7 06:32 null
crw-------  1 root    root     10, 144 Oct  7 06:31 nvram
crw-r-----  1 root    kmem      1,   4 Oct  7 06:32 port
crw-------  1 root    root    108,   0 Oct  7 06:32 ppp
crw-------  1 root    root     10,   1 Oct  7 06:32 psaux
crw-rw-rw-  1 root    tty       5,   2 Oct  7 07:25 ptmx
drwxr-xr-x  2 root    root           0 Oct  7 06:31 pts
crw-rw-rw-  1 root    root      1,   8 Oct  7 06:32 random
crw-rw-r--+ 1 root    netdev   10, 242 Oct  7 06:32 rfkill
lrwxrwxrwx  1 root    root           4 Oct  7 06:32 rtc -> rtc0
crw-------  1 root    root    249,   0 Oct  7 06:32 rtc0
brw-rw----  1 root    disk      8,   0 Oct  7 06:32 sda
brw-rw----  1 root    disk      8,   1 Oct  7 06:32 sda1
crw-rw----  1 root    disk     21,   0 Oct  7 06:32 sg0
crw-rw----+ 1 root    cdrom    21,   1 Oct  7 06:32 sg1
drwxrwxrwt  2 root    root          40 Oct  7 06:31 shm
crw-------  1 root    root     10, 231 Oct  7 06:32 snapshot
drwxr-xr-x  3 root    root         200 Oct  7 06:32 snd
brw-rw----+ 1 root    cdrom    11,   0 Oct  7 06:32 sr0
lrwxrwxrwx  1 root    root          15 Oct  7 06:31 stderr -> /proc/self/fd/2
lrwxrwxrwx  1 root    root          15 Oct  7 06:31 stdin -> /proc/self/fd/0
lrwxrwxrwx  1 root    root          15 Oct  7 06:31 stdout -> /proc/self/fd/1
crw-rw-rw-  1 root    tty       5,   0 Oct  7 06:32 tty
crw--w----  1 root    tty       4,   0 Oct  7 06:32 tty0
crw--w----  1 root    tty       4,   1 Oct  7 06:32 tty1
crw--w----  1 root    tty       4,  10 Oct  7 06:32 tty10
crw--w----  1 root    tty       4,  11 Oct  7 06:32 tty11
crw--w----  1 root    tty       4,  12 Oct  7 06:32 tty12
crw--w----  1 root    tty       4,  13 Oct  7 06:32 tty13
crw--w----  1 root    tty       4,  14 Oct  7 06:32 tty14
crw--w----  1 root    tty       4,  15 Oct  7 06:32 tty15
crw--w----  1 root    tty       4,  16 Oct  7 06:32 tty16
crw--w----  1 root    tty       4,  17 Oct  7 06:32 tty17
crw--w----  1 root    tty       4,  18 Oct  7 06:32 tty18
crw--w----  1 root    tty       4,  19 Oct  7 06:32 tty19
crw--w----  1 lemonon tty       4,   2 Oct  7 06:32 tty2
crw--w----  1 root    tty       4,  20 Oct  7 06:32 tty20
crw--w----  1 root    tty       4,  21 Oct  7 06:32 tty21
crw--w----  1 root    tty       4,  22 Oct  7 06:32 tty22
crw--w----  1 root    tty       4,  23 Oct  7 06:32 tty23
crw--w----  1 root    tty       4,  24 Oct  7 06:32 tty24
crw--w----  1 root    tty       4,  25 Oct  7 06:32 tty25
crw--w----  1 root    tty       4,  26 Oct  7 06:32 tty26
crw--w----  1 root    tty       4,  27 Oct  7 06:32 tty27
crw--w----  1 root    tty       4,  28 Oct  7 06:32 tty28
crw--w----  1 root    tty       4,  29 Oct  7 06:32 tty29
crw--w----  1 root    tty       4,   3 Oct  7 06:32 tty3
crw--w----  1 root    tty       4,  30 Oct  7 06:32 tty30
crw--w----  1 root    tty       4,  31 Oct  7 06:32 tty31
crw--w----  1 root    tty       4,  32 Oct  7 06:32 tty32
crw--w----  1 root    tty       4,  33 Oct  7 06:32 tty33
crw--w----  1 root    tty       4,  34 Oct  7 06:32 tty34
crw--w----  1 root    tty       4,  35 Oct  7 06:32 tty35
crw--w----  1 root    tty       4,  36 Oct  7 06:32 tty36
crw--w----  1 root    tty       4,  37 Oct  7 06:32 tty37
crw--w----  1 root    tty       4,  38 Oct  7 06:32 tty38
crw--w----  1 root    tty       4,  39 Oct  7 06:32 tty39
crw--w----  1 root    tty       4,   4 Oct  7 06:32 tty4
crw--w----  1 root    tty       4,  40 Oct  7 06:32 tty40
crw--w----  1 root    tty       4,  41 Oct  7 06:32 tty41
crw--w----  1 root    tty       4,  42 Oct  7 06:32 tty42
crw--w----  1 root    tty       4,  43 Oct  7 06:32 tty43
crw--w----  1 root    tty       4,  44 Oct  7 06:32 tty44
crw--w----  1 root    tty       4,  45 Oct  7 06:32 tty45
crw--w----  1 root    tty       4,  46 Oct  7 06:32 tty46
crw--w----  1 root    tty       4,  47 Oct  7 06:32 tty47
crw--w----  1 root    tty       4,  48 Oct  7 06:32 tty48
crw--w----  1 root    tty       4,  49 Oct  7 06:32 tty49
crw--w----  1 root    tty       4,   5 Oct  7 06:32 tty5
crw--w----  1 root    tty       4,  50 Oct  7 06:32 tty50
crw--w----  1 root    tty       4,  51 Oct  7 06:32 tty51
crw--w----  1 root    tty       4,  52 Oct  7 06:32 tty52
crw--w----  1 root    tty       4,  53 Oct  7 06:32 tty53
crw--w----  1 root    tty       4,  54 Oct  7 06:32 tty54
crw--w----  1 root    tty       4,  55 Oct  7 06:32 tty55
crw--w----  1 root    tty       4,  56 Oct  7 06:32 tty56
crw--w----  1 root    tty       4,  57 Oct  7 06:32 tty57
crw--w----  1 root    tty       4,  58 Oct  7 06:32 tty58
crw--w----  1 root    tty       4,  59 Oct  7 06:32 tty59
crw--w----  1 root    tty       4,   6 Oct  7 06:32 tty6
crw--w----  1 root    tty       4,  60 Oct  7 06:32 tty60
crw--w----  1 root    tty       4,  61 Oct  7 06:32 tty61
crw--w----  1 root    tty       4,  62 Oct  7 06:32 tty62
crw--w----  1 root    tty       4,  63 Oct  7 06:32 tty63
crw--w----  1 root    tty       4,   7 Oct  7 06:32 tty7
crw--w----  1 root    tty       4,   8 Oct  7 06:32 tty8
crw--w----  1 root    tty       4,   9 Oct  7 06:32 tty9
crw-------  1 root    root      5,   3 Oct  7 06:32 ttyprintk
crw-rw----  1 root    dialout   4,  64 Oct  7 06:32 ttyS0
crw-rw----  1 root    dialout   4,  65 Oct  7 06:32 ttyS1
crw-rw----  1 root    dialout   4,  74 Oct  7 06:32 ttyS10
crw-rw----  1 root    dialout   4,  75 Oct  7 06:32 ttyS11
crw-rw----  1 root    dialout   4,  76 Oct  7 06:32 ttyS12
crw-rw----  1 root    dialout   4,  77 Oct  7 06:32 ttyS13
crw-rw----  1 root    dialout   4,  78 Oct  7 06:32 ttyS14
crw-rw----  1 root    dialout   4,  79 Oct  7 06:32 ttyS15
crw-rw----  1 root    dialout   4,  80 Oct  7 06:32 ttyS16
crw-rw----  1 root    dialout   4,  81 Oct  7 06:32 ttyS17
crw-rw----  1 root    dialout   4,  82 Oct  7 06:32 ttyS18
crw-rw----  1 root    dialout   4,  83 Oct  7 06:32 ttyS19
crw-rw----  1 root    dialout   4,  66 Oct  7 06:32 ttyS2
crw-rw----  1 root    dialout   4,  84 Oct  7 06:32 ttyS20
crw-rw----  1 root    dialout   4,  85 Oct  7 06:32 ttyS21
crw-rw----  1 root    dialout   4,  86 Oct  7 06:32 ttyS22
crw-rw----  1 root    dialout   4,  87 Oct  7 06:32 ttyS23
crw-rw----  1 root    dialout   4,  88 Oct  7 06:32 ttyS24
crw-rw----  1 root    dialout   4,  89 Oct  7 06:32 ttyS25
crw-rw----  1 root    dialout   4,  90 Oct  7 06:32 ttyS26
crw-rw----  1 root    dialout   4,  91 Oct  7 06:32 ttyS27
crw-rw----  1 root    dialout   4,  92 Oct  7 06:32 ttyS28
crw-rw----  1 root    dialout   4,  93 Oct  7 06:32 ttyS29
crw-rw----  1 root    dialout   4,  67 Oct  7 06:32 ttyS3
crw-rw----  1 root    dialout   4,  94 Oct  7 06:32 ttyS30
crw-rw----  1 root    dialout   4,  95 Oct  7 06:32 ttyS31
crw-rw----  1 root    dialout   4,  68 Oct  7 06:32 ttyS4
crw-rw----  1 root    dialout   4,  69 Oct  7 06:32 ttyS5
crw-rw----  1 root    dialout   4,  70 Oct  7 06:32 ttyS6
crw-rw----  1 root    dialout   4,  71 Oct  7 06:32 ttyS7
crw-rw----  1 root    dialout   4,  72 Oct  7 06:32 ttyS8
crw-rw----  1 root    dialout   4,  73 Oct  7 06:32 ttyS9
crw-------  1 root    root     10,  60 Oct  7 06:32 udmabuf
crw-------  1 root    root     10, 239 Oct  7 06:31 uhid
crw-------  1 root    root     10, 223 Oct  7 06:32 uinput
crw-rw-rw-  1 root    root      1,   9 Oct  7 06:32 urandom
crw-------  1 root    root     10, 240 Oct  7 06:31 userio
crw-rw----  1 root    tty       7,   0 Oct  7 06:32 vcs
crw-rw----  1 root    tty       7,   1 Oct  7 06:32 vcs1
crw-rw----  1 root    tty       7,   2 Oct  7 06:32 vcs2
crw-rw----  1 root    tty       7,   3 Oct  7 06:32 vcs3
crw-rw----  1 root    tty       7,   4 Oct  7 06:32 vcs4
crw-rw----  1 root    tty       7,   5 Oct  7 06:32 vcs5
crw-rw----  1 root    tty       7,   6 Oct  7 06:32 vcs6
crw-rw----  1 root    tty       7, 128 Oct  7 06:32 vcsa
crw-rw----  1 root    tty       7, 129 Oct  7 06:32 vcsa1
crw-rw----  1 root    tty       7, 130 Oct  7 06:32 vcsa2
crw-rw----  1 root    tty       7, 131 Oct  7 06:32 vcsa3
crw-rw----  1 root    tty       7, 132 Oct  7 06:32 vcsa4
crw-rw----  1 root    tty       7, 133 Oct  7 06:32 vcsa5
crw-rw----  1 root    tty       7, 134 Oct  7 06:32 vcsa6
crw-rw----  1 root    tty       7,  64 Oct  7 06:32 vcsu
crw-rw----  1 root    tty       7,  65 Oct  7 06:32 vcsu1
crw-rw----  1 root    tty       7,  66 Oct  7 06:32 vcsu2
crw-rw----  1 root    tty       7,  67 Oct  7 06:32 vcsu3
crw-rw----  1 root    tty       7,  68 Oct  7 06:32 vcsu4
crw-rw----  1 root    tty       7,  69 Oct  7 06:32 vcsu5
crw-rw----  1 root    tty       7,  70 Oct  7 06:32 vcsu6
drwxr-xr-x  2 root    root          60 Oct  7 06:31 vfio
crw-------  1 root    root     10,  63 Oct  7 06:32 vga_arbiter
crw-------  1 root    root     10, 137 Oct  7 06:31 vhci
crw-------  1 root    root     10, 238 Oct  7 06:31 vhost-net
crw-------  1 root    root     10, 241 Oct  7 06:31 vhost-vsock
crw-------  1 root    root     10,  58 Oct  7 06:32 vmci
crw-rw-rw-  1 root    root     10,  57 Oct  7 06:32 vsock
crw-rw-rw-  1 root    root      1,   5 Oct  7 06:32 zero
crw-------  1 root    root     10, 249 Oct  7 06:31 zfs
```



