---
title: Installing Streamer.bot on Linux
description: Information on how to install Streamer.bot on Linux including prequisites
published: true
date: 2021-12-12T06:03:27.854Z
tags: linux, install, how to
editor: markdown
dateCreated: 2021-11-23T00:46:04.543Z
---

# Installing Streamer.bot on Linux (Ubuntu/Arch)

This page will show you what you need to do in order to install Streamer.bot on an Ubuntu install or an Arch based linux install.

> Pop OS! is Ubuntu / Debian based so please follow the Ubuntu Install Steps in this guide  
{.is-info}

## Prerequisites that need to be installed:
- Wine v6.19 or newer
- Winetricks version 20210206 or newer 
- Curl (Ubuntu only)
- and finally Git

### Installing Wine v6.19 or newer 

**Ubuntu**  - So from the desktop you need to open up a terminal window or press <kbd>Ctrl + Alt + T</kbd> and enter the following to install wine 

  `sudo dpkg --add-architecture i386` - enable the 32bit architecture
  
  `wget -nc https://dl.winehq.org/wine-builds/winehq.key` - imports the repository key 
  	
  `sudo apt-key add winehq.key` - adds the key to the repository checker 


 Find the version of Ubuntu you're running.  *Note: Streamer.Bot only has been evaluated on Ubuntu 20.04.3 LTS*, once you have found the version you’re running. You'll need to run the command next to your version of Ubuntu to add the repository to your own repository list and press <kbd>Enter</kbd>.   


> 
> Ubuntu 21.10 - *`sudo add-apt-repository 'deb https://dl.winehq.org/wine-builds/ubuntu/ impish main'`*
> 
> Ubuntu 21.04 - *`sudo add-apt-repository 'deb https://dl.winehq.org/wine-builds/ubuntu/ hirsute main'`*
> 
> Ubuntu 20.10 - *`sudo add-apt-repository 'deb https://dl.winehq.org/wine-builds/ubuntu/ groovy main'`*
> 
> Ubuntu 20.04 - *`sudo add-apt-repository 'deb https://dl.winehq.org/wine-builds/ubuntu/ focal main'`*
{.is-info}



Once complete it's good practice to update the repository cache on your system to do this you need to run 
	`sudo apt update` 

Now for the installing of Wine part at this time of writing 
- v6.0.2 – stable 
- v6.23 - staging

`sudo apt install --install-recommends winehq-staging` and then press enter Y. Wait for this to complete. 

Congratulations you have just installed Wine to verify what version you're running type in the terminal window  `wine --version` to verify what version you’re running. 

**Arch Linux:** So for all of those on Arch Linux it nice and easy from your desktop open up a terminal  <kbd>Ctrl + Alt + T</kbd> and type the following commands 
> pacman is the default package handler built in to Arch Linux but yay and pacman use the same parameters. You can install yay if you want but it not required for this. 
{.is-info}

`pacman-S wine` or `yay -S wine`  and then press <kbd> Enter </kbd>

A prompt for the sudo(root) user password will appear enter your password and press y to go ahead with install, then sit back wait for the install process to complete and you’re done.  


![wine_install_.png](/linux-screenshots/wine_install_.png){.align-center}


### Winetricks version 20210206 or newer 

**Ubuntu Users** Next we need to install winetricks.  In the terminal window type - `sudo apt-get install winetricks` then press <kbd>Enter</kbd> 

![winestricks.png](/linux-screenshots/winestricks.png){.align-center}

This will install winetricks the latest version available on the offical Ubuntu repository list this will do for now as we will install the latest version from the developers after. Once installed you will need to use this command `sudo winetricks --self-update` hit the <kbd>Enter</kbd> and press y to continue. This installs the latest version released by winetricks developers.

![selfupdatewinetricks.png](/linux-screenshots/selfupdatewinetricks.png){.align-center}

Leave the install complete and you're on the latest version of winetricks. you can verify this by typing in the `winetricks --version` this will display what version of winetrick is installed.

### Curl
**Ubuntu users:** You'll need to install curl. 

so the CURL is needed for the install script to run but all you need to do is simply open a terminal window and type `sudo apt install curl` and then press <kbd> Enter </kbd> 

**Arch Linux** users shouldn’t need to install this. 

### GIT
The Git command is also needed to be installed because we need to clone the repository from GitHub. To install on this, follow the steps below: 

**Ubuntu Users** - In the terminal window type the following command in.

`sudo apt install git` and then press <kbd> Enter</kbd> and when prompted press Y then <kbd> Enter</kbd> again to install 

![git_install.png](/linux-screenshots/git_install.png){.align-center}

Congratulations your now ready to install Streamer.Bot on your machine 

**Arch Linux Users** - In the terminal window type the following command in.

`pacman -S git` or `yay -S git` and then press <kbd> Enter</kbd>  and when prompted press Y then <kbd> Enter</kbd> again to install.

![git_install_.png](/linux-screenshots/git_install_.png){.align-center}

Congratulations your now ready to install Streamer.Bot on your machine 

## Installing Streamer.bot with the script on to your Linux install. 

>Note: These commands apply to both Ubuntu and Arch Linux 

Firstly, open a terminal of your choice, 
Type in the terminal the following commands:

`git clone https://github.com/Streamerbot/sb-linux-installer` then press <kbd> Enter</kbd>

![gitclone.png](/linux-screenshots/gitclone.png){.align-center}

This will clone the github install repo to your `‘/home/Name/’` directory. So next we need to navigate to this directory in the terminal to run the install script. To do this simply type `cd sb-linux-installer/` and press <kbd> Enter</kbd>. it should look simialr to the image below. 

![directorynav.png](/linux-screenshots/directorynav.png){.align-center}

So now we have sucessfully navigated to the git clone directory. We need to use the install script that was created for use to install Streamer.Bot. So to do this type in the following `./install.sh` and then press <kbd> Enter</kbd>. 

![streamerbotinstallprocess1.png](/linux-screenshots/streamerbotinstallprocess1.png){.align-center}

Now the script will run and install all that is necessary for Streamer.Bot to run. 
> Note: it is important to accept and install all the prompts that appear for the bot to run 

![installcomplete.png](/linux-screenshots/installcomplete.png){.align-center}

When the script is complete it will say in the terminal window *installation successful* .

Congratulations Streamer.Bot is now installed but, there is one thing missing. If you look in the app draw you will see it without an icon, but we can fixed this with 2 simple commands in the terminal. (Although this should be fixed in the next update) 

![no_icon_in_app_draw.png](/linux-screenshots/no_icon_in_app_draw.png){.align-center}

In the terminal enter the following commands
- `cd ~/.local/lib/streamer.bot` 
- `wget https://cdn.discordapp.com/attachments/625780541454811136/900390770626928680/SB_Logo_oversized_bottomed.png -O streamer.bot.png`

![wget.png](/linux-screenshots/wget.png){.align-center}

When you have run those 2 commands your app draw and menu will display the streamer.bot with it's icon.

Just like the ones below.

![icon_in_appdraw.png](/linux-screenshots/icon_in_appdraw.png) ![arch_menu_icon.png](/linux-screenshots/arch_menu_icon.png)

Congratulations you have successful install and have a running Streamer.bot on your Ubuntu/Arch Linux install. 

![streamer_bot_running_.png](/linux-screenshots/streamer_bot_running_.png){.align-center}
![streamerbot_running_.png](/linux-screenshots/streamerbot_running_.png){.align-center}



