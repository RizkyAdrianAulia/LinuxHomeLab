# Ubuntu Server Installation

## Objective
Install and make sure Ubuntu Server is running on a VMWare (Virtual Machine)

## Requirement
1. Ubuntu Server 26.04 ISO
2. Virtual Machine (VMWare / Virtualbox)

## Installation Steps
1. Download Ubuntu Server ISO.
2. Create a new virtual machine.
3. Configure the specification of the server :
   RAM   : 4GB
   Disk  : 30GB
   CPU   : 2 Core
4. Choose the default ubuntu server installation and click next.
5. Check the disk information and click next.
6. Configure the device name, server name and password.
7. Do the installation and wait until its done.
8. Login into the server.

## Validate Installation
1. Try to check updates for the server. Use "sudo apt update" and if there is an update, run "sudo apt upgrade".
2. Check hostname using "hostname" command.
3. Set date and time to your are using "timedatectl set-timezone area" command. Check the datetime using "date" command.
