# A Relatively Secure LEMP Server Stack Setup in Ubuntu 20.04 LTS

> By _Dishant Modh_

- [A Relatively Secure LEMP Server Stack Setup in Ubuntu 20.04 LTS](#a-relatively-secure-lemp-server-stack-setup-in-ubuntu-2004-lts)
	- [Introduction](#introduction)
		- [Specifications/Target](#specificationstarget)
	- [The Installation](#the-installation)
		- [Update APT](#update-apt)
		- [Installing Nginx](#installing-nginx)
		- [Installing MySQL](#installing-mysql)
		- [Installing PHP](#installing-php)
		
		
## Introduction

In this guide, **LEMP** stands for **Linux**, **Nginx** (pronounced as
Engine-X), **MySQL** and **PHP** (PHP Hypertext Preprocessor). Also, as a
bonus.

I have gone through many websites in order to learn even just the basics of
setting up a LEMP server. Here I have created a through guide to help someone 
relatively new to setup a powerful LEMP machine easily and effortlessly. 
I hope this guide comes to someone's rescue.

The instructions on this guide has been tested to work on a fresh install of
Ubuntu 20.04. Also, the system was fully updated before we started with the 
LEMP setup procedure.

For any other platform, this guide should still serve as a useful resource. The
"mini goals" are well defined in various paragraphs. And one can easily look
elsewhere for specific instructions for that platform to achieve same "mini
goal", one at a time.

For a system already running other version of server stacks (example LAMP),
some additional steps (like removing those packages or disabling them) might
be required. That is beyond the scope of this guide.

### Specifications/Target

* **Ubuntu**                v20.04
* **Nginx**                 v1.18.0
* **MySQL**                 v8.0.26
* **PHP**                   v7.4.3

## The Installation

Let's finally begin the actual installations processes.

_During the installation of any package, when faced with any unsure prompt,
just go with the default option/action._

### Update APT

First, we want to make sure we have the latest records in our local packages
registry. Let's run the following command in the terminal like so.

```shell
sudo apt update
```

### Installing Nginx

First thing we’re going to install is the server called Nginx.

```shell
sudo apt install nginx
```

If you do not have a domain name pointed at your server and you do not know your server’s public IP address, you can find it by running the following command:

```shell
ip addr show eth0 | grep inet | awk '{ print $2; }' | sed 's/\/.*$//'
```
This will print out a few IP addresses. 

Type the address that you receive in your web browser and it will take you to Nginx’s default landing page:

```shell
http://server_domain_or_IP
```
