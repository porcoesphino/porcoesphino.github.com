### Installing Ubuntu on on a Macbook Air using a USB drive

I had a bit of fun with this. I started off playing with some things through virtual box and figured I could mount a partition in there, clone it with the current drive, play with the bootloader and be done. That may have worked out if I didn't find [this great post][], decide that most of my things are on the cloud and most of the installation would happen while I was sleeping.

Problems I found
 - It's annoying and hard to set up a bootable USB
    - It seems like you need [rEFIt][]/[rEFInd][]/[Grub 2][]
    - [The instructions Ubuntu provides][] didn't work for me
     - It wasn't recognised at all even before the reboot
        - I assume user error

Basic steps:
 - Download the [64-bit Mac (AMD64) desktop image][]
    - Yes, you read right _Mac_ image from Ubuntu
 - Install [rEFIt][]
    - Unmaintained: They recommend [rEFInd][])
 - Partition
    - Leave around one Gb for SWAP
 - Make your bootable USB
    - Use the [64-bit Mac (AMD64) desktop image][]
    - Use [UNetbootin for Mac][]
       - Don't select distribution
 - Reboot into [rEFIt][]/[rEFInd][]/[Grub 2][]
    - Apparently it's normal to need to reboot multiple times or reinstall. I'd love to know why.
    - Click the penguin
 - Install
    - **Installation Type:** ***Something Else***
    - Choose swap partition
    - Choose main partition (Ext4)
       - Mountable with [MacFuse][] and [Fuse-Ext2][]
    - **Booloader:** ***The above partition***

[this great post]: http://www.thatsthewayyoudoit.me/2013/04/how-to-install-ubuntu-1304-on-macbook.html
[rEFIt]:	http://refit.sourceforge.net/doc/c1s1_install.html
[rEFInd]:	http://www.rodsbooks.com/refind/
[Grub 2]:	http://www.ploxiln.net/wiki/dual-booting_linux_on_x86_64_macbooks
[The instructions Ubuntu provides]:	http://www.ubuntu.com/download/desktop/create-a-usb-stick-on-mac-osx
[64-bit Mac (AMD64) desktop image]:	http://releases.ubuntu.com/13.04/
[UNetbootin for Mac]:	http://unetbootin.sourceforge.net/
[MacFuse]:	https://code.google.com/p/macfuse/
[Fuse-Ext2]:	http://sourceforge.net/projects/fuse-ext2/
