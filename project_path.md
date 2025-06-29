# The detailed project path  

## Project name => thinkfan Debian Buster 12.11

## Project target

## This repository shows how to use the utility  thinkfan [![Alt-Text][1]](https://github.com/vmatare/thinkfanl). The approach is described using the example of the Debian 12.10 operating system and Lenovo hardware typ ThinkCentre M92P

## Project start date

```bash <!-- markdownlint-disable-line code-block-style -->
$ date
Sun Jun 29 02:34:05 PM CEST 2025
```

## Hardware

###
<!--- THis empty line inside the block is necessary for correct format -->
```bash<!-- markdownlint-disable-line code-block-style -->
hostnamectl 
 Static hostname: debian
       Icon name: computer-desktop
         Chassis: desktop 🖥️
      Machine ID: ######
         Boot ID: ######
         Operating System: Debian GNU/Linux 12 (bookworm)  
          Kernel: Linux 6.1.0-37-amd64
    Architecture: x86-64
 Hardware Vendor: Lenovo
  Hardware Model: ThinkCentre M92P
Firmware Version: 9SKT58AUS
```
<!--- THis empty line inside the block is necessary for correct format -->
### Install How do install lshw  on debian [![alt text][1]](https://www.tecmint.com/commands-to-collect-system-and-hardware-information-in-linux/)
<!--- THis empty line inside the block is necessary for correct format -->
```bash<!-- markdownlint-disable-line code-block-style -->
sudo apt update
sudo apt install lshw
```
<!--- THis empty line inside the block is necessary for correct format -->
### Used

<!--- THis empty line inside the block is necessary for correct format -->
```bash<!-- markdownlint-disable-line code-block-style -->
        sudo lshw -class cpu -class memory
        [sudo] password for trapapa:
        *-cpu
            description: CPU
            product: Intel(R) Core(TM) i5-3470 CPU @ 3.20GHz
            vendor: Intel Corp.
            physical id: 42
            bus info: cpu@0
            version: 6.58.9
            slot: SOCKET 0
            size: 2836MHz
            capacity: 3800MHz
            width: 64 bits
            #truncated
        *-memory
        description: System Memory
        physical id: 41
        slot: System board or motherboard
        size: 16GiB
        #truncated
```
><!--- THis empty line inside the block is necessary for correct format -->
### OS-Version - cat /etc/os-release
<!-- Required to comply with the Markdownlint specification -->
```bash
cat /etc/os-release 
PRETTY_NAME="Debian GNU/Linux 12 (bookworm)"
NAME="Debian GNU/Linux"
VERSION_ID="12"
VERSION="12 (bookworm)"
VERSION_CODENAME=bookworm
ID=debian
HOME_URL="https://www.debian.org/"
SUPPORT_URL="https://www.debian.org/support"
BUG_REPORT_URL="https://bugs.debian.org/"
```
<!-- Required to comply with the Markdownlint specification -->
### Point Releases - Those updates are called "Point Releases" [![alt text][1]](https://wiki.debian.org/DebianReleases/PointReleases)
<!-- Required to comply with the Markdownlint specification -->
```bash
> cat /etc/debian_version
12.11
```
<!-- Required to comply with the Markdownlint specification -->
## OS-Version - uname -a

```bash <!-- markdownlint-disable-line code-block-style -->
$ uname -a
Linux debian 6.1.0-28-amd64 #1 SMP PREEMPT_DYNAMIC Debian 6.1.119-1 (2024-11-22) x86_64 GNU/Linux
```

## IDE used for the project - MS Visual Studio Code
<!--- THis empty line inside the block is necessary for correct format -->
```text
Version: 1.100.2
Commit: 848b80aeb52026648a8ff9f7c45a9b0a80641e2e
Date: 2025-05-14T21:47:40.416Z
Electron: 34.5.1
ElectronBuildId: 11369351
Chromium: 132.0.6834.210
Node.js: 20.19.0
V8: 13.2.152.41-electron.0
OS: Linux x64 6.1.0-34-
```
<!--- THis empty line inside the block is necessary for correct format -->
>[!NOTE]
> Manual page **curl** [![alt text][1]](https://linux.die.net/man/1/curl)
>
> Manual page **wget** [![alt text][1]](https://linux.die.net/man/1/wget)
>
<!--- THis empty line inside the block is necessary for correct format -->
>[!NOTE]
>Different between the utilities ``curl`` vs ``wget`` [![alt text][1]](https://daniel.haxx.se/docs/curl-vs-wget.html)
<!--- THis empty line inside the block is necessary for correct format -->
<!-- FIXIT sudo apt-get update vs upgrade – What is the Difference https://www.freecodecamp.org/news/sudo-apt-get-update-vs-upgrade-what-is-the-difference/ -->
<!-- TODO check is a package already installed in the latest stable version>
<!-- TODO Find daily Use Case for a PC Computer-->
<!-- TODO hOW enable thinkfan now on debian -->
<!-- TODO Docker/Podman image for compile optimize gcc scache -->
<!-- TODO user less scache command without editor-->
<!-- TODO best optimize version for gcc depend of cpu mem io -->
<!-- TODO count intration of program / debug >
## Used compiler
<!--- THis empty line inside the block is necessary for correct format -->
```bash
gcc --version
gcc (Debian 12.2.0-14+deb12u1) 12.2.0
Copyright (C) 2022 Free Software Foundation, Inc.
This is free software; see the source for copying conditions.  There is NO
warranty; not even for MERCHANTABILITY or FITNESS FOR A PARTICULAR PURPOSE.
```
<!--- THis empty line inside the block is necessary for correct format -->
## Install & update necessary package [![alt text][1]](https://manpages.ubuntu.com/manpages/xenial/man8/apt.8.html)
<!--- THis empty line inside the block is necessary for correct format -->
```bash
sudo -i # make user to root
apt update # fetches the latest version of the package list from your distro's software repository
apt upgrade # upgrade is used to install available upgrades of all packages currently installed on the system from the sources configured via sources.list
apt install -y cmake-curses-gui
apt install -y build-essential
apt install -y cmake
apt install -y g++
apt install -y libyaml-cpp-dev
apt install -y libyaml-cpp-dev pkgconfig
apt install -y libyaml-cpp-dev pkg-config
apt install -y libsensors-dev


```

>[!TIP]
<!--- THis empty line inside the block is necessary for correct format -->
>- Download Link symbol via wget [![alt text][1]](https://askubuntu.com/questions/207265/how-to-download-a-file-from-a-website-via-terminal) man page [![alt text][1]](https://linux.die.net/man/1/wget)
>- Command option wget
>   -P ``<dir>``  **UPPER LETTER**  
>   --page-requisites  
>   This option causes Wget to download all the files that are necessary to properly display a given HTML page. This includes such things as inlined images, sounds, and referenced stylesheets
<!--- THis empty line inside the block is necessary for correct format -->
>## Command to create folder and download via bash shell
<!--- THis empty line inside the block is necessary for correct format -->
>```bash
>mkdir -p img && wget  -P img/ "https://raw.githubusercontent.com/MathiasStadler/link_symbol_svg/>360d1327d05280d53de5fa816c522f89a35891ca/img/link_symbol.svg"
>```
<!--- THis empty line inside the block is necessary for correct format -->
<!-- Link sign - Don't Found a better way :-( - You know a better method? - send me a email -->
[1]: ./img/link_symbol.svg
