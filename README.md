raspberry_pi
============
I need help remembering what to do after I set up a raspberry pi.

### Required Setup
1. Hardware - what hardware do I need
2. Raspbian OS - how to install the OS for the pi
3. SSH (Remote Connection) - how to setup a remote connection to the pi

### Optional Setup
todo


Table of Contents
-----------------
1. [Hardware](#Hardware)
2. [Raspbian OS](#Raspbian)
3. [SSH (Remote Connection)](#SSH)


<a name="Hardware"/>

Hardware
--------
I'd recommend one starter kit so that you can set up SSH and network/wifi more easily. It should include:
- x1 Raspberry Pi
- x1 Power Supply
- x1 HDMI cable
- x1 SD card
- x1 SD card to USB reader

Additionally you should already have:
- x1 Keyboard
- x1 Mouse

<a name="Raspbian"/>

Raspbian OS
-----------
Typically you can just insert the SD card into the pi and image it when you turn on the pi, but I ran into issues with corruption / failure to start.
Highly recommend using [Raspberry Pi Imager](https://www.raspberrypi.com/software/) but you can use any OS imaging software that floats your boat.
For beginners, I'd recommend using the desktop image, but if you know what you're doing and just need a terminal, install the OS lite image.

<a name="SSH"/>

SSH (Remote Connection)
-----------------------
Setup a remote connection to the raspberry pi.

1. Run updates
`sudo apt-get update`

2. Start the SSH server
`sudo raspi-config` -> Interface Options -> SSH -> enable

3. From your main computer or laptop you want to connect to the raspberry pi, you should be on the same wifi or network. Then you can run:
`ssh <username>@<domain.local>` for me, this is `ssh richard@richardpi.local`

ZSH Shell
---------
Upgrade the raspberry pi shell.

1. Install ZSH
`sudo apt-get install zsh`

2. Install 'oh my zsh'
`sh -c "$(wget https://raw.githubusercontent.com/ohmyzsh/ohmyzsh/master/tools/install.sh -O -)"`



