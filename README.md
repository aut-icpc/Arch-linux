# Archlinux

## Introduction
For AUT-ICPC competitions of 2019, an Archlinux iso image was provided. 
So here are some links and explanations for the journey of installing and configuring and having a live image in Archlinux.

## Getting Started

At first I quote some sort of advise from [Archlinux website](https://www.archlinux.org):
```
**You may not want to use Arch, if**

- you do not have the ability/time/desire for a __'do-it-yourself'__ GNU/Linux distribution.
- you require support for an architecture other than **x86_64**.
- you believe an operating system should configure itself, run out of the box, and include a complete default set of software and desktop environment on the installation media.
```
[See by youself](https://wiki.archlinux.org/index.php/Frequently_asked_questions#Why_would_I_not_want_to_use_Arch?)

## Contents
- [Download Arch](#download archlinux iso)
- [Installation](#intallation)
- [Post-installation](#post-installation)
- [Live Image](#live image)

## Download Archlinux Iso
You can download Arch iso from [here](https://www.archlinux.org/download).

## Installation
For installing Arch, you can use the documents existing at [Archwiki](https://wiki.archlinux.org) or just watching tutorials at Youtube.

- [Installation guide](https://wiki.archlinux.org/index.php/installation_guide) at Archwiki.
- Tutorials at Youtube:
 - [first tutorial](https://www.youtube.com/watch?v=DuX4ERxnrsY)
 - [second tutorial](https://www.youtube.com/watch?v=lizdpoZj_vU&t=1475s)

> Tips
- For a fully functional base system, pay attention to the packages that you append to the _pacstrap_ command otherwise you may end up having no _text editor_ or _network manager_. for example:
`pacstrap /mnt base linux linux-firmware`
- Set the system clock up to date. Otherwise you may face some problems later.

## Post-installation
Like setting up a **graphical user interface**, **sound** or a **touchpad**.
You can visit Archwiki for [General recommendations](https://wiki.archlinux.org/index.php/General_recommendations) after installation.
For a list of applications that may be of interest, see [List of applications](https://wiki.archlinux.org/index.php/List_of_applications). 

### Graphical user interface


## Live Image




> **General Tip**
- 