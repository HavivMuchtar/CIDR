# CIDR
# EXERCISE 1
![cidr subnet](https://user-images.githubusercontent.com/2261139/178157032-0758774f-9536-4563-8e75-8713b1ad5967.jpg)

# EXERCISE 2
<li>How a PC uses packets to retrieve a webpage</li>

![cn_purple_fig13](https://user-images.githubusercontent.com/2261139/178159351-5fb5361f-9f1a-42b6-8cf7-550787d1c19d.jpg)

<li>The user within the home LAN enters a URL such as www.bbc.co.uk into the browser on their PC, which has an IP of 192.168.0.101. The PC then creates an IP packet addressed to the local DNS server, as it needs to resolve the correct IP address for the BBC web server:</li>

![cn_purple_fig14](https://user-images.githubusercontent.com/2261139/178159377-da4b8c0d-1192-4d2b-babe-54893d8bfa22.jpg)

<li>The packet uses the IP address of the home PC as its source and the IP address of the DNS server as its destination. The packet contains a request from the DNS for the IP address of the BBC web server. Note that the ‘type’ field of the packet identifies the User Datagram Protocol (UDP), which is responsible for segmenting the DNS request so that the IP can encapsulate it within a packet.</li>
    <li>The PC identifies that the packet is leaving the LAN, as the source and destination networks are within different IP networks, so it forwards the packet towards the default gateway it has learnt via DHCP: 192.168.0.1, which is the LAN interface of the home router.</li>
    <li>The router examines its routing table, which identifies all the IP networks the router can forward packets to. It is then able to identify an exit interface to use in order to forward the packet towards the destination network identified in the packet.</li>
   <li> The packet may be required to pass through multiple routers, but it eventually arrives at the DNS server, which examines the DNS request and identifies the IP address that maps to the URL. It then creates a new packet containing a response, which is forwarded back to the home PC:</li>
   
   ![cn_purple_fig15 small](https://user-images.githubusercontent.com/2261139/178159410-21ad404d-3b1c-4b97-a353-2d386407233a.jpg)
   
<li>The packet returns to the home router, which forwards it to the PC. The PC now has the correct IP address for the URL it wishes to contact, so it can construct a new packet containing the web server as a destination and carrying an HTTP GET message requesting webpage content. Note that the protocol type has changed to Transmission Control Protocol (TCP). Like UDP it performs segmentation, but also provides reliability mechanisms to protect against data errors if packets are lost or damaged during transmission.</li>

   ![cn_purple_fig15 small](https://user-images.githubusercontent.com/2261139/178159419-eab0487b-c123-4e50-a662-4f3fbab5839c.jpg)
   
   <li>Once again, the PC realises that the packet’s destination is not on the local LAN and forwards it to the home router, which in turn forwards the packet to the ISP and onto the Internet via its WAN interface. The packet passes through several routers as it heads towards the web server, with each router checking the destination address within the packet and forwarding appropriately.
    Once the web server receives the packet, it examines the GET message to see which particular page is required, and then returns the webpage as HTML within a series of packets addressed to the home PC:</li>

![cn_purple_fig17 small](https://user-images.githubusercontent.com/2261139/178159442-2ea90c50-c94d-4da0-910c-15eabf229da1.jpg)

<strong><u>Source:</u><strong> https://www.open.edu/openlearncreate/mod/oucontent/view.php?id=129584&section=7

*I hope that I understand the exercise.

# EXERCISE 3

![table](https://beetledigital.com/wp-content/uploads/2021/06/IPv4-Subnet-Mask-Cheat-Sheet.png)
