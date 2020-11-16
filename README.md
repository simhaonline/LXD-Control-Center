# LXD Control Center

It is yet another simple UI for LXD with Django and Subprocess.
Easily manage your Linux containers from any devices. Note that you need to have root acces and have LXD installed and initialized. All the command bellow have to be run as root user. Use the command : _sudo su_ to impersonate the root user if you are using sudo on your system.



![alt text](https://imgur.com/7zcIV74.png "Screenshot By the way lydianna is the hostame of the computer it was runnin on.")

### On many linux distro to install and initialize lxd


snap install lxd

lxd init

learn more on LXD with this good documentation !

https://linuxcontainers.org/lxd/getting-started-cli/

## To try LXD Control Center 

### install dependency :

#### Debian based OS :

_apt install python3 git wget_

#### Redhat based OS :

_yum install python3 git wget_

#### Arch based OS :

_pacman -S python3 git wget_

### download the script :

_wget https://github.com/radio0but/LXD-Control-Center/releases/download/Version-1/install.sh_


Execute the install script to install LXD-Control-Center in your /opt folder:

### Make it excutable :

_chmod +x ./install.sh_

### And execute it

_./install.sh_

Its gonna ask for an username, an e-mail adress and a password

(You can leave the e-mail adress blank)

## To uninstall or Update

delete the folder /opt/LXD-Control-Center

__rm -r  /opt/LXD-Control-Center/__

then to update simply rerun the install script

## To start the server:

First you have to make the *start.sh* script executable

**chmod +x /opt/LXD-Control-Center/start.sh**

Then run the start script

__/opt/LXD-Control-Center/start.sh__ 

## Almost Done

to see the UI go to http://localhost:8082/

Go to http://localhost:8082/admin to change your password and add users. Users need to have staff permission to access LXD-Control-Center

## Optional Settings

If you want the app to be visible on the network add your IP or 0.0.0.0 to /opt/LXD-Control-Center/settings.py 

__nano /opt/LXD-Control-Center/LXDcontrolCENTER/settings.py__

change
__ALLOWED_HOSTS = ["localhost"]__

To something like this

__ALLOWED_HOSTS = ["localhost","Yo.ur.Lo.cal.Ip","exemple.com"]__

Then you can use one of your containers as a reverse proxy.  
