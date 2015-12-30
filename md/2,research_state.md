### The discussion for the indoor positioning technology based on wireless technology

With the rapidly increase of data/multimedia service and the growing demand for positioning and navigation (especially in complex indoor environments, such as airports, exhibition halls, supermarkets, libraries, etc.) mobile terminals needs to be identified with indoor location information. But because of the restrictions of the positioning time, the positioning accuracy and complicated indoor environment, a relatively complete positioning technology is still unable to be used efficiently. A vast number of solutions of indoor positioning technologies were proposed by network experts.


1. Indoor GPS technology  
GPS, Global Positioning System, currently the widely spread positioning technology. When the GPS receiver used indoor, due to the influence of the building, the signal is greatly attenuated, so the positioning accuracy is poor. There is no method to get equal performance as the outdoor navigation with extraction of the navigation data and time information from the satellite broadcasting in a straight way. In order to obtain higher signal sensitivity, the residence time of the delay on each waypoint needs to be extended.   
A-GPS (Assisted GPS) technology offers the possibility to solve this problem. A-GPS is the convergence technology between GPS technology and the wireless cellular technology. The mobile terminal has not to download and decode the navigation data from the GPS satellites, receives directly the positioning information of the aid from the mobile network and there is no need to decode the timing measurement.
The advantage of GPS is the wide and effective coverage and the accuracy of the positioning signal and navigation signal. The disadvantage of the GPS is the limitation by indoor usage and the high cost of the terminal.  
 

2. Infrared positioning technology  
The principle of infrared positioning technology as another method, with an infrared beam sends the infrared radiation, positioning depends on the optical sensor, which receives the infrared radiation. While infrared has a relatively high positioning accuracy, but the light cannot pass through the obstacle, so that the infrared is only the sight propagation. The straight sight and the short transmission distance are the two major disadvantages of infrared positioning, it makes the poor effect of the positioning. When the infrared is blocked by pocket or wall, it will not work properly, so needs to install the receiving antenna in each room and corridor. The costs in total are higher. Therefore, the infrared method is only suitable for short-distance transmission, it has limitations on the precise positioning.  

3. Ultrasonic positioning technology  
Ultrasonic positioning technology uses the mainly reflective odometry to determine the position of an object through triangulation algorithms. It is achieved by emitting ultrasonic waves and receiving the echoes from the measured object, according to the time difference between the echo and transmission wave, it is possible to determinate the distance with a sequential calculation. The ultrasonic positioning system consists of several transponders and a main rangefinder. With the main rangefinder targeting on the measured object, the computer command emits the radio signal of the same frequency to transponders in fixed locations. After transponders receive radio signals, ultrasonic signals were simultaneously transmitted to the main rangefinder to get the distance between the main rangefinder and each transponders. When three or more than three transponders aren’t in the same straight line, it is possible to calculate and determine the position of the object in the two-dimensional coordinate system. Ultrasonic Positioning has the higher positioning accuracy and simple structure, but ultrasound makes the great influence by multi-path effects and needs higher priced investment for the basic hardware facilities.    

4. Bluetooth technology  
Bluetooth technology is a wireless transmission technology of short-distance and low-power consumption by measuring the signal strength for positioning. The appropriate Access Points of Bluetooth LAN have been installed, the network is configured to the connection mode of basic network based on a multi-user. The Access Points are always the master device in the piconet, it can obtain the user's location information. Bluetooth technology is mainly used in small-scale positioning, such as single hall or warehouse. The biggest advantage of Bluetooth technology is the small circuit, it is easy to integrate in PDA, PC and mobile phone, so it is easy to popularize for many adopters. In theory, as long as the Bluetooth device is turned on, it is possible to determine its position. On the other hand, the price of Bluetooth devices and equipment is higher (also it is unstable in complex environments with influence of noise frequencies).    

5. Radio frequency identification technology (RFID)  
RFID technology uses radio frequency mode for the data exchange non¬-conductive and bidirectional communications, mainly purpose of identifying and positioning. Part of this technique is short distance transmission, usually a few metre. But it can obtain the information of the positioning accuracy within milliseconds, and the transmission range is large and low cost. The problems for the controversial and difficult research of RFID positioning technology are to establish the theoretical propagation model, the user's privacy and security aspects and international standardization.   

