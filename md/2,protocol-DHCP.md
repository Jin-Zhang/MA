#### DHCP
DHCP, Dynamic Host Configuration Protocol is a local area network protocol; typically it is used in large-scale local area network environment. The concentrated management and assignment of the IP address is the main task, to verify that the host can get a dynamic IP address, Gateway address, DNS server address and other relevant information, and enhance the utilization of the IP address.  

DHCP protocol uses a client - server model, it has three mechanisms for the assignment of IP address:  
*	Automatic Allocation, DHCP server allocates a permanent IP address for the host.  
*	Dynamic Allocation, DHCP server allocates the IP address with time limited for the host, as time expires, it can be used by other hosts.  
*	Manual Allocation, DHCP server allocates the IP address by the network administrator for the host.  

DHCP uses UDP as a transport protocol. The host sends a request message to the DHCP server in 67 port, DHCP server gets the response to the host's 68 port.

