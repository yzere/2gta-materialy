# Materiały merytoryczne z lekcji CISCO

Tutaj zamieszczone zostają notatki z zagadnień CISCO w języku angielskim.



# Notatka 1: Urządzenia sieciowe / Network devices

## Definition of Computer network:

A computer network is a group of computers that use a set of common communication protocols over digital interconnections for the purpose of sharing resources located on or provided by the network nodes. 

## Network devices:

<p align="center">
  <img src="/media/network-devices.jpg">
</p>

### End-hosts
- Clients (def. Clients are nodes that access resources or services shared on the network by a server)
  - PC
  - Laptop
  - Smartphone
- Servers (def. Servers are nodes that provide resources or services via network for client)

### Border
- Firewall

> Firewall can be software and hardware. Hardware firewall is a device that is between outer network (internet) and local endpoints. It can be inside network or just before network (before or after main router). Firewall can also be software. So called host-based firewall filters traffic on end-host device. New advanced firewall devices are called Next-Generation Firewalls. They receive data on pins 3 and 6, also send data on pins 1 and 2.

- Proxy Server
> Proxy server is a network server that allows clients to connect indirectly to resources or services located on the other network.

### Core
- Switch
> Switches are devices that connect multiple endpoints together and redirect traffic using packet switching. They have a lot of ports to connect multiple devices at once. They operate on layer 2 of OSI stack so they understand MAC addresses of devices. They do not separate networks, but they are used to extend existing networks. They send data on pins 3 and 6 , also receive data on pins 1 and 2 .

- Hub
> Hubs are now rarely used but you can still encounter them. They connect network devices to act as one network segment. They simply allow network traffic to flow through them to lower number of cables coming to switch. Because of that they operate on layer 1 of OSI stack. As well as switches they send data on pins 3 and 6 , also receive data on pins 1 and 2 .

- Router
> Routers are devices that connect networks with each other allowing communication between them. They have fewer ports. They operate on layer 3 of OSI stack so they understand logical IP address.  They separate networks from each other making a distinct border of local area network. They receive data on pins 3 and 6, also send data on pins 1 and 2

- Gateway
>Gateways provide connectivity between one discrete network to another. It is distinguished from router in the manner  that it can utilize more than one protocol to connect different networks. It can operate on any level of OSI stack. Most of the time it refers to device that performs functions of gateway.

- Repeater
> Repeaters are used to extend physical range of network. Their usage is posed when network requires to connect devices on lengths larger than Ethernet cables can provide. Now they are mostly underused because optic fiber cables can operate even on MAN bases.

# Notatka 2: Kable i interfejsy / Cables and interfaces

## In use today we specify 3 types of cable:

### Coaxial (pl. koncentryczne)

> These cables consist of copper core that transmits data. They were not developed to transmit network data but because of lack of options for this purpouse, admins started to build networks based on them. Their slow bandwith and structure brought them to extinction, where non of new networks use them.

<p align="center">
  <img src="/media/coaxial.jpg">
</p>

### Twisted-pair cable

> They were developed strictly for networking purposes. They are also knows as "Ethernet cables". Nearly all modern day networks use this type of cable. They consist of 4 pairs, 8 wires in total, twisted together to mitigate EMI (electro-magnetic interference). Their max lenght is 100m.

- UTP - unshielded twisted pair - all 4 pairs are wrapped in one sheath
- STP - shielded twisted pair - each pair is wrapped in metal shield to mitigate even more EMI between pairs and then into one sheath
- FTP - foil screened twisted pair - all 4 pair are wraped in foil that shields cable from outer interference.

<p align="center">
  <img src="/media/utp-stp.jpg">
</p>

#### There are two main types of ethernet cables:
- straight-through cable - these are used to connect other network devices to layer 1 and 2 devices such as switches and hubs.
- cross-over cable - these are used to connect devices from layer 3 and higher together, and to ceonnect switches together. Their main goal is to allow connect devices with the same pin arangement. Today 
Difference between the two is on pin arrangement shown on included photo.

<p align="center">
  <img src="/media/straight-cross.jpg">
</p>

### Optic fiber cable

Fiber cables use light to transmit data through a glass crystal core. It was designed for transition of large amount of data on longer distances. In contrast to UTP cables, these can go up to  30-50km depending on revision and quality of cable. They also require special connector SFP transceiver (Small form-factor pluggable).

<p align="center">
  <img src="/media/fiber-crossection.jpg">
</p>

- SMF - single mode fiber
> More expensive type of fiber cables. It consists of core that allows light to travel under one angle. This makes it go further and have higher bandwidth. It is moslty used in MAN networks and to transfer data to other building in town.

