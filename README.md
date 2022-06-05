# UPDATE: My development MBL which died is back alive
During kernel 5.4 Asynchronuous DMA driver work, my MBL died over 18 months ago.  Apperently u-boot and/or u-boot variables were corrupted.  In a nothing-to-lose-effort, I managed to unsolder a chip and reflash it.

# My-Book-Live (MBL) customization
Kernel patches and Debian release for Western Digital My Book Live.</br>
__NOTE__: these customizations will void your warranty and are delivered on best-effort only</br>
__NOTE__: while the posted methods allow you to fully customize a MBL without ever opening it, you need to keep in mind that there might be a failure which requires you to ultimately open up the shell.</br> 
__NOTE__: none of this work is tested on a My Book Live DUO for the simple reason that we don't own one. That said it, community members have successfully deployed on MBL Duo.</br>
  
## Why customize ? ##

- __My disk died__: in this scenario, you may have to open up your MBL if your warranty is void and you will be exposed to the "complexity" of Linux commands/shell scripts, formatting, u-boot, etc.   It's a good time to explore all the possibilities. 
- __Supportability__: original firmware comes with Debian Lenny (5.0.x), which was released in February 2009.  Security and other updates have been discontinued as of February 2012.  While Western Digital has done a great job to provide updated firmware, it's ultimately impossible to keep up with back-porting vulnerability updates on pre-2010, outdated releases.
- __Security vulnerabilities__: protect your valuable data (see [report](https://techrevelations.de/2018/07/28/sorry-your-nas-is-not-safe-anymore/))
- __Performance__: custom kernels can increase your performance by 50%+
- __Functionality__: many new packages are no longer supported on 2.6 kernels and Debian Jessie (e.g. newer versions of Samba with better Windows 10 support)

## Why not customize ? ##
- Losing WD support/warranty
- Loss of the graphical user interface: while it's possible to port the original web user interface, it's not really worth it the time and effort.

## Tree Structure ##

* __debian__: Debian 8.11 with security patches backported to PowerPC
* __kernel__: Kernel patches, pre-compiled kernels and device tree structure
* __samba__ : Optimal perfomance with Samba using sample config files
* __uboot__ : Netconsole support, u-boot boot files, TFTP boot and ways to safely boot My Book Live

Documentation is posted within each section.

## Latest validated kernel support ##
* Kernel 2.6.32.71, released Sat, 12 Mar 2016<br>
* Kernel 4.9.169, released Wed, 17 Apr 2019<br>
* Kernel 4.19.99, released Mon, 27 Jan 2020


## What is new ? ##
* __4.19 kernel (pre-compiled and patches) released__
* high performance kernel 4.19.99 released
* patches updated for 4.19.99
* section on Samba
* section on cross-compiling kernels
* fixed a few Github postng issues
* released 4.9.149 & 4.9.169
* support for TFTP booting including netconsole support
* initramfs section
* improved section on installing custom kernels on original firmware
* update on Debian sources.list (package repositories)

## Known issues ##
* (Disk activity) led not working on 4.19 kernels 
