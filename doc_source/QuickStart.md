# Quick Start
## Requirements
* Web browser  
Google Chrome or Firefox  
* serial connection application  
* SSH client  


## Preparation
connect AC adapter and power on automatically  

### Connection with Wireless network  
1. Connect with the following information  
SSID : iotfamily_***SERIAL_NUMBER***  
Password : openblocks  

    ***SERIAL_NUMBER*** is on back of the body.

1. Access with Web browser  
    HTTPS : https://192.168.254.254:4430  
    HTTP : http://192.168.254.254:880  

### Connection with wired network  
1. Connect with ethernet cable  

1. Set IP address to client as following  
192.168.253.0/24(except 192.168.253.254)  

1. Access with Web browser  
    HTTPS : https://192.168.253.254:4430  
    HTTP : http://192.168.253.254:880  


## Initial Settings

1. License Agreement  
Scroll to the end of screen and read contents.  
If you accept license, select [Agree].  
![License](/image/webui/license.png)

1. Web UI Administrator Account Settings  
Input username and password and click [Save].  
![account](/image/webui/account.png)

1. Network Settings  
![network](/image/webui/network.png)  
Set Wireless LAN and/or Ethernet you use.  
    1. Wireless LAN  
![wirelesslan](/image/webui/wirelesslan.png)

    1. Ethernet  
![ethernet](/image/webui/ethernet.png)

1. Reboot  
Reboot for applying settings.  
    1. click restart  
![restart1](/image/webui/restart1.png)  
    1. push Reboot Run button  
![restart2](/image/webui/restart2.png)  
    1. click OK on pop up  
![restart3](/image/webui/restart3.png)  

## SSH settings
### enable SSH connection  
In case you use SSH connection, you need to enable SSH connection.  
[System] -> [Filter] tab  
![filter](/image/webui/filter.png)  
Check "Enable open setting of filter after reboot too.", if you want to enable SSH connection even after rebooting.  

## Login  
### Login information  
Login : root  
Password : 0BSI0T 

### serial port connection  
1. Connect with USB console cable  

1. Setting serial connection as following  
Baud rate : 115200bps  
Data length : 8bits  
Parity : None  
Stop : 1bit  

### SSH connection  
#### connect with SSH client  
In case you set DHCP at IP address setting, you need to confirm IP address with serial port connection before SSH connection.  


## Next Step

* [How to get BLE beacon data]()
* [Hands-on to create custom handler]()

## Reference
* [OpenBlocks IoT Web UI Setup Guide]()
