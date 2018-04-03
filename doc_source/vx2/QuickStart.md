# Quick Start

## Requirements
* Web browser  
Google Chrome or Firefox  
* serial connection application  
* SSH client  

## Preparation
Connect AC adapter and power on automatically  

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
    1. Click restart on the upper red line  
![restart1](/image/webui/restart1.png)  
    1. Click Run button on Reboot  
![restart2](/image/webui/restart2.png)  
    1. Click Run button  
![restart2](/image/webui/restart3.png)  
    1. Click OK on pop up  
![restart3](/image/webui/restart4.png)  

## Login  
In case of setting as DHCP client, you need to confirm IP address with serial port connection before login on Web UI or SSH connection.  
In addition, in case of using Wireless LAN, you also need to change Wireless connection settings of your PC.  

### Login on Web UI  
1. Access with Web browser  
    HTTPS : https://[IP address]:4430  
    HTTP : http://[IP address]:880  
1. Input Username and Password, and then, click Login button  
![login](/image/webui/login.png)  
transit to dashboard screen  
![dashboard](/image/webui/dashboard.png)  

### Login information for serial port connection or SSH connection  
Login : root  
Password : 0BSI0T  

#### Serial port connection  
1. Connect with USB console cable  

1. Setting serial connection as following  
Baud rate : 115200bps  
Data length : 8bits  
Parity : None  
Stop : 1bit  

1. Connect with serial connection client  

#### SSH connection  
1. SSH settings  
In case you use SSH connection, you need to enable SSH connection.  
[System] -> [Filter] tab  
![filter](/image/webui/filter.png)  
Check "Enable open setting of filter after reboot too.", if you want to enable SSH connection even after rebooting.  

1. Connect with SSH client  

## Reset
1. Connect with serial client and reboot  
1. Select **OBS IoT VX - WebUI init boot** on GRUB menu  

## Next Step

* [How to get BLE beacon data](/doc_source/vx2/HowToGetBLEBeaconData.md)
* [How to create custom PD-Handler with Node.js](/doc_source/vx2/HowToCreateCustomPdHandlerWithNodejs.md)

## Reference
* [OpenBlocks IoT Web UI Setup Guide]()
