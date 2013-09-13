The `lsmod` range of tools has been replaced with:
 - kextutil, kextstat, kextload, kextunload

[kextunload](https://developer.apple.com/library/mac/#documentation/Darwin/Reference/Manpages/man8/kextunload.8.html) can use full Kernel Extension path, like kextload.
	sudo kextunload /System/Library/Extensions/msdosfs.kext
Or the bundle identifier, as listed by kextstat:
	sudo kextunload -b com.apple.filesystems.msdosfs

ioreg -c IOUSBDevice -l -w 0
