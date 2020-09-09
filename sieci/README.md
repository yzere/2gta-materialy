# Materiały merytoryczne z lekcji CISCO

Tutaj zamieszczone zostają notatki z zagadnień CISCO w języku angielskim.



# Urządzenia sieciowe / Network devices

## Definition of Computer network:

A computer network is a group of computers that use a set of common communication protocols over digital interconnections for the purpose of sharing resources located on or provided by the network nodes. 

## Network devices:

![GitHub Logo](/media/network-devices.jpg)
Format: ![Alt Text](url)

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
