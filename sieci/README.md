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

# Notatka 2: Cables and interfaces

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
