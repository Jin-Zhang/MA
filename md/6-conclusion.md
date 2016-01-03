# Chapter 6. Conclusion

#### Summary
Because of the high speed, larger coverage and simple installation, Wi-Fi technology and WLAN technology are widely used, recently it has become an important part of life. The demand for location-based services grows rapidly. Wireless positioning technology is also increasingly concerned and applied to the various industries, the development of the positioning based on the Wireless technology is  possibility and necessary.  

This thesis describes the approach of design and implementation about "Guidance System" is also based on Wi-Fi technology and SNMP, by a practical web service for Mobile devices in WWW environments. The application implements that, though the MAC-to-IP address mapping, the network device of supporting SNMP finds the AP or wireless router, which directly is connected to a Mobile device of user. In case of an emergency, forwarding is turned on, the user's browser is redirected to a specified page. It contains also a graphical user interface for management. The management module can add and delete the managed network devices.



#### Future works
This thesis could be extended to several directions in the future:


Delay:   
Due to the differece of equipment leads to the delay in application, when a user roams from one AP to the next AP. Using the SNMP Trap might solve this problem, because managed device will send activly the notification to SNMP manager, instead of waiting for the SNMP manager to poll again. When the connection state changed, it should provide a real-time information for user. Further study is, how SNMP traps and the MAC-to-IP address mapping can be used together for supporting push services.


Management interface:  
Improve the management interface, make the administrator to manage simply the new added device and increased remote management capability.   

In the plan, using Django as the server, offers a Web Service interface for remote manipulating operations.

User Interface:  
Since there is no a determined escape scene, User page shows MAC address and IP address of the connected AP in the form of text. When the indoor environment is determined, through a graphical floor plan can mark out the current position and exit. A good user interface should be intuitive, can automatically adapt to different screen resolution.

Security：

There is no security measures concurrently in this project. But for a pratical use, security is definitive neccesary. For example, a hacker who want to make prunk may cause frightened in the people, or the terrorists could control the system and guide the LoYiW users to a danger zone. 

SNMP supports SNMPsec (Secure SNMP), shell command could be invoked using SSH(Secure SHell ), so it's possible the implement the secure measures.





1. 使用Traps 增加实时性
2. 测试不同的设备，找到一个可用于实际定位的设备组合
3. 解决加密问题
4. 完善管理界面，增加远程管理功能

### Test

This system should be test on plenty equipments.

### Traps

### Delay

When the connection state changed, the state of the devices should be updated.

### 
