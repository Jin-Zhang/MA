#### MAC Address

**MAC Address** means _Media Access Control or Medium Access Control_. Or it is called the physical address, hardware address, is used to define the location of network device. In the OSI model, the network layer (OSI Layer 3) is responsible for the IP address; the data link layer is responsible for the MAC address. Therefore, a media interface has a MAC address and an IP address in network. The network interface controller (NIC) determines the MAC address, and it is fixed. (Belongs to the device)

MAC address used hexadecimal digits separated by hyphens (-) or by colons (:) , a total of six bytes (48 bits). Actually MAC address is the adapter address or adapter identifier EUI-48. It is divided into the first three octets and the following three octets:  
* The first three octets, is called Organizationally Unique Identifier, namely OUI. It is assigned to different manufacturers, Which have registered in IEEE, to distinguish the devices of the different manufacturers.  
* The following three octets, is assigned by the manufacturers themselves, called Extended Identifier. For the same manufacturer, it is also different.  

Talking MAC address, we have to say about IP address(see next the section). For complete the communication，IP address worked on the network layer, the packet is forwarded from one network to another network; MAC address worked on the data link layer, a frame is transmitted from one node to another one in the same link. In a stable network, IP address and MAC address are a pair. So IP address and MAC address make a correspondence. This mapping between IP address and MAC address has done by the ARP(Address Resolution Protocol).  
The difference between MAC address and IP address:  
The same with MAC address and IP address is unique, but the different characteristics are:  
* On the same device or a computer, The change of the IP address is easy (but it must be unique). The MAC address was made by the manufacturer, generally can not be changed.   
* Different length. The length of IP address is 32 bits, MAC address is 48 bits.  
* Different assignment rules. IP address based on the network topology, MAC address based on the manufacturer.  
* Different OSI layer for the addressing 


  

