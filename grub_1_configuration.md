# Grub menu booting 103 systems out of 144 partitions  
color          white/blue black/light-gray  
default        0  
timeout        1000  

# Disk hda has 60 partitions fully populated 56 are bootable systems  


title          DOS 6.22 @ hda1  
unhide         (hd0,0)  
root           (hd0,0)  
chainloader    +1  
	
#  hda2 is the extended partition  and has no storage space itself  

title          Empty @ hda3 #initially used by a BSD system moved to another disk  
root           (hd0,2)  
chainloader    +1  

title          Empty @ hda4#initially used by a BSD system moved to another disk  

root           (hd0,3)  
chainloader    +1  

# hda5 is a swap partition common to all Linux in the box  

title          Puppy 1.0.6 @ hda6  
root           (hd0,5)  
chainloader    +1  

title          Arch 0.71 @ hda7  
root           (hd0,6)  
chainloader    +1  

title          Mandrake 9.2 @ hda8  
root           (hd0,7)
chainloader    +1

title          Suse 9.1 pro @ hda9
root           (hd0,8)
chainloader    +1

title          eLive 0.3 @ hda10
root           (hd0,9)
chainloader    +1

title          Red Hat 9 @ hda11
root           (hd0,10)
chainloader    +1

title          Lycoris 4 @ hda12
root           (hd0,11)
chainloader    +1

title          Libranet 2.8.1 @ hda13
root           (hd0,12)
chainloader    +1

title          Mandrake 10 @hda14
root           (hd0,13)
chainloader    +1

title          Debian Woody @ hda15
root           (hd0,14)
chainloader    +1


title          Yoper 2.0.0 @ hda16
root           (hd0,15)
chainloader    +1

title          Knoppix 3.6 @ hda17
root           (hd0,16)
chainloader    +1

title          Bufflo 1.5 @ hda18
root           (hd0,17)
chainloader    +1

title          Kanotix 2004.9 @ hda19
root           (hd0,18)
chainloader    +1

title          Kalango 3.2 @ hda20
root           (hd0,19)
chainloader    +1

title          Blax 30001 @ hda21
root           (hd0,20)
chainloader    +1

title          Fedora Core 4 @ hda22
root           (hd0,21)
chainloader    +1

title          Debian Sarge (booted directly because high partitions not supported) in hda23
root           (hd0,22)
kernel         /boot/vmlinuz-2.4.27-2-386 root=/dev/hda23 ro 
initrd         /boot/initrd.img-2.4.27-2-386

title          Red Flag 4.1 @ hda24
root           (hd0,23)
chainloader    +1

title          Linare prof Edition 2 @ hda25
root           (hd0,24)
chainloader    +1

title          Tiny Sofa 2.0 @ hda26
root           (hd0,25)
chainloader    +1

title          Slackware 10.0 @ hda27 
root           (hd0,26)
chainloader    +1

title          Xandros 201 @ hda28
root           (hd0,27)
chainloader    +1

title          Vine 3.2 @ hda29
root           (hd0,28)
chainloader    +1
                  
title          Specifix 0.15 @ hda30
root           (hd0,29)
chainloader    +1
                  
title          Ubunto 5.04 @ hda31
root           (hd0,30)
chainloader    +1
                  
title          PCLinuxOS 9.1 @ hda32
root           (hd0,31)
chainloader    +1

#  Here is the approximate 137Gb barrier in the hard disk hda

title          Asian Linux  @ hda33
root           (hd0,32)
chainloader    +1
                  
title          Ubuntu 6.04 Dapper (by direct boot) @ hda34
root           (hd0,33)
kernel         /boot/vmlinuz-2.6.15-8-386 root=/dev/hda34 ro quiet splash
initrd         /boot/initrd.img-2.6.15-8-386
               	

title          Wolvix 1.0.4  @ hda35
root           (hd0,34)
kernel         /boot/vmlinuz rw root=/dev/hda35

title          Mepis 3.4.2 rc1 (by direct booting) @ hda36
root           (hd0,35)
kernel         /boot/vmlinuz-2.6.12-1-586tsc root=/dev/hda36 nomce quiet splash=verbose vga=791 
initrd         /boot/initrd.img-2.6.12-1-586tsc


title          TurboLinux V7 @ hda37 (boot with Slackware 10 kernel in hda27 +rw)
root           (hd0,36)
kernel         (hd0,26)/boot/vmlinuz rw root=/dev/hda37
                                  
                  
title          Slampp 1.1 @ hda38
root           (hd0,37)
chainloader    +1
                  
                                  
                  
