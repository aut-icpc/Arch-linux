# Arch-linux

## Introduction
For AUT-ICPC competitions of 2019, I provided an Archlinux iso image.
So here are some links and explanations for the journey of installing and configuring and having a live image in Archlinux.

![alt text](https://raw.githubusercontent.com/aut-icpc/Arch-linux/master/Arch-Xfce-icon2.png)
### Getting Started

A heads up from Archlinux website for starting([see by youself](https://wiki.archlinux.org/index.php/Frequently_asked_questions#Why_would_I_not_want_to_use_Arch?)):
```
You may not want to use Arch, if

- you require support for an architecture other than x86_64.
- you do not have the ability/time/desire for a 'do-it-yourself' GNU/Linux distribution.
- you believe an operating system should configure itself, run out of the box, and include a complete default
  set of software and desktop environment on the installation media.
```
> **General Tip**
- Whenever you got stuck in the procedures, Archwiki will be your saviour.

## Contents
- [Download Arch Iso](#download-arch-iso)
- [Installation](#installation)
- [Post-installation](#post-installation)
   - [Graphical user interface](#graphical-user-interface)
      - [Desktop environment](#desktop-environment)
- [Live Image](#live-image)

## Download Arch Iso
You can download Arch iso from [here](https://www.archlinux.org/download).

## Installation
For installing Arch, you can use the documents existing at [Archwiki](https://wiki.archlinux.org) or just watching tutorials at Youtube.

- [Installation Guide](https://wiki.archlinux.org/index.php/installation_guide) at Archwiki.
- Tutorials at Youtube:
  - [First tutorial](https://www.youtube.com/watch?v=DuX4ERxnrsY)
  - [Second tutorial](https://www.youtube.com/watch?v=lizdpoZj_vU&t=1475s)


> Tips
- For a fully functional base system, pay attention to the packages appended to the end of **pacstrap** command, otherwise you may end up having no _text editor_ or _network manager_.
for example:
 ```
 pacstrap /mnt base linux linux-firmware
 ```
- Set the system clock up to date, otherwise you may face some problems later.

## Post-installation
- Like setting up a **graphical user interface**, **sound** or a **touchpad**.
You can visit Archwiki for [General recommendations](https://wiki.archlinux.org/index.php/General_recommendations) after installation.
- For a list of applications that may be of interest, see [List of applications](https://wiki.archlinux.org/index.php/List_of_applications). 

### Graphical user interface
- Archwiki's documents on [GUI](https://wiki.archlinux.org/index.php/Category:Graphical_user_interfaces)

#### Desktop environment
For setting up a desktop environment and choosing the desktop itself, [Arcolinuxd website](https://arcolinuxd.com/7-the-actual-installation-of-arch-linux-phase-3) is a good source to go. 
- An example of installing Xfce on Arch(Of course you can install something else instead of Xfce):
```
pacman -S xorg-server xorg-apps xorg-xinit xterm
```
You need to install a display manager or a login manager. For example install **lightdm**.
We will install the desktop environment **Deepin** lateron. We do **not** need to install **line 2** now. Deepin has its own lightdm greeter.
```
pacman -S lightdm
pacman -S lightdm-gtk-greeter lightdm-gtk-greeter-settings
systemctl enable lightdm.service
```
- **Do not reboot until you have a desktop environment.**
- **Do not FORGET TO ENABLE Lightdm**.
Now choose your desktop([List of desktop environments](https://arcolinuxd.com/7-the-actual-installation-of-arch-linux-phase-3))!I go with Xfce now:
```
pacman -S xfce4
pacman -S xfce4-goodies
```
If you forget to activate the **lightdm.service** you will **never** be able to boot into the **graphical** environment. Of course you can fix it but I'm giving you the heads up! :)

## Live Image
In order to generate Arch images, you need to use Archiso.
> Archiso is a small set of bash scripts capable of building fully functional Arch Linux live CD/DVD/USB images.
- For installing Archiso use the following command:
```
pacman -S archiso
```
or
```
yaourt archiso-git
```
- [Archiso Documentation](https://wiki.archlinux.org/index.php/Archiso)
- A tutorial on 'How to use Archiso: Custom Arch Linux Build' at Youtube
   - [Part1](https://www.youtube.com/watch?v=y_Blo7hB8Ag)
   - [Part2](https://www.youtube.com/watch?v=y_Blo7hB8Ag)
