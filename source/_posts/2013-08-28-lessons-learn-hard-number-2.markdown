---
layout: post
title: "lessons learn hard#2"
date: 2013-08-28 01:13
comments: true
categories: 
---

Installing VirtualBox on Ubuntu 13.04
======================================
1. When installing virtual box on linux boxes generic headers need to be installed.

  	a. go to vagrantup and grab the latest version for your os 	
  	b. install latest version 	
  	c. install linux-generic headers suggestion by virtualbox  
  	d. Virtual Box 
  	e. Restart is necessary or same error will be thrown 

More at  	

http://askubuntu.com/questions/171684/trouble-running-virtualbox-on-ubuntu

Using PPAs
==========================================
2. Clear benefit of using PPAs instead of ones provided by linux canonical

	a. most up to date version   
	b. fixed anything if you are doing early_adopter/bleeding edge projects  
	c. usually add once, and done  

head to launchpad.net   
read technical instructions   
add that PPA for your version and flavor of linux   

sudo apt-get update   
sudo apt-get upgrade  

Either now you will have an updated version of your tool you are trying to run or you can now sudo apt-get install it 


Mergetools
===================
3. Using different mergetools whichever one you like best

git mergetool -t xdiff3 is pretty cool.

