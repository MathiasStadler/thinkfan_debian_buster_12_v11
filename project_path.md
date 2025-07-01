# The detailed project path  
<!--- THis empty line inside the block is necessary for correct format -->
## Project name => thinkfan Debian Buster 12.11
<!--- THis empty line inside the block is necessary for correct format -->
## Project target
<!--- THis empty line inside the block is necessary for correct format -->
## This repository shows how to use the utility  thinkfan [![Alt-Text][1]](https://github.com/vmatare/thinkfanl). The approach is described using the example of the Debian 12.10 operating system and Lenovo hardware typ ThinkCentre M92P
<!--- THis empty line inside the block is necessary for correct format -->
## Project start date
<!--- THis empty line inside the block is necessary for correct format -->
```bash <!-- markdownlint-disable-line code-block-style -->
$ date
Sun Jun 29 02:34:05 PM CEST 2025
```
<!--- THis empty line inside the block is necessary for correct format -->
## Hardware
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
### How do install lshw  on debian [![alt text][1]](https://www.tecmint.com/commands-to-collect-system-and-hardware-information-in-linux/)
<!--- THis empty line inside the block is necessary for correct format -->
```bash<!-- markdownlint-disable-line code-block-style -->
sudo apt update
sudo apt install lshw
```
<!--- THis empty line inside the block is necessary for correct format -->
### Used hardware
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
<!--- THis empty line inside the block is necessary for correct format -->
```bash <!-- markdownlint-disable-line code-block-style -->
$ uname -a
Linux debian 6.1.0-28-amd64 #1 SMP PREEMPT_DYNAMIC Debian 6.1.119-1 (2024-11-22) x86_64 GNU/Linux
```
<!--- THis empty line inside the block is necessary for correct format -->
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
> Manual page ``curl`` [![alt text][1]](https://linux.die.net/man/1/curl)
>
> Manual page ``wget`` [![alt text][1]](https://linux.die.net/man/1/wget)
>
<!--- THis empty line inside the block is necessary for correct format -->
>[!NOTE]
>Different between the utilities ``curl`` vs ``wget`` [![alt text][1]](https://daniel.haxx.se/docs/curl-vs-wget.html)
<!--- THis empty line inside the block is necessary for correct format -->
<!-- FIXIT sudo apt-get update vs upgrade – What is the Difference https://www.freecodecamp.org/news/sudo-apt-get-update-vs-upgrade-what-is-the-difference/ -->
<!-- [ ] check is a package already installed in the latest stable version>
<!-- [x] done-->
<!-- TODO Find daily Use Case for a PC Computer-->
<!-- TODO hOW enable thinkfan now on debian -->
<!-- TODO Docker/Podman image for compile optimize gcc scache -->
<!-- TODO user less scache command without editor-->
<!-- TODO best optimize flags version for gcc depend of cpu mem io -->
<!-- TODO count inaction of program / debug -->
## Used compiler and tools

### gcc
<!--- THis empty line inside the block is necessary for correct format -->
```bash
gcc --version
gcc (Debian 12.2.0-14+deb12u1) 12.2.0
Copyright (C) 2022 Free Software Foundation, Inc.
This is free software; see the source for copying conditions.  There is NO
warranty; not even for MERCHANTABILITY or FITNESS FOR A PARTICULAR PURPOSE.
```
<!--- THis empty line inside the block is necessary for correct format -->
### cmake
<!--- THis empty line inside the block is necessary for correct format -->
```bash
cmake --version
cmake version 3.25.1

CMake suite maintained and supported by Kitware (kitware.com/cmake)
```
<!--- THis empty line inside the block is necessary for correct format -->

<!--- THis empty line inside the block is necessary for correct format -->
>[!TIP]
>TL;DR: What is the Set Command in Linux? [![alt text][1]](https://ioflood.com/blog/set-linux-command/)
>>The set command in Linux is a built-in shell command used to set or unset
>>values of shell options and positional parameters. The basic use syntax is,
>>set [options] [arguments]. It’s like a master control panel
>>for your shell environment.
><!--- THis empty line inside the block is necessary for correct format -->
<!--- THis empty line inside the block is necessary for correct format -->
>[!TIP]
> set command options [![alt text][1]](https://www.gnu.org/software/bash/manual/html_node/The-Set-Builtin.html)
>
>```set -euxo pipefail```  
>> set -> Modifying Shell Behavior  
>> -e ->  Exit immediately if a pipeline,
>> which may consist of a single simple command
>> -u ->
>> -x ->  
>>>Print a trace of simple commands, for commands,
>>> case commands, select commands, and arithmetic for >> >>>commands and their arguments or associated word lists >>>after >>they are expanded and before they are executed. >>>The value >>of the PS4 variable is expanded and the >>>resultant value is >>printed before the command and its >>>expanded arguments.
>> -o -> Set the option corresponding to option-name  
>> pipefail -> If set, the return value of a pipeline
>> is the value of the last (rightmost) command to exit with >>a non-zero status, or zero if all commands in the pipeline >>exit successfully. This option is disabled by default.
>
<!--- THis empty line inside the block is necessary for correct format -->
>[!TIP]
>How To Use set and pipefail in Bash Scripts on Linux/Debian [![alt text][1]](https://www.howtogeek.com/782514/how-to-use-set-and-pipefail-in-bash-scripts-on-linux/)  
>>Using the example of installing the package build-essential  
>>see below

<!--- THis empty line inside the block is necessary for correct format -->
<!-- FIXIT https://www.gnu.org/software/bash/manual/html_node/The-Set-Builtin.html -->
><!--- THis empty line inside the block is necessary for correct format -->
>```bash
>#!/bin/bash
>set -euxo pipefail
>```
<!--- THis empty line inside the block is necessary for correct format -->
>[!TIP]
>How to see contents of a .deb Debian / Ubuntu package file [![alt text][1]](https://www.cyberciti.biz/faq/view-contents-of-deb-file/)
><!--- THis empty line inside the block is necessary for correct format -->
>```bash
>set -euxo pipefail && \
>#install/update && \
>sudo apt-get --yes update && \
>sudo apt-get install --yes apt-file && \
>#Updating APT database && \
>sudo apt-file update && \
>#List contents Of a Debian .deb File / Package && \
>#apt-file list packageName && \
>sudo apt-file list build-essential && \
>#change to /tmp folder && \
>cd /tmp
>```
<!--- THis empty line inside the block is necessary for correct format -->
### build-essential [![alt text][1]](https://itsfoss.com/build-essential-ubuntu/)
<!--- THis empty line inside the block is necessary for correct format -->
#### Contains a list of essential packages
<!--- THis empty line inside the block is necessary for correct format -->
```bash
This list was generated on Sun 03 Jan 2021 11:30:56 AM CET for amd64
It contains a list of essential packages (which are also build-essential).

base-files
base-passwd
bash
bsdutils
coreutils
dash
debianutils
diffutils
dpkg
findutils
grep
gzip
hostname
init-system-helpers
libc-bin
login
ncurses-base
ncurses-bin
perl-base
sed
sysvinit-utils
tar
util-linux
```
<!--- This empty line inside the block is necessary for correct format -->
>[!TIP]
>Obtain root shell [![alt text][1]](https://www.cyberciti.biz/faq/how-to-install-and-configure-sudo-on-debian-linux/)  
>sudo -i [![alt text][1]](https://unix.stackexchange.com/questions/106663/how-to-run-a-command-that-involves-redirecting-or-piping-with-sudo)
>>The -i (simulate initial login) option runs the shell
>>specified by the password database entry of the target user
>>as a login shell.  This means that login-specific resource
>>files such as .profile or .login will be read by the shell.
>>If a command is specified, it is passed to the shell for
>>execution via the shell's -c option.  If no command is
>>specified, an interactive shell is executed.
><!--- THis empty line inside the block is necessary for correct format -->
>```bash
>sudo -s
>## OR ##
>sudo -i
>```
><!--- THis empty line inside the block is necessary for correct format -->
<!--- THis empty line inside the block is necessary for correct format -->
## Install and update described and additionally packages [![alt text][1]](https://manpages.ubuntu.com/manpages/xenial/man8/apt.8.html)
<!--- THis empty line inside the block is necessary for correct format -->
```bash
echo "# Step 1 => Change to /tmp folder" && \
cd /tmp && \
echo "# Step 2 => Obtain root shell" && \
sudo -i
# next step  inside root shell
echo "# Step 3 => update/upgrade" && \
set -euxo pipefail && \
echo "# fetches the latest version of the package" && \
echo "list from your distro's software repository" && \
apt update && \ 
echo "# apt upgrade - is used to install available upgrades " && \
echo "of all packages currently installed on the system from " && \
echo "the sources configured via sources.list" && \ 
apt upgrade -y && \
echo "# Step 4 => install packages" && \
apt install -y build-essential && \
apt install -y cmake && \
apt install -y cmake-curses-gui && \
apt install -y g++ && \
apt install -y libsensors-dev && \
apt install -y libyaml-cpp-dev && \
apt install -y pkg-config && \
echo $?

```
<!--- THis empty line inside the block is necessary for correct format -->
## Create a folder for this project
<!--- THis empty line inside the block is necessary for correct format -->
```bash

```
<!--- THis empty line inside the block is necessary for correct format -->
## Fetch project from GitHub [![Alt-Text][1]](https://github.com/vmatare/thinkfanl)

>[!TIP]
><!--- THis empty line inside the block is necessary for correct format -->
>- Download Link symbol via wget [![alt text][1]](https://askubuntu.com/questions/207265/how-to-download-a-file-from-a-website-via-terminal) man page [![alt text][1]](https://linux.die.net/man/1/wget)
>- Command option wget
>   -P ``<dir>``  **P as UPPER LETTER**  
>   --page-requisites  
>   This option causes ``wget`` to download all the files that are necessary to properly display a given HTML page. This includes such things as inlined images, sounds, and referenced stylesheets
<!--- THis empty line inside the block is necessary for correct format -->
>## Command to create folder and download via bash shell
<!--- THis empty line inside the block is necessary for correct format -->
>```bash
>mkdir -p img && wget  -P img/ "https://raw.githubusercontent.com/MathiasStadler/link_symbol_svg/>360d1327d05280d53de5fa816c522f89a35891ca/img/link_symbol.svg"
>```
<!--- THis empty line inside the block is necessary for correct format -->
<!-- Link sign - Don't Found a better way :-( - You know a better method? - send me a email -->
[1]: ./img/link_symbol.svg