- MMF - multi mode fiber
> Less expensive type of fiber cable. Core of this type of cable allows light to travel under many angles. This decreases its reach and bandwidth but is much cheaper to produce. You would see it in datacenters where there are distances longer than 100m that requiring fast and responsive answer.

### Cables specs
Down below are tables with standars for ethernet and fiber cables.

#### Ethernet

<p align="center">
  <img src="/media/ethernet-table.png">
</p>

#### Fiber

<p align="center">
  <img src="/media/fiber-table.png">
</p>

## Interfaces / Connectors

### RJ-45 (or 8P8C)

Pin layout and functions of RJ-45 connector, that is the most popular interface for ethernet cables.

<p align="center">
  <img src="/media/pins.jpg">
</p>

### SFP transceiver

<p align="center">
  <img src="/media/sfp-image.jpg">
</p>

# Notatka 3: Model sieciowy OSI i TCP/IP / OSI and TCP/IP networking models

## Definition of networking model:
>Network models categorize and provide a structure of protocols and standards.

This briefly means that networking models try to gather together ways our media devices can communicate so that we dont encounter not compatible elements.

### Disclaimer:
**OSI model is precursor of todays IP/TCP suit. Sheer OSI model is not in use today but network engineers tend to refare to OSI model when talking about data on network. It is important that you also understand concepts of IP/TCP suit and its correlations to OSI model. It will allow for greater understanding of network basics. **

Links to one of the best explanations of OSI model as well as its real world examples:

<a href="https://www.youtube.com/watch?v=CRdL1PcherM"> OSI model explaination </a>
<br>
<a href="https://www.youtube.com/watch?v=3kfO61Mensg"> OSI model real world examples </a>

## Definition of OSI model

> The Open Systems Interconnection model (OSI model) is a conceptual model that characterises and standardises the communication functions of a telecommunication or computing system without regard to its underlying internal structure and technology.

### OSI stack can be a bit tricky to understand, but to put it in simple terms:
<br>

OSI model specifies how (what protocol, what format, what data, what voltage) network traffic is processed, send, recived and read by media devices. Process of packing network data into these 7 layers is called Encapsulation. It allows to, following standards, pack data into packets that can be processed by any device on its way.
<br></br>
IP/TCP as a child grown by OSI model is very similar to it. The difference between the two is that IP/TCP merges aplicaton, presentation and sesion into one layer, Application. It also merges data link and physical  into Link layer (or Network interface layer). It allows to simplify traffic description, even though network engineer tend to still refer to OSI model when talking about traffic and encapsulation.


*Not all packets are wraped in 7 layers. For example ARP requests operate on layer 2 utilizing MAC adresses to get to destination. Where as ping command that uses ICMP protocal, operates on layer 3 using logical IP addresses. I highly recomend you dive deep into understanding OSI stack as it gives all networking concept more sense.*

## OSI model layers

### Important note:
Every layer has its own special kit of functions. Its important to differentiate what functions are on which layer as its help to understand later on, how do different packets travel through network. Below is a list of characteristics of every layer:

- Layer 7 - Application :
  - This layer is closes to user.
  - It interacts with application for example web browser and is NOT one.
  - It operates on HTTP and HTTPS protocols.
  - It is used to identify communication partners.
  - It allows to synchronize communication.

- Layer 6 - Presentation
  - Data in  application layer is "application format" that need s to be translated to different format to be sent via internet.
  - Presentation layer translates between application and network formats
  - It for example encrypts and decrypts data upon departure and arrival.

- Layer 5 - Session
  - Controls bialogues (sessions) between communication hosts.
  - It manages connection between local and remote application.
  - It is responsile for establishing and closing these connections.

**These 3 layes merge into one Application layer in TCP/IP model, and they are not a thing of discussion between network engeneers. They do not influence traffic but data inside. For these layers are responsible software devs.**

- Layer 4 - Transport
  - Encapsulated data is here called segment. Device attaches L4 header here that provides host to host connection. Main parts of L4 header is to provide destination port and protocol.
  - This layer segments and reassembles data from end hosts communication.
  - It devides big data pieces into smaller segmenta that can be sent over the network.

- Layer 3 - Network
  - This layer is responsible for providing logical addressing for packet. It means that L3 header that is atached her includes logical adressing (IPv4).
  - Data is here called Packet, it has data+L4 header+L3 Header.
  - It provides connection between end hosts on diffrent networks.
  - It allows for path selection from source to destination.
  - Routers operate on layer 3 as they connect diffrent network together.

