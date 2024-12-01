# home network and servers for automation

## overview

1. the modem
2. the router
3. the PoE switch
4. the access points
5. the home server
6. automation bits for the home

## networking

this guide is focused on setting up a DOCIS based network, using a nice TLD as the primary internal/external address for simplicity of routing.

### modem

this is one of the simplest bits, an [Arris S34](https://www.surfboard.com/products/cable-modems/s34/) is my go to. it has a 2.5 Gbps port so should work for any soon to come or current DOCIS based speed. one important factor to consider is the signal strength on the actual co-ax cable, this can be measured by the installing tech.

### router

i personally built a router, but buying a [netgate 4200](https://shop.netgate.com/products/netgate-4200-base-pfsense-security-gateway) is a very simple solution. if you want to build your own i recommend:

1. intel atom MB
2. 16 gb ECC ram
3. 2u rack mount case
4. high write throughput SSD
5. platinum level PSU
6. PCI 10gb NIC

expect the cost to go into the $1500 range. from there you'd install pfSense and go from there

#### pfSense network level ad blocking

this can be done via [pfBlockerNG](https://www.zenarmor.com/docs/network-security-tutorials/pfblockerng). this will give you incredibly nice network level blocking of all of these types of tracking and ads.

### poe switch

i personally love aruba's instant on series, a 24 port with a few highspeed ports is the way to go, [1930 series PoE+ 24port switch](https://www.newegg.com/hpe-networking-instant-on-jl683b-aba/p/0XP-002G-02ND0?Item=0XP-002G-02ND0) is what i have, but it does not have anything other than SFP ports, which is probably fine. this will totally allow you to have super high speed APs and then you can also do IP cams easily.

### access points

the aruba instant on [AP22](https://www.newegg.com/p/0ED-00K0-00003) is a killer wifi 6E AP, they will have wifi 7 at some point, but wifi 7 is mostly consumer focused so enterprise APs have almost no reason to build it fast. these APs do a few wonderful things for free out of the box:

1. many networks at once, i have a high compatibility 2.4 Ghz network for IoT
1. a guest network fully divorced from the primary. it also let me configure the guest network to be funny as hell and redirect the end user to 'never gonna give you up' post login which is awesome
1. ability to connect hundreds of dedicated IOT devices without issues
1. any AP will do this, but being able to spread them accross the house will also allow fancy things like a pool WiFi smart controller, path lights and more. 

## server

### applications

### home automation

## smart devices