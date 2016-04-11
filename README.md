Librerouter
==============


## What is Librerouter?

***Librerouter*** is a technology that makes protecting your privacy easy by:

a) If you buy a premade server
b) If you install the scripts in a Virtual machine that becames bridge virtual server

Thanks to a unique combination of open hardware (Yes really open and just a say check the link here) and open source software(yes bree of binary blobs so no just opensource but paranoid openess according Libre Kernel GNU standars.) 

###Why do we need this technology?

The Internet is full of ___free___ services and you are the product they sell your data, in their _terms and conditions page_, that ***almost nobody reads***, and **Librerouter** operates exactly the opposite:


## Services runing in Librerouter

Some of __Librerouter__ services has being provided by some time, but un-integrated and with some flaws, let's show you:

![Services](https://ksr-ugc.imgix.net/assets/003/699/855/2679953ba748e512d3ec207f732d1bb2_original.jpg?v=1430329011&w=680&fit=max&auto=format&q=92&s=b7153d55686098a5c8a52ef9a57e10bd)

If you want more information about the software that we picked check [here](https://cageos.org/index.php?page=apps).

## Librerouter protect us against...?
- **Sniffers**: those that are checking your traffic
- **Government spy/monitoring institutions passive actions**: like passive bots collecting general data from worldwide, if they target  anyone... that is another story.
- **CommunityLibrerouter evil nodes**:  a box Owned for those _bad people_.
- **Malicious internet nodes**: better known as _blackbones_.
- **Your internet provider (ISP)**: if they would trying anything with your data.

## How it will protect me?
 - Filtering virus, exploits _malware_, ads , bad IP-sources and bad content.
 - Decentralizing the services (doing impossible to apply big data to you )
 - Open authentication (dissolve legal relation between user and name-ip), Dark-nets (anonymisation of IP)
 - Forcing encryption for all communications and data storage and in rest.
 - Filtering the data that expose you, like scripts,cookies, browser info,etc.
![Network](https://www.cageos.org/network/images/NetworkTraffic6-small.png?raw=true "Optional Title")
You want more information, you can check [here](https://cageos.org/index.php?page=network) for more information or 

## Which hardware is needed to run Librerouter?

This is on discussion yet, but the idea is to offer a solution that can be deployable on a public distribution with your own hardware, but as standalone  we have this models:

- **Librerouter** has two presentations:

|Low-end model - Odroid C2| High-end model - Odroid XU4|
|--------|--------|
|Odroid C2  | Odroid XU4 |
|ssd 8gbc10|ssd 8gbc10|
|USB2ETH | HDD 2TB|
|2xWLAN 1watt| SB2ETH |
|Batteries|2xWLAN 1watt|
|CASE| CASE|
|RoboPeak Usb tft screen  |RoboPeak Usb tft screen  |

![XU4](https://ksr-ugc.imgix.net/assets/003/944/858/1dd038cc6d011fae2e9c64b3373f26aa_original.jpg?v=1433797073&w=680&fit=max&auto=format&q=92&s=7465889c0357eb0ccbaf781a4c0e7016)

More information [here](https://213.129.164.215:4580/dokuwiki/doku.php?id=technical:hardware:communityLibrerouter_-_odroid_xu3_lite).


## Setup
<!-- this part needs to be refactored by someone that does know the current state of building process -->
There are 2 ways to join to CommunityLibrerouter network

##### 1. Setup CommunityLibrerouter software on Physical/Virtual machine.
##### 2. Setup CommunityLibrerouter software on Odroid XU3/XU4/C1+/C2.

#### Steps to setup on Physical/Virtual machine.

**Step 1: Checking requirements**

Your Physical/Virtual machine need to meet the minimum requirements:

1. 2 network interface
2. 1 GB of Physical memory
3. 16 GB of free space

If your machine is ok with requirement, then you can process to next step.

**Step 2: Setup the network.**

In this step you need to connect one interface of your machine to Internet, and other one to local network device.

**Step 3. Executing scripts.**

In this step you need to download and execute the following scripts on your machine with given order.

**1. test.sh (Initialization script)**

Script workflow

1. Check User 
  * You need to run script as root user

2. Check Platform 
  * Platform should be Debian 7/8, Ubuntu 12.04/14.04

3. Check Hardware 
  * If you are running this script on odroid it should detect Intel processor

4. Check Requirements 
  * Machine should match the requirements mentioned above

5. Check Internet
  * Check Internet connection.

6. Prepare perositories
  * Update repositories for necessary packages

7. Download packages
  * Download necessary packages

8. Install packages
  * Install necessary packages

>You can find Initialization workflow [here](https://213.129.164.215:4580/dokuwiki/doku.php?id=initialization_workflow)

**2. app-installation-script.sh (Configuration script)**

It aims to configure all the packages and services.


#### Steps to setup on Odroid board.

**Step 1. Get an odroid and assemble it.**

There are several seperate modules that need to be connected to odroid board.

You can find more information about necessary modules [here](https://213.129.164.215:4580/dokuwiki/doku.php?id=technical:hardware:communityLibrerouter_-_odroid_xu3_lite).

**Step 2. Executing scripts.**

In this step you need to download and execute the following scripts on your machine with given order.

**1. test.sh (Initialization script)**

Script workflow

1. Check User 
  * You need to run script as root user

2. Check Platform 
  * Platform should be Debian 7/8, Ubuntu 12.04/14.04

3. Check Hardware 
  * If you are running this script on odroid it should detect ARM processor

4. Check If Assembled 
  * All neccessary modules should be connected to odroid board

5. Configure Bridge Interfaces 
  * eth0 and wlan0 will be bridged into interface br0
  * eth1 and wlan1 will be bridged into interface br1
  * In ethernet network, br0 should be connected to Internet and br0 to local network
  * In wireless network, bridge interdace with wore powerful wlan will be connected to Internet and other one to local network

6. Check Internet
  * Check Internet connection.

7. Prepare perositories
  * Apdate repositories for necessary packages

8. Download packages
  * Download necessary packages

9. Install packages
  * Install necessary packages


>You can find Initialization workflow [here](https://213.129.164.215:4580/dokuwiki/doku.php?id=initialization_workflow)

**2. app-installation-script.sh (Configuration script)**

It aims to configure all the packages and services.


## License
>You can check out the full license [here](https://github.com/CommunityLibrerouter/debian-autoscript/blob/master/LICENSE)

This project is licensed under the terms of the **GNU GPL V2** license.