- Layer 2 - Data Link
  - This is last layer that operates of software part of traffic. 
  - Data here is called Frame. This layer attachaes L2 header as well as L2 trailer.
  - It provides node-to-node connection and data transfer. (PC to switch, switch to router etc)
  - It defines how data is formated for transmition over physical medium.
  - It provides error detection and correction for Physical layer.
  - It has its own addressing. Layer 2 addressing uses MAC adresses (BIA addresses).
  - Switches operate on layer 2.

- Layer 1 - Physical
  - It defines characteristics of medium used to dransfer data.
  - It defines physical specification of data transfer (for example: voltage levels, maximum transmission distance, connectors or cable specs)
  - Data here is split into bits and sent over the physical medium as electric current, light or electro-magnetic waves.

## Encapsulation and PDUs (protocol data units)

When you finaly understand concept of OSI model and what layers it is composed of, you can understan encapsulation.
Encapsulation is a process of packing a data into envelope that is secure and can be read by every intended device on its way. As said in previus part, Layer 4,3 and 2 headers as well as Layer 2 Trailer are a main part of encapsulation process.

<p align="center" width="90%">
  <img src="/media/encap.gif">
</p>
*As you can see on image above, the data is moving down the stack beeing prepared with all nessesary data attached. Further down this note I will provide references to how each header is composed and why it is the way it is. It is not required right now but lated on in the course you will feel need to check them out.*

For now it is important that you remember how do we call data on each layer of encapsulation:

<p align="center">
  <img src="/media/pdu.jpg">
</p>

### Additional reading materials:

<a href="https://www.cloudflare.com/learning/ddos/glossary/open-systems-interconnection-model-osi/">CloudFlare explaination of OSI layers </a>

<a href="https://pasja-informatyki.pl/sieci-komputerowe/model-tcp-ip-iso-osi/">Po polsku: Mirosław Zelent o modelach TCP/IP oraz OSI </a>

Cheatsheet that you can download and have on hand when you study: <a href="https://community.cisco.com/kxiwq67737/attachments/kxiwq67737/4461-docs-network-infrastructure/5987/1/01.%20OSI%20Model%20CheatSheet%20-%20ATech%20(%20Waqas%20Karim%20)%20v1.2.pdf"> Download!
  
<p align="center">
  <img src="/media/cheatsheet.png">
</p>
</a>

# Notatka 4: Wstęp do CLI i konfiguracja wstępna / Introduction to CLI and pre-configuration

**To start with CLI connect to console port via Rollover Cable with RJ45/USB MicroB to COM1 connectors. Use Putty with mode Serial, Port 9600 and default serial settings (8 data bits, 1 stop bit, Flow Control: NONE)

## Modes:
1. User EXEC mode (default when entering CLI)
   - allows to see certain things
2. Privileged EXEC mode (command: enable)
   - allows to see configuration, restart device etc
3. Global configuration (command: configure terminal)
   - allows to configure device settings and save them
   
## Useful tricks:
- `*** ?` - shows all available commands
- `***?` - shows all available endings
- Cisco ISO CLI require you to only type this part of command that is unique between others ex: `enable` --> `en`  not "e" alone because there are two options: `enable`, `exit`; `configure terminal` --> `conf t`; etc.
- Cisco ISO CLI also autocompletes commands with TAB key.
- `exit` - to exit global conf
- `end` - to exit global conf for interfaces etc
- `do [your_commands]` - use in global config mode when executing privileged exec commands ex: do sh run - to show running config file
- `no [command]` - disables command from running config

*Note: sht. - short version of commands

## Config files:
`running-config` - configuration of device running right now
`startup-config` - configuration to be loaded upon restart
--Commands:
`show running-config` (sht. `sh run`) - shows running config
`show startup-config` (sht. `sh start`) - shows startup config
`write` / `write memory` / `copy running-config startup-config` - all 3 save running config to startup config (sht. `wr`)

## Passwords (in global configuration):

`enable password [your_password]` (sht. `ena p` / `enable pass`) - adds password to enter exec mode and configuration (Warning!! is not secure. Use only with encryption below)

`service password-encryption` (sht. `ser p` / `serv pass`) - encrypts you passwords in running-config file. Encryption is Cisco type 7 encryption that is very easy to break, but is still better than plain text Does not affect secret bellow. Disabling will only affect future passwords.

`enable secret [your_secret]` (sht. `ena s` / `enable sec`) - creates secret that is MD5 encrypted and is not dependent on password encryption shown above in running config. Is the most secure so is recommended. Number of this encryption in Cisco ISO is 5.

**When secret and password are enabled only secret is prompted to enter privileged mode. Password is simply ignored.
