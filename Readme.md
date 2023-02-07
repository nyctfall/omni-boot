# OminBoot - GRUB Multiboot ISO Config

This is a project to help make a single USB stick that can hold multiple ISOs!

It uses GRUB as its bootloader, so it works natively with Linux, FreeBSD, NetBSD, and OpenBSD. And it can boot Windows and MacOS by using bootloader chainloading.


## Install:


#### For Linux:

First follow the instructions in the [Multiboot USB Wiki](https://wiki.archlinux.org/title/Multiboot_USB_drive).

Then use the contents of the `grub.cfg` in this project as the [manual configuration](https://wiki.archlinux.org/title/Multiboot_USB_drive#Manual_configuration) in the GRUB directory.


## Need For Contributions:

- [ ] OpenBSD Testing

Right now I can't do much bare metal testing of OpenBSD, as it cannot use any NVIDIA GPUs made after the GTX 200-series (Tesla architecture) from 2009. And since I only have a newer NVIDIA GPU, I can't test any graphics display issues.

Anyone with an old NVIDIA GPU or any AMD GPU/APU or Intel GPU/iGPU should feel free to do more testing with it.

- [ ] GNU Guix Debugging

GNU Guix is not booting properly, likely due to an incorrectly configured ISO path in the kernel boot arguments, or even entirely missing kernel arguments that I don't know about.

I haven't had much time to test Guix to see what the problem is, so any suggestions from anyone who's familiar with Guix would be a huge help.


## Testing

I usually test the GRUB configs by booting them on bare metal (my physical PC) to make sure all the USB drives (or SD cards) work.
But it's also possible to use VirtualBox (or another virtual machine hypervisor) to test just the GRUB configs.

On Linux (and possibly also WSL) some testing can be done using the `grub-emu` package to emulate GRUB in a terminal. But I've found it to be buggy, and the older  versions I've used have a terminal interface that's very cumbersome and inconvenient. So your mileage may vary.


---


##  Useful References & Other Projects
 - [GNU GRUB  Manual](https://www.gnu.org/software/grub/manual/grub/grub.html)
 - [Ubuntu Linux Wiki - GRUB](https://help.ubuntu.com/community/Grub2)
 - [Ubuntu Linux Wiki - GRUB ISO Booting](https://help.ubuntu.com/community/Grub2/ISOBoot)
 - [Ubuntu Linux Wiki - GRUB ISO Booting (Examples)](https://help.ubuntu.com/community/Grub2/ISOBoot/Examples)
 - [Arch Linux Wiki - GRUB](https://wiki.archlinux.org/title/GRUB)
 - [Arch Linux Wiki - GRUB Tips & Tricks](https://wiki.archlinux.org/title/GRUB/Tips_and_tricks)
 - [Arch Linux Wiki - Multiboot USB](https://wiki.archlinux.org/title/Multiboot_USB_drive)
 - [MBUSB Multiboot USB - GitHub](https://github.com/mbusb/multibootusb)
 - [Live USB Build - GitHub](https://github.com/mytbk/liveusb-builder)
