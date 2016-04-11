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
![fgfs](https://cloud.githubusercontent.com/assets/13025157/14443209/0a778136-003e-11e6-98dc-5a699933e7f6.jpg)

If you want more information about the software that we picked check [here](https://cageos.org/index.php?page=apps).

## Librerouter protect us against...?
- **Sniffers**: those that are checking your traffic
- **Government spy/monitoring institutions passive actions**: like passive bots collecting general data from worldwide, if they target  anyone... that is another story.
- **CommunityLibrerouter evil nodes**:  a box Owned for those _bad people_.
- **Malicious internet nodes**: better known as _blackbones_.
- **Your internet provider (ISP)**: if they would trying anything with your data.

## How it will protect me?
 - Filtering virus, webexploits, malware,ads ,bad IP-sources and bad content.
 - Decentralizing the services (doing impossible to apply big data to you )
 - Open authentication (dissolve legal relation between user and name-ip), Dark-nets (anonymisation of IP)
 - Forcing encryption for all communications and data storage and in rest.
 - Filtering the data that expose you, like scripts,cookies, browser info,etc.

## Which hardware is needed to run Librerouter?
 - https://www.gitbook.com/book/bananapi/bpi-r1/details
 - https://www.olimex.com/Products/OLinuXino/A20/A20-OLinuXIno-LIME2/open-source-hardware
 - https://www.element14.com/community/community/designcenter/sama5d3xplained/blog/2014/04/25/debian-on-the-sama5d3-xplained
 - https://eewiki.net/display/linuxonarm/ATSAMA5D3+Xplained

This is on discussion yet, but the idea is to offer a solution that can be deployable on a public distribution with your own hardware, but as standalone  we have this models:

- **Librerouter** has two presentations:

| Board | Board | Board | 
|--------|--------|--------|
| Banana bpir1  | OLinuXIno-LIME2 | ATSAMA5D3Xplained |
| ssd 8gbc10 | ssd 8gbc10| ssd 8gbc10 |
| 1xUSB2ETH+1xonboard | 1xUSB2ETH+1xonboard | 1xUSB2ETH+1xonboard |
| HDD 1TB | HDD 1TB | HDD 1TB|
| 2xWLAN 1watt | 2xWLAN 1watt| 2xWLAN 1watt| 
| Batterie UPS| Batterie UPS| Batterie UPS|
| Adapt-POE-volt| Adapt-POE-volt| Adapt-POE-volt| 
| usbto-Ledsblinkstick.com| usbto-Ledsblinkstick.com| usbto-Ledsblinkstick.com|
| CASE | CASE |  CASE | 
| RoboPeak RUSB or Waveshare | RoboPeak RUSB or Waveshare | RoboPeak RUSB or Waveshare | 

![dddd](https://cloud.githubusercontent.com/assets/13025157/14441894/5ea09592-0037-11e6-9e6c-14e2254f6728.jpg)

## Setup
<!-- this part needs to be refactored by someone that does know the current state of building process -->
There are 2 ways to join to CommunityLibrerouter network

##### 1. Setup CommunityLibrerouter software on Physical/Virtual machine----Debian or librekernel distro
##### 2. Setup CommunityLibrerouter software on ARM-------------------------Debian or librekernel distro croscompiled

#### Steps to setup on Physical/Virtual machine.
**Step 1: Checking requirements**
Your Physical/Virtual machine need to meet the minimum requirements:
 - 1. x2 network interfaceS
 - 2. 1 GB of RAM
 - 3. 16 GB of SD or micro SD or virtual booting HD
 - 4. SATA HARDDISK or separate second phzsical or virutual DISK

The way networking works in Librerouter will be:

2 Bridges two interfaces each
 - 1x bridge acts as a WAN
 - 2st bridge acts as LAN

So, we actually have 4 possible PHySICAL scenarios
 - WAN is WiFi, LAN is WiFi
 - WAN is WiFi, LAN is Cabled Ethernet
 - WAN is Cabled Ethernet, LAN is WiFi
 - WAN is Cabled Ethernet, LAN is Cabled Ethernet

**Step 2: Setup the network.**
In this step you need to connect one interface of your machine to Internet, and other one to local network device.
Networking of Librerouter has two way to work.
**Server mode**
The way networking works in Librerouter will be:
 -1 uniqe fix IP LAN or Bridge> can be WLAN or Cabled Ethernett connected to the existing internet router LAN. Server mode with single LAN interface and not redirecting domains or threating the traffic (not hable to defend against web browsing leaks and malware)
![server](https://cloud.githubusercontent.com/assets/13025157/14443924/9c798300-0042-11e6-85b1-1760c5b3789d.png)
 -b) Bridge mode where the trafic is filtered by dns, and by proxy squid with clamav and ssl bumping, and surikata. Also redirecting dns via TOR and dnssec)
![bridge](https://cloud.githubusercontent.com/assets/13025157/14443871/4bf91bfc-0042-11e6-9ca5-06a23891d32e.png)

![wizard](https://cloud.githubusercontent.com/assets/13025157/14444156/373281de-0044-11e6-9d3d-6c536c0b3844.png)



**Step 3. Executing scripts.**
In this step you need to download and execute the following scripts on your machine with given order.
1. app-installation-script.sh
2. app-configuration-script.sh



#### Steps to setup on LibreRouter.

**Step 1. Get an A20-OLinuXIno-LIME2 and assemble it.**

There are several seperate modules that need to be connected to A20-OLinuXIno-LIME2.

You can find more information about necessary modules [here](https://213.129.164.215:4580/dokuwiki/doku.php?id=technical:hardware:communityLibrerouter_-_odroid_xu3_lite).

**Step 2. Executing scripts.**

In this step you need to download and execute the following scripts on your machine with given order.

1. app-installation-script.sh
2. app-configuration-script.sh


#### Workflow of scripts.

**1. app-installation-script.sh (Initialization script)**

Script workflow

1. Check User 
  * You need to run script as root user

2. Check Platform 
  * Platform should be Debian 7/8, Ubuntu 12.04/14.04, Trisquel 7.0

3. Check Hardware 
  * If you are running this script on odroid it should detect Intel processor

4. Check Requirements (Only for Physical/Virtual machine) 
  * Machine should match the requirements mentioned above

5. Check Internet
  * Check Internet connection

6. Check If Assembled (Only gor LibreRouter)
  * All neccessary modules should be connected to odroid board

7. Configure Bridge Interfaces (Only for LibreRouter)
  * eth0 and wlan0 will be bridged into interface br0
  * eth1 and wlan1 will be bridged into interface br1
  * In ethernet network, br0 should be connected to Internet and br0 to local network
  * In wireless network, bridge interdace with wore powerful wlan will be connected to Internet and other one to local network

8. Prepare perositories
  * Update repositories for necessary packages

9. Download packages
  * Download necessary packages

10. Install packages
  * Install necessary packages

>You can find Initialization workflow [here](https://213.129.164.215:4580/dokuwiki/doku.php?id=initialization_workflow)

**2. app-configuration-script.sh (Parametrization script)**

It aims to configure all the packages and services.

![networktraffic6](https://cloud.githubusercontent.com/assets/13025157/14437535/f40d21c4-0021-11e6-9e4a-1c73e06e965b.png)

1. Check User 
  * You need to run script as root user

2. Get variables
  * Get variables values defined by app-installation-script.sh

3. Configure network interfaces
  * External interface will be configured to get ip dinamically 
  * Internal interface will be configured with static ip address 10.0.0.1/24
  There are also 4 virtual interfaces
  * :1 10.0.0.251/24 for Yacy services
  * :2 10.0.0.252/24 for Friendica services
  * :3 10.0.0.253/24 for Owncloud services 
  * :4 10.0.0.254/24 for Mailpile services

4. Configure DNS resolution
  * Unbound DNS will be configured to listed 10.0.0.1:53
  * Tor DNS will be configured to listed 10.0.0.1:9053
  * DjDNS will be configured to listed 10.0.0.1:8053

#### DNS resolution process.
##### Classified domains
  * Search engines  - will be resolved to ip address 10.0.0.251 (Yacy) by unbound.
  * Social networks - will be resolved to ip address 10.0.0.252 (friendics) by unbound.
  * Storages        - Will be resolved to ip address 10.0.0.253 (Owncloud) by unbound.
  * Webmails        - Will be resolved to ip address 10.0.0.254 (MailPile) by unbound.
    
##### Local, i2p and onion domains
  * .local - will be resolved to local ip address (10.0.0.0/24 network) by unbound.
  * .i2p   - will be resolved to ip address 10.191.0.1 by unbound.
  * .onion - unbound will forward this zone to Tor DNS running on 10.0.0.1:9053
   
##### Other domain names
  * Any other domain name will be resolved by DjDNS with DNSSEC validation.

>Please see left part of workflow image.

5. Configure Reverse proxy

## License
>You can check out the full license [here](https://github.com/CommunityLibrerouter/debian-autoscript/blob/master/LICENSE)

This project is licensed under the terms of the **GNU GPL V2** license.

//////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////
This wizard should ask the customer about and is pending in the project to be developed:
 -a) Do you want your protect your privacy or just user Librerouter services? if yes then mode bridge if not then mode equals server.
 -b) Mode Transparent firewall Bridge:
 -     Lets configure the Internet access (WAN)
 -     Do you want to conect your Librerouter to your Internet router via cable or WLAN?
 -         if WLAN
Please specify your internet router SSID Please specify your encryption methods WPA or WPA2 WEP not allowed no encryption not allowed Please specifiy your SSID password The daemon should check the conection getting up If not especify error conditions

if Cable:

*If Cable and DHCP:
Please specify if you would use fix IP or DHCP client? If DHCP Then setup dhcp client in the interface and try to receive IP The daemon should check the conection getting up If not especify error conditions

If Cable and FIX IP address:
*Please provide the IP address Please provide the default GW Please provide the DNS server Trying ping against the IPs If correct finish The daemon should check the conections answers If not especify error conditions

Lets configure the Internal access (LAN Intranet)
 -Do you want to setup your internal protected network via cable or WLAN?

If WLAN then:
 -Please specify your internal new WLAN name SSID Please specifiy your SSID WPA2 CCMP password The daemon should check the connection getting up If not especify error conditions The IP addresses are 10.0.0.1 forced (if the guy another then hack the box)

if Cable then:
 -Please be aware we use this internal range: 10.0.0.100 to 200 Gateway 10.0.0.1 and DNS
 -Please plug a cable Detecting link Link up Now your connected

c) Mode Server only WAN external bridge will be used and then all WLAN and ETH will be all 4 interfaces in the same Bridge NIC logical interface.Do you want to use a cable or want CCube connect to your router or switch?

if WLAN

Please specify your internet router SSID Please specify your encryption methods WPA or WPA2 WEP not allowed no encryption not allowed Please specifiy your SSID password The daemon should check the conection getting up If not especify error conditions

if Cable:
If Cable and DHCP:
Please specify if you would use fix IP or DHCP client? If DHCP Then setup dhcp client in the interface and try to receive IP The daemon should check the connection getting up If not specify error conditions

If Cable and FIX IP address:
Please provide the IP address Please provide the default GW Please provide the DNS server Trying ping against the IPs If correct finish The daemon should check the connections answers If not specify error conditions

