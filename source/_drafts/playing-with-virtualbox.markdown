* aptitude isn't installed in ubuntu by default so use that (even if it's installed in the server addition

Caveeats:
* If installing from dodgy internet connection be sure to run these again:
* sudo apt-get update
* sudo apt-get install virtualbox-guest-x11
This can cause "Ubuntu is running in Low Graphics mode."

Ensure to install extras pack

VBoxManage list usbhost

tail -f /var/log/system.log | grep USB

sudo dmesg

sudo dseditgroup -o edit -a yourusername -t user operator
    $ sudo chmod 666 /dev/disk1*

    $ VBoxManage internalcommands createrawvmdk -filename ~/vm/dev-disk1.vmdk -rawdisk /dev/disk2 -partitions 1
    RAW host disk access VMDK file /Users/yourusername/vm/dev-disk1.vmdk created successfully.
    $ chmod 777 ~/vm/dev-disk1*
    $ ls ~/vm/
    dev-disk1-pt.vmdk  dev-disk1.vmdk