title          Slax 5.0.4 @ hda39
root           (hd0,38)
chainloader    +1
                  
                  
title          PCLinuxOS 0.92 @ hda40
root           (hd0,39)
chainloader    +1
                                  
                  
title          Sam 1.1 @ hda41
root           (hd0,40)
chainloader    +1
                  
title          Vector 5.1 @ hda42
root           (hd0,41)
chainloader    +1
                  
                                  
                  
title          Suse 10.0 @ hda43
root           (hd0,42)
chainloader    +1
                  
title          Kororaa 2005 Beta 2 @ hda44
root           (hd0,43)
chainloader    +1
                                      
title          smgl 0.45 @ hda45
root           (hd0,44)
kernel         /boot/vmlinuz root=/dev/hda45 ro

title          Lunar 1.6 @ hda46
root           (hd0,45)
kernel         /boot/2.6.14.1-normal ro root=/dev/hda46 devfs=no mount
                  
title          Foresight 0.93 @ hda47
root           (hd0,46)
chainloader    +1
                                    
                  
title          Skolelinux Pro 6  in hda48
root           (hd0,47)
kernel         /boot/vmlinuz-2.6.8-2-386 root=/dev/hda48 ro 
initrd         /boot/initrd.img-2.6.8-2-386
                                      
                  
title          Kubuntu dapper in hda49
root           (hd0,48)
kernel         /boot/vmlinuz-2.6.12-9-386 root=/dev/hda49 ro quiet splash
initrd         /boot/initrd.img-2.6.12-9-386
                                      
                  
title          Klax 3.5 @ hda50
root           (hd0,49)
chainloader    +1
                                      
                  
title          K12LTSP 4.10 (need rw switch on) @ hda51
root           (hd0,50)
kernel         /boot/vmlinuz-2.6.7-1.494.2.2 rw root=/dev/hda51
initrd         /boot/initrd-2.6.7-1.494.2.2.img
                                      
                  
title          Progeny 2.0 booted by Slackware's kernel  @ hda52
root           (hd0,51)
kernel         (hd0,26)/boot/vmlinuz ro root=/dev/hda52
                                      
                  
title          grml 0.5 @ hda53
root           (hd0,52)
chainloader    +1
                                      
                  
title          Fedora Core 2 @ hda54 (must be booted directly  with rw switch)
root           (hd0,53)
kernel         /boot/vmlinuz-2.6.5-1.358 rw root=/dev/hda54
initrd         /boot/initrd-2.6.5-1.358.img
                  
title          Whax 3.0 @ hda55
root           (hd0,54)
chainloader    +1
                                      
                  
title          Troppix 1.2 @ hda56
root           (hd0,55)
chainloader    +1
                                      
                  
title          TopologLinux 6.0 @ hda57
root           (hd0,56)
chainloader    +1
                                      
                  
title          Haansoft 2006 ws @ hda58
root           (hd0,57)
chainloader    +1
                                      
                  
title          Fedora Core 3 @ hda59
root           (hd0,58)
chainloader    +1
                                      
                  
title          Scientific Linux (with rw) @ hda60
root           (hd0,59)
kernel         /boot/vmlinuz-2.6.9-5.0.5.EL rw root=/dev/hda60 rhgb quiet
initrd         /boot/initrd-2.6.9-5.0.5.EL.img
                                      

# Disk hdc has 54 partitions with 30 systems

title          Dos 7.10 @ hdc1
hide           (hd0,0)
unhide         (hd1,0)
map            (hd1) (hd0)
map            (hd0) (hd1)
root           (hd1,0)
makeactive
chainloader    +1

title          Win98 @ hdc2
hide           (hd0,0)
hide           (hd1,0)
unhide         (hd1,1)
root           (hd1,1)
makeactive
map            (hd1) (hd0)
map            (hd0) (hd1)
chainloader    +1

title          Empty @ hdc3
root           (hd1,2)
chainloader    +1

# Extended partition is hdc4

title          B2D Pure KDE 2005 @ hdc5
root           (hd1,4)
chainloader    +1

title          CollegeLinux 2.5 @ hdc6
root           (hd1,5)
chainloader    +1

title          Berry 0.65 @ hdc7
root           (hd1,6)
chainloader    +1

title          Morhpix KDE 0.4 @ hdc8
root           (hd1,7)
chainloader    +1

title          Feather 0.6 @ hdc9
root           (hd1,8)
chainloader    +1

title          Buffalo 1.7.3.9 @ hdc10
root           (hd1,9)
chainloader    +1

