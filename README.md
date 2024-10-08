![Arch Linux Secure AF](./archLinux.png)
Wallpaper: [https://www.reddit.com/user/alienpirate5/](https://www.reddit.com/user/alienpirate5/)
## Awesome Arch Linux

This is a working guide on how to install Arch Linux with improved security which utilizes 
LUKS2 encrypted partition and how to set up Secure Boot and enroll TPM2. 
It is based on the awesome guides of @schm1d and @joelmathewthomas, 
big thanks for their work, the links are below.

My goal was to gather all the best things from them and to improve some outdated solutions.

***This implementation forces user to use a PIN to allow TPM to load the key.*** 


### Installation
First downaload Arch ISO [here](https://archlinux.org/download/)

#### Method 1
Boot the media on the target device you want install Arch linux.

If there is no git running, you can install it with:

    pacman -Syy && pacman -S git

Then on the live system do the following:

    git clone https://github.com/aulyxair/HAL.git
    cd HAL/base
    chmod +x *.sh
    ./archinstall.sh

#### Method 2
Boot the media on the target device you want install Arch linux.

Download the script on your machine.
Copy to a removable media and use it in the live system.

To run the base scripts on your target machine, all you need to do is:

1. Have both **archinstall.sh** and **chroot.sh** on the same directory.
2. chmod +x **archinstall.sh** and **chroot.sh**
3. Then run **archinstall.sh** like so: `./archinstall.sh`


[AwesomeArchLinux by @schm1d](https://github.com/schm1d/AwesomeArchLinux/)

[archinstall-luks2-lvm2-secureboot-tpm2 by @joelmathewthomas](https://github.com/joelmathewthomas/archinstall-luks2-lvm2-secureboot-tpm2)
