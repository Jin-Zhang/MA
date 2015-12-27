### The discussion for the indoor location technology based on wireless technology 

With the rapidly increasing in data services and multimedia services, the increasing demand for positioning and navigation, especially in complex indoor environments, such as airport, exhibition halls, supermarkets, libraries, etc. The mobile terminal need to be identified with indoor location information. But because of the restriction of the positioning time, the positioning accuracy and complicated indoor environment, a relatively complete positioning technology is still unable to be good used. A number of solutions of the indoor positioning technology was proposed by Experts.


1. Indoor GPS technology  
GPS, Global Positioning System, currently it is the most widely used positioning technology. When the GPS receiver works in the room, due to the influence of the building, the signal is greatly attenuated, then the positioning accuracy is very low. It is impossible to achieve the same result as the outdoor, extracting the navigation data and time information from the satellite broadcasting directly. In order to obtain a higher signal sensitivity, the residence time of the delay on each code needs to be extended.  
A-GPS (Assisted GPS) technology offers the possibility to solve this problem. A-GPS is the convergence technology between GPS technology and  the wireless cellular technology. The mobile terminal has not to download and decode the navigation data from the GPS satellites, receives directly the positioning information of the aid from the mobile network and has not to decode for the timing measurement.  
The advantage of the GPS satellite positioning is the wide and effective coverage and the free of the positioning signal and navigation signal. The disadvantage of the GPS is the weak signal by the reaching the ground and the high cost of the terminal.  

2. Infrared positioning technology  
The principle of infrared positioning technology, the infrared of identification sends the infrared radiation, positioning depends on the optical sensor, which receives the infrared radiation. While infrared has a relatively high positioning accuracy, but the light can not pass through the obstacle, so that the infrared is only the sight propagation. The straight sight and the short transmission distance are the two major disadvantages of infrared positioning, it makes the poor effect of the positioning. When the infrared is blocked by pocket or wall, it  will not work properly, so needs to install the receiving antenna in each room and corridor. It costs higher. Therefore, the infrared is only suitable for short-distance transmission, it has limitations on the precise positioning.

3. Ultrasonic positioning technology  
Ultrasonic positioning technology uses the mainly reflective odometry to determine the position of an object through triangulation algorithms. It means emitting ultrasonic waves and receiving the echoes by the measured object, according to the time difference between the echo and transmission wave in order to calculat the distance. The ultrasonic Positioning System consists of several transponders and a main rangefinder. The main rangefinder places on the measured object, By the computer command emits the radio signal of the same  frequency to transponders in fixed position. After transponders receive radio signals, ultrasonic signals were simultaneously transmitted to the main rangefinder to get the distance between the main rangefinder and each transponders. When three or three more transponders respond during not the same straight line, calculate and determine the position of the object in the two-dimensional coordinate system. Ultrasonic Positioning has the higher positioning accuracy and simple structure, but ultrasound makes the great influence by multi-path effects and needs a lot of the investment for the basis hardware facilities.  

4. Bluetooth technology  
Bluetooth technology is a wireless transmission technology of short-distance and low-power by measuring the signal strength for positioning. The appropriate Access Points of Bluetooth LAN have been installed, the network is configured to the connection mode of basic network based on a multi-user. The Access Points are always the master device in the piconet, it can obtain the user's location information. Bluetooth technology is mainly used in small-scale positioning, such as single hall or warehouse. The biggest advantage of Bluetooth technology is the small device, it is easy to integrate in PDA, PC and mobile phone, so it is easy to popularize. In theory, as long as the Bluetooth device is turned on, it is possible to determine its position. The other side, the prices of Bluetooth devices and equipment is more expensive, but also stability of the Bluetooth system is slightly less for complex space environment, it makes the strong influence by the noise signal.  

5. Radio frequency identification technology (RFID)  
RFID technology uses radio frequency mode for the data exchange by non-contact and Bidirectional communications in order to achieve the purpose of identifying and positioning. The role of this technique is short distance, generally up to tens of meters. But it can obtain the information of the positioning accuracy within milliseconds, and the transmission range is large and low cost. The problems for the hot and difficult research of RFID is to build the theoretical propagation model, the user's privacy and security and international standardization.  