title          CentOS 4.1  @ hdc11
root           (hd1,10)
chainloader    +1

title          Vector 4.3 @ hdc12
root           (hd1,11)
chainloader    +1

title          Tao Linux 4.0 @ hdc13
root           (hd1,12)
chainloader    +1

title          Frugaalware 0.1 @ hdc14
root           (hd1,13)
chainloader    +1

title          Agnula Demudi 1.2 @ hdc15
root           (hd1,14)
chainloader    +1

title          Damn Small Linux @ hdc16 
root           (hd1,15)
chainloader    +1

title          Monoppix 1.1.8 booted by Slackware 10.2 kernel from (hd1,34) @ hdc17
root           (hd1,16)
kernel         (hd1,34)/boot/vmlinuz ro root=/dev/hdc17 

title          Symphony A4 @ hdc18
root           (hd1,17)
chainloader    +1

title          Pocket Linux 1.2 @ hdc19
root           (hd1,18)
chainloader    +1

title          UltimaLinux 4.0 @ hdc20
root           (hd1,19)
chainloader    +1

title          VLOS 1.2 @ hdc21
root           (hd1,20)
kernel         /boot/vmlinuz-2.6.12-vidalinux_r3 ro root=/dev/ram0 init=/linuxrc real_root=/dev/hdc21 video=vesafb:1024x768-32@85 splash=silent,theme:vlos-1.2 quiet CONSOLE=/dev/tty1
initrd         /boot/initrd-2.6.12-vidalinux_r3.img

title          Tiny Sofa (Ceara) @ hdc22
root           (hd1,21)
chainloader    +1

title          64 Studio 0.6 @ hdc23
root		(hd1,22)
kernel         /boot/vmlinuz-2.6.13-1-multimedia-amd64-generic root=/dev/hdc23 ro vga=791 splash=silent
initrd          /boot/initrd.img-2.6.13-1-multimedia-amd64-generic

title          Empty @ hdc24
root           (hd1,23)
chainloader    +1

title          Empty @ hdc25
root           (hd1,24)
chainloader    +1

title          Empty @ hdc26
root           (hd1,25)
chainloader    +1

# here is the approximate boundary of the 137Gb barrier of hdc

title          Empty @ hdc27
root           (hd1,26)
chainloader    +1

title          Empty @ hdc28
root           (hd1,27)
chainloader    +1

title          Empty @ hdc29
root           (hd1,28)
chainloader    +1

title          Empty @ hdc30
root           (hd1,29)
chainloader    +1

title          rPath 0.99.2 @ hdc31
root           (hd1,30)
chainloader    +1

title          STX 1.0 rc2 @ hdc32
root           (hd1,31)

chainloader    +1

title          Fedora Core 5 @ hdc33
root           (hd1,32)
chainloader    +1

title          StartCom 4.0.4 Raam @ hdc34
root           (hd1,33)
chainloader    +1

title          Slackware 10.2 @ hdc35
root           (hd1,34)
chainloader    +1

title          Foresight Foresight 0.9 @ hdc36
root           (hd1,35)
kernel         /boot/vmlinuz-2.6.12.5-fdl.2.x86.i686.cmov ro root=/dev/hdc36 splash=silent vga=791  quiet
initrd         /boot/initrd-2.6.12.5-fdl.2.x86.i686.cmov.img

title          Xandros 3.0 @ hdc37
root           (hd1,36)
chainloader    +1

title          Ubuntu 5.10 Breezy Badger @ hdc38
root           (hd1,37)
chainloader    +1

title          Kate 2.2 (booted by Suse 10 Kernel in hdc43) @ hdc39
root           (hd1,38)
kernel         (hd0,42)/boot/vmlinuz ro root=/dev/hdc39
initrd         (hd0,42)/boot/initrd

# Partitions hdc40 to hdc54 are partitions each 200Mb for Grub working as submenus.

title          Grub menu for MS systems only (Dos & Windows) @ hdc40
root           (hd1,26)
chainloader    +1

title          Grub menu for recent additions @ hdc41
root           (hd1,40)
chainloader    +1

title          Grub menu for only small distros @ hdc42
root           (hd1,41)
chainloader    +1

title          Grub menu for only large distros @ hdc43

root           (hd1,42)
chainloader    +1

title          Grub reserved menu (Empty) @ hdc44
root           (hd1,43)
chainloader    +1

title          Grub menu for IDE disk hda only @ hdc45
root           (hd1,44)
chainloader    +1

title          Grub menu for IDE disk hdc only @ hdc46
root           (hd1,45)
chainloader    +1