6. Ultra-wideband technology  
Ultra-wideband technology is a new communication technology, which has huge differences with traditional communication technologies. It doesn’t need to use the Carrier in conventional communication systems, by the sending and receiving of ultra‐short pulses within nanosecond duration to transmit data in the GHz bandwidth. UWB systems compared to conventional narrowband systems, brings better penetration, lower power consumption, better resistance to multipath effects, more safety, lower system complexity and more precise positioning accuracy. Therefore, Ultra-wideband technology can be used for location tracking and indoor navigation for stationary or moving objects and people.    

7. ZigBee technology  
ZigBee is a new short-range and low-rate wireless network technology. It falls in between RFID and Bluetooth, and can also be used for indoor positioning. It has its own radio standards, with communication between thousands of tiny sensors with each other apportioned in different spots in order to achieve precise positioning. The energy demand of these sensors is very small, utilizing a relay way to transmit the data by radio waves from one sensor to another sensor, it increases the communication efficiency. The main significant technical features of ZigBee are low power consumption and low costs.    

8. Wi-Fi technology  
Wi-Fi is a wireless interconnection technology for PC, handheld devices and other mobile or stationary terminals. It is a trademark of wireless network communication technology, which belongs to the Wi-Fi Alliance. Hotspots are areas，where a wireless network (WLAN) is available，these access points to the Internet are installed mostly in bars, hotels, airports, train stations or even in public places. Any place, where people open the mobile terminal, can get free access to the Internet via Wi-Fi. For these reasons，Wi-Fi technology is a new platform for information collection that can implement the complex positioning, monitoring and tracking tasks in a wide range. The positioning of the network node is the basis and premise for most applications, using wireless LAN standards IEEE802.11. It is easy to install, less base stations and using the same structure in underlying wireless network.    

Except the above-mentioned positioning technologies, which are available to public, as well as computer vision, optical tracking based on image analysis, magnetic field and military beacon, more technologies are still in the experimental stage.    

### The purpose of the application in thesis
Due to the popularity of Wi-Fi, the application, which will be implemented in this thesis, is based on Wi-Fi and hotspot technology.  
It´s developed as "Guidance system" for mobile devices to evacuate people from buildings. The application runs on mobile terminal without any additional software or APP, requires only the web browser. In case of an emergency, the web page through HTTP Redirect technology opens a navigation page. The following paragraphs focus on positioning in the Wi-Fi environment. There are several methods as location information in Wi-Fi environment.


#### IP address  
The IP address of device is automatically distributed through DHCP to connect to AP. If the IP address is used in the different address segment by any APs, it can determine the IP address area of the AP for the terminal. According to the different IP address, the connected AP can be found.   
* Advantage：  
No installation of additional software and hardware required. It is suitable for the web application.    
* Disadvantage:  
In fact, the installation process of the wireless network has a lot of possibilities, it is no universal and feasible method, using only the IP address to find the connected AP. Because in the mobile IP mechanism, the device might remain the same IP address in the different AP area. In this situation, the connected AP cannot be determined by device, we need to get the Care-of address for better adjustment as well.   

#### Signal strength of the communication between the device and AP  
By the described principle of triangulation the position is detected with three different points, makes a use of triangular geometry to determine the position and the distance. Wireless Triangulation is a method for determining the location of wireless nodes with IEEE 802.11 standards. Usually it is implemented by measuring the received signal strength (RSS). Because of the multipath effects of the signal it is impossible to determine the accurate position, and it needs to calculate three individual signal strengths of the different AP.     

#### Authentication of the user
In many public Wi-Fi hotspots users need to authenticate before log in to the Internet, based on the centralized RADIUS server or IEEE 802.1X and providing centralized authentication, authorization, and accounting for the network access. The mobile device sends an authentication request to an AP, then it forwards the request to the RADIUS server. Further information such as the time, the AP's ID and the MAC address of the mobile device are stored in the RADIUS server to determine information, which AP a mobile device is currently associated with. Therefore, the method of the RADIUS depends on the RADIUS server and other protocols. It is only suitable for the use of authentication WLAN, and it is not suggested for web application because the MAC address of mobile device being recorded in RADIUS server.        

In summary，for indoor environment, a IEEE802.11 WLAN mainly consists of one or more Access Points (AP) to provide the wireless access service. Usually any mobile device connects to the AP with the strongest signal and the shortest distance.
Since the AP has been previously placed in a fixed location, it is possible to specify the location of the mobile device based on current information of the AP, which is connected to the mobile device. 
And I found that most of the current network devices with SNMP technology. This thesis presents the application based on web mode with combination of the WLAN technology and SNMP technology, using the location of AP to determine the position of the user's mobile device for sending the escape instructions.
 