6. Ultra-wideband technology  
Ultra-wideband technology is a new communications technology, which has great differences with traditional communication technologies. 
It needs not to use the Carrier in conventional communication system, using by the sending and receiving within nanosecond or less nanosecond of the ultra‐short	pulses to transmit data, so as to have the GHz bandwidth. UWB systems compares with conventional narrowband systems, having penetration, low power consumption, good resistance to multipath effects, safety, low system complexity and the precise positioning accuracy. Therefore, Ultra-wideband technology can be used location tracking and navigation in indoor for stationary or moving objects and people.  

7. ZigBee technology  
ZigBee is a new short-range and low-rate wireless network technology. It falls in between RFID and Bluetooth, and also be used for indoor positioning. It has its own radio standards, coordinating communication between the thousands of tiny sensors with each other in order to achieve positioning. The energy demand of these sensors is very low, using a relay way to transmit the data by radio waves from one sensor to another sensor, so their communication efficiency is very high. The most significant technical features of ZigBee are low power and low cost.  

8. Wi-Fi technology  
Wi-Fi is wirelessly interconnection technology with PC, handheld devices and other mobile or non-mobile terminal, it is a trademark of  wireless network communication technology, belongs to the Wi-Fi Alliance. Hotspots are areas，where a wireless network (WLAN) is available，these access points to the Internet are installed mostly in bars, hotels, airports, train stations or even in public places. Anywhere people open the mobile terminal, can freely connect to the Internet via Wi-Fi. It is for these reasons，Wi-Fi technology is a new platform for information collection that can implement the complex positioning, monitoring and tracking tasks in a wide range. The positioning of the network node is the basis and premise for most applications, using wireless LAN standards IEEE802.11. It is easy to install, less base stations and using the same structure in underlying wireless network.  

Except the above-mentioned positioning technology, as well as computer vision, optical tracking, based on image analysis, magnetic field and a beacon positioning. Many technologies are still in the experimental stage.  

### The purpose of the application in thesis
Due to the popularity of WiFi，this application, which will be implemented in this thesis, is based on WiFi and hotspot technology, it is "Guidance system" for mobile devices in order to evacuate from the building for people. The application runs on mobile terminal without any additional software or APP, requires only the web browser. When an emergency occurs, the web page of user through HTTP Redirect technology to guide page. The following paragraphs focus on positioning in the WiFi environment. There are several methods as location information in Wi-Fi environment.

#### IP address  
The IP address of device is automatically distributed through DHCP to connect to AP. If the IP address is used in the different address segment by any APs, it can determine the IP address area of the AP for the terminal. According to the different IP address, the connected AP can be found. 
* Advantage：  
Without installation of additional software and hardware. It suitable for the web application.  
* Disadvantage:  
In fact, the installation process of the wireless network has a lot of possibilities,  it is not universal and feasible way, using only the IP address directly to find the connected AP. Because in the mobile IP mechanism, the device might remain the same IP address in the different AP area. In this situation, the connected AP cannot be determined by device, we need to also get the Care-of address for more judgment.  

#### Signal strength of the communication between the device and AP  
By principle of triangulation detects the position from three different points, and then uses the triangle geometric principles to determine the position and the distance. Wireless Triangulation is a method for determining the location of wireless nodes with IEEE 802.11 standards. It is normally implemented by measuring the received signal strength (RSS). Because of the multipath effects of the signal can not determine the accurate position, and it needs to calculate three signal strengths of the different AP.   

#### Authentication of the user
In many public Wi-Fi zone requires users to authenticate before using the Internet, based on the centralized RADIUS server or IEEE 802.1X and providing centralized authentication, authorization, and accounting for the network access. The mobile device sends an
authentication request to an AP, then it forwards the request to the RADIUS server. Such as the time, the AP's ID and the MAC
address of the mobile device are recorded in the RADIUS server in order to determine information, which AP a mobile device is currently associated with. Therefore, the method of the RADIUS depends on the RADIUS server and other protocols. It is only suitable for the use of authentication WLAN, and it is not good for web application because of using the MAC address of mobile device to record in RADIUS server. 
In summary，in the indoor environment, a IEEE802.11 WLAN is mainly composed of one or more of AccessPoint (AP) to provide the wireless access service. Usually any mobile device connects to the AP of the strongest signal and the nearest AP, since the AP has been previously placed in a fixed location, so we can determine the location Information of the mobile device through location Information of the AP, which is connected to by the mobile device. And I found that most of the current network devices with SNMP service.  
Therefore, this thesis presents the application based on web mode with combination of the WLAN technology and SNMP technology, using the location of AP to determine the positioning of the user's mobile device for getting the escape information. 








