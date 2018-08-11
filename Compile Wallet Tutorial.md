---
# EOCH Qt Wallet GUI Compilation Guide
---

## Building the EOCH wallet on Ubuntu/Debian

This is a guide for compiling the EOCH wallet using Linux. By following this guide, you will be able to create a GUI wallet directly from the source code.

## Requirements

The basic requirements for wallet compilation:

```
Linux (Ubuntu or Debian-based distribution is prefered but any other Linux distro can be used)

32 or 64-bit
```

It is recommended to have at least 1 GB of memory available when compiling the EOCH wallet. 
Compilation will take much longer with 512 MB of memory or less.

## Getting started

You need to make sure your Linux machine is up to date. 
Open a terminal window by clicking the right side mouse button and choosing Open Terminal while in the Desktop.

![Image](http://github.com/EOCHfoundation/EOCH/blob/master/etc/images/1terminal.png?raw=true)

In the terminal window type:

```
sudo apt-get update (press Y to update)

sudo apt-get upgrade (press Y to upgrade)
```

![Image](http://github.com/EOCHfoundation/EOCH/blob/master/etc/images/1sudopass.png?raw=true)

**Note**: Every time you issue a command using **sudo**, it will ask you for your password. It will not be visible while you type it. Press enter once you finish typing it.

It might take a few minutes to update/upgrade.

## Install the dependency packages

Sometimes it is necessary to install extra libraries and dependency packages or simply to update them.
Using the terminal window, type:

```
sudo apt-get install qt5-default qt5-qmake qtbase5-dev-tools qttools5-dev-tools build-essential libssl-dev libdb++-dev libboost-all-dev libqrencode-dev libminiupnpc-dev
```

Accept any installation or update prompt by pressing the Y key.

## Download the EOCH source code

You can download the source code directly to your Desktop. It will automatically create a EOCH folder.

```
cd Desktop

git clone http://github.com/EOCHfoundation/EOCH.git
```

![Image](http://github.com/EOCHfoundation/EOCH/blob/master/etc/images/1gitclone.png?raw=true)

## Final stage - Compilation

You are now ready to compile the wallet. You need to enter the directory where the source code was copied to, in this case the EOCH folder:

```
cd EOCH
```

Execute this command:

```
qmake EOCH-qt.pro
```

![Image](http://github.com/EOCHfoundation/EOCH/blob/master/etc/images/1qmake.png?raw=true)

And:

```
make -f Makefile
```

You will see something like this being displayed. Wait until the process is finished.

![Image](http://github.com/EOCHfoundation/EOCH/blob/master/etc/images/1xtramake1.png?raw=true)

Once the wallet has been successfully compiled, you will be able to run it.

***


#### An alternate way to compile the wallet

This is an alternate way to compile the wallet. Follow all the above steps but instead of typing **qmake EOCH-qt.pro** and **make -f Makefile**, use the following command:

```
qmake && make
```

![Image](http://github.com/EOCHfoundation/EOCH/blob/master/etc/images/1qmake1.png?raw=true)


Once it is done type:

```
chmod +x EOCH-qt 
```

![Image](http://github.com/EOCHfoundation/EOCH/blob/master/etc/images/1chmod1.png?raw=true)

**Note**: Though not necessary, this command makes the file executable.

***

## Running the wallet

To run the wallet simply type:

```
./EOCH-qt
```

![Image](http://github.com/EOCHfoundation/EOCH/blob/master/etc/images/1wallet2.png?raw=true)

You now have a fully functional wallet. Enjoy!

![Image](http://github.com/EOCHfoundation/EOCH/blob/master/etc/images/1wallet.png?raw=true)

## Info

EOCH Core downloads and stores the entire history of EOCH transactions;
depending on the speed of your computer and network connection, the synchronization
process can take anywhere from 15 minutes to a few hours or more.

Join Slack for more help and information. Please visit our bitcointalk ANN at http://bitcointalk.org/index.php?topic=1864397.0 and request an invitation. Send a DM to either: fishfishfish313, BRYAN_K, rule144, cefinnell01 or CCRevolution (in the forum) and we will manually add you to the Slack. Thank you!

## EOCH social links:

**BITCOINTALK FORUM** - http://bitcointalk.org/index.php?topic=1864397.0 <br />
**FACEBOOK** - http://www.facebook.com/EOCHOfficial/ <br />
**TWITTER** - http://twitter.com/EOCH <br />
**REDDIT** - http://www.reddit.com/r/EOCH <br />
**YOUTUBE** - http://www.youtube.com/c/EOCHOFFICIAL <br />
**STEEM** - http://steemit.com/@EOCH <br />
**MEDIUM** - http://medium.com/@EOCH <br />
**INSTAGRAM** - http://www.instagram.com/EOCH <br />
**VIMEO** - http://vimeo.com/EOCH <br />
**SLACK** - http://EOCH.herokuapp.com <br />

***

Version 1.0
