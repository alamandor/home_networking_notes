# Networking For Beginners

## Basic Router Setup

*You should get assistance from the router's manual for this*
* Connect modem with ethernet cable, to the WAN port of the router
* Connect LAN port from the router to a computer's ethernet port
* Open browser, navigate to 192.168.1.1, possibly 192.168.0.1
* Default gateway: 192.168.1.1 possibly 192.168.0.1, please consult your manual
* Subnet Mask: 255.255.255.0
* To enable WIFI, set up Wireless Network, it's recommended that you set up WPA-2 Personal Security.

## Wireless Setup

*It is recommended that use a wireless scanner for this step. WiFi Analyzer for Android*

## How to determine what settings to use for your wireless network:
* 2.4GHz, use it for range and device comparability
* 5GHz, use it for speed/bandwidth, minimize interference with other signals
* After scanning your area with a WiFi tool, determine what channels are being used by neighboring networks
* You want to set your WiFi on a different channel as to minimize interference, while at the same time choosing the highest channel available. For instance if you see someone on channel 9, you want to set your WiFi on channel 10 or 11.
* Higher channels offer slightly better performance. If there are no other wireless networks, choose a high channel number.*

*Additionaly, and as pointed out by /u/v-_-v on his post bellow, there are only three channels on the spectrum that do not overlap. These being channels 1, 6 and 11. Therefore it is also suggested that if possible, to simply choose these channels. Unless of course these are overused where you live. For more information on this topic, please read the comment referred.*

## Advanced Setups

#### Terms to keep in mind:
* DHCP Server- this is used by the router to automatically assign addresses to the various connecting devices.
* Static IP- an assigned address that does not change.
* QoS- used to prioritize network traffic.
* DMZ- allows all traffic to bypass the router's firewall. Do not enable this unless you know exactly what you're doing.
* Port Forwarding- specifies what port to allow traffic through. Please check out portforwarding.com for extensive help with this, including hundreds of router guides.

### Connecting Two Routers to Expand Your Network

There are several ways to do this, and there are several goals to keep in mind when doing so. Here's the run down to the most typical set ups.

Keep in mind that some routers offer "Routing Modes." This can make configuration easier. Please refer to your user's manual.

#### Wireless Access Point

* This is used to connect two routers with a cable. All connected devices can see each other on the local network, regardless of what router they are connected to.
* Connect ethernet cable from the primary router(default gateway) LAN port, to a LAN port on the secondary router(Access Point)

__On the secondary router:__
* Disable DHCP, your primary router will handle this task
* Subnet Mask must be the same as Primary Router

#### Repeater Bridge
* Used to connect two routers wirelessly. Recommended only if you cannot run a wire to the second router. Devices connected to either network can see each other on the local network.
* You can follow a similar set up as a Wireless Access Point. However your second router needs to be able to connect to the primary router via WiFi.
* Assign a Static IP on your primary router, to the secondary router, usually 192.168.1.2 or 192.168.0.2 (must match the primary router's subnet). This becomes the local IP on the second router allowing you to connect to it's configuration page.

__On the secondary router:__
* Disable DHCP, your primary router will handle this task
* Subnet Mask must be the same as Primary Router

#### Client Bridge
* The goal here is to connect a second router and therefore create a second network. Devices connected to either router, cannot see devices on the other router on the local network. The keyword here is "subnetting."
* Connect ethernet cable from LAN on the primary router to WAN on the secondary router.

__On the secondary router:__
* Default gateway is the primary router's IP address. (192.168.1.1 for example)
* Local IP must be a different subnet. If the primary router's IP is 192.168.1.1, then this secondary router must be 192.168.2.1. You can further subnet routers down the network to further create more and more networks.
* You must enable DHCP. Since this is a new network, the new router needs to assign addresses on the new subnet.
* DNS can be let up to the default gateway/primary router.

## FAQ

- How can I improve my router's performance?

- You may want to consider installing 3rd party software on your router. A popular solution being DD-WRT. Check out /r/DDWRT. Others to consider, Tomato and if you have and Asus router check out Merlin.

- Be aware that this may void your router's warranty or possibly brick it if incorrectly done.

 ### How to I set up Port Forwarding?

- As mentioned above, please check out portforwarding.com. They have hundreds of guides specific to hundreds of router models.
