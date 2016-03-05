---
layout: post
title: Getting started with Ethereum and the Mist Browser
date: 2016-02-28 16:19:00
description: A quick guide to installing the Mist browser on Ubuntu 12.04
---

### Prepare a folder to install into

We are going to create a new folder to hold all of the ethereum related repos we will be downloading, so to start:

{% highlight c++ %}
mkdir ethereum
cd ethereum
{% endhighlight  %}

In order to get the code we will be running, we will be using git, which I will not cover here. So, assuming you have git installed and set up, we will start by installing the dependecies:

{% highlight c++ %}
sudo apt-get update

sudo apt-get install curl

curl https://install.meteor.com/ | sh 


sudo apt-get install npm 

sudo npm install -g electron-prebuilt

{% endhighlight  %}

if this does now work, try

{% highlight c++ %}
sudo apt-get install nodejs-legacy first
{% endhighlight  %}

This is required because node changed its package name, and as such cannot always be found. This package creates a link between the new and old directories.


## Install Mist

We will use mist, as the graphical front end of ethereum. It is still in development, so have patience. 

So lets first go ahead, clone the source and install it with npm

{% highlight c++ %}
git clone https://github.com/ethereum/mist.git
cd mist
git submodule update --init
npm install
{% endhighlight  %}


### Start the interface

Hopefully, that will have installed the mist software, from here, we will need to run it, which is not an obvious process. We are going to require two terminal windows.

In  new terminal window (Ctrl +Shif +T), we will move to the interface folder, and start a meteor process.

{% highlight c++ %}
cd interface && meteor
{% endhighlight  %}

Let this update the package catalogue, it may take a minuite. Now, leaving that meteor process running, we will move back to the original window, and start the mist program, like so:

{% highlight c++ %}
electron .
{% endhighlight  %}

And that should be it, the mist browser should now run, assuming everything installed correctly.

The wallet will now sync with the block chain, this can take a long time, so I recommend looking through some of the tutorials.

After mist has synced up with the blockchain, if you get a window that is completly white (as I did) you might be having issues with a NVIDIA and itel graphics card.

In this case, try running:
{% highlight c++ %}
electron . --ignore-gpu-blacklist
{% endhighlight  %}


Next step, we will start to play with the wallet and easy contracts.