title          Grub menu for Sata disk sda only @ hdc47
root           (hd1,46)
chainloader    +1

title          Grub menu for Sata disk sdb only @ hdc48
root           (hd1,47)
chainloader    +1

title          Complete menu for all 100+ systems @ hdc49
root           (hd1,48)
chainloader    +1

title          Master Menu to boot submenus @ hdc50
root           (hd1,49)
chainloader    +1

title          Grub reserved menu (Empty) @ hdc51
root           (hd1,50)
chainloader    +1

title          Grub reserved menu (Empty) @ hdc52
root           (hd1,51)
chainloader    +1

title          Grub reserved menu (Empty) @ hdc53
root           (hd1,52)
chainloader    +1

title          Grub reserved menu (Empty) @ hdc54
root           (hd1,53)
chainloader    +1

# Third disk sda is a Sata with 15 partitions, 9 are bootable

title          XP pro @ sdb1
hide           (hd0,0)
hide           (hd1,0)
hide           (hd1,1)
unhide         (hd2,0)
map            (hd2) (hd0)
map            (hd0) (hd2)
root           (hd2,0)
makeactive
chainloader    +1

title          Empty @ sda2
root           (hd2,1)
chainloader    +1

title          Empty @ sda3
root           (hd2,2)
chainloader    +1

# Extended partition here is the sdb4

title          Empty @ sda5
root           (hd2,4)
chainloader    +1

title          Ututu x2 2005.1 @ sda6
root           (hd2,5)
chainloader    +1

title          Helix 1.7 @ sda7
root           (hd2,6)
chainloader    +1

title          MagicLinux 2.0 rc2 @ sda8
root           (hd2,7)
chainloader    +1

title          Zenwalk 1.2 @ sda9
root           (hd2,8)
chainloader    +1

title          MedianLinux 4 rc5 @ sda10
root           (hd2,9)
chainloader    +1

title          NetBSD i386 3.0 rc6 @ sda11
root           (hd2,10)
chainloader    +1

title          Arabian 0.6 rc1 @ sda12
root           (hd2,11)
chainloader    +1

title          Mepis 3.3.2 @ sda13
root           (hd2,12)
chainloader    +1

# Persinal data partion @ sda14


title          Empty @ sda15
root           (hd2,14)
chainloader    +1

# Fourth disk sdb is a Sata with 15 partitions, 8 are bootable

title          Win2k @ sdb1
hide           (hd0,0)   # hiding DOS 6.22 partition in hda1
hide           (hd1,0)   # hiding DOS 7.10 partition in hdc1
hide           (hd1,1)   # hiding Win98    partition in hdc2
hide           (hd2,0)   # hiding Win XP   partition in sda1
unhide         (hd3,0) # unhide Win2k partition for execution
root           (hd3,0)
makeactive
map            (hd3) (hd0)
map            (hd0) (hd3)
chainloader    +1

title          FreeDOS @ sdb2
hide           (hd0,0)   # hiding DOS 6.22 partition in hda1
hide           (hd1,0)   # hiding DOS 7.10 partition in hdc1
hide           (hd1,1)   # hiding Win98    partition in hdc2
hide           (hd2,0)   # hiding Win XP   partition in sda1
hide           (hd3,0)   # hiding Win2k    partition in sdb1
unhide         (hd3,1)
root           (hd3,1)
makeactive
map            (hd3) (hd0)
map            (hd0) (hd3)
chainloader    +1

title          Empty @ sdb3
root           (hd3,4)
chainloader    +1

# Partition sdb4 is an extended partition

title          NetBSD 3.0 AMD64 @ sdb5
root           (hd3,4)
chainloader    +1

title          Empty @ sdb6
root           (hd3,5)
chainloader    +1

title          Empty @ sdb7
root           (hd3,6)
chainloader    +1

title          Frugalware 0.4 @ sdb8
root           (hd3,7)
chainloader    +1

title          Empty @ sdb9
root           (hd3,8)
chainloader    +1

title          Quantian 0.7.9.1 @ sdb10
root           (hd3,9)
chainloader    +1

title          Suse 10.1 x86 64 @ sdb11
root           (hd3,10)
chainloader    +1

title          Empty @ sdb12
root           (hd3,11)
chainloader    +1

title          Knoppix 4.0.2 @ sdb13
root           (hd3,12)
chainloader    +1

title          Mandriva Release 2006 @ sdb14
root           (hd3,13)
chainloader    +1

title          Empty @ sdb15
root           (hd3,14)
chainloader    +1