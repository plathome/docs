# How to install an extension packages
Immediately after shipment,  
OpenBlocks IoT Family is installed only with software to set up network settings, etc.  
If there is a need to apply extensions for use as an IoT Gateway,  
it is possible to add supported packages using the [Maintenance]-[Enhancements] tab.

## Instruction

### 1. Open Enhancements menu  
Click [Maintenance]-[Enhancements] tab to open Enhancements menu
![Extensions1](/image/webui/extensions1.png)

### 2. Choose a package to install  
Choose a package to install from pull down menu and click the "Execution" button for installation.
![Extensions2](/image/webui/extensions2.png)
* To install software using this function, the unit must support an Internet environment.
* If the network connected to the Internet is slow, installation of package may take some time.

### 3. When click the Execution button
When click the Execution button, a confirmation window will be displayed.  
When the proper package is displayed, press the OK button to confirm selection.   
During installation, it is not possible to choose buttons.
![Extensions3](/image/webui/extensions3.png)
* After pressing the Execution button, a button to check the installation status will appear.  
Clisk this button to check on the progress of installation.

### 4. After installing
Regardless of whether an installation has been successful or not,  
a window will be displayed when the process is completed.  
If installation has been a success, press the OK button to accept the message.  
After installing an extension with this function, and as the system needs to be rebooted, restart the unit.
![Extensions3](/image/webui/extensions4.png)

## Troubleshooting
* If an installation failed, recheck Internet environment, etc., and execute installation again.
* Installing some packages may require the addition to sources.list and public keys of packages repository.

## List of available packages
packages available for installation from this function are as follows.

| Packages | Contents |
  ---------|---------
| Samba | WEB UI for Samba and a set of applications for file sharing. |
| IoT dada control | WEB UI for IoT data control and a set of applications. |
| Node-RED | WEB UI for Node-RED and a set of Node-RED. |
| Security | A set of functions that carry out access rejection, etc. against illegal access to WEB UI and SSH. |
| Camera | WEB UI for image capture by camera and image display / motion detection software. |
| Docker | Installs Docker DAEMON. |
| Moby | Installs Docker DAEMON, which build by Microsoft from Moby. |
| Docker (including WEB UI) | Installs a set of functions to control Docker containers, etc. from WEB UI. Docker DAEMON also installed. |
| Azure IoT Edge | Installs a set of Azure IoT Edge and WEB UI for setup. Docker DAEMON installation is required in advance. |

## Next Step

* [How to get BLE beacon data](/doc_source/vx2/HowToGetBLEBeaconData.md)
* [How to create custom PD Handler with Node.js](/doc_source/vx2/HowToCreateCustomPdHandlerWithNodejs.md)

## Reference
* [OpenBlocks IoT Family WEB UI Setup Guide](/docs/3.3/OpenBlocks_WEBUI_Guide_v3.3.0_Eng_20181206.pdf)
