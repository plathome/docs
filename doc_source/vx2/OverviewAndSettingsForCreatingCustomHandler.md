# Overview And Settings For Creating Custom PD Handler

## Preparation
* [Quick Start](/doc_source/vx2/QuickStart.md)
* [How To Use Node-RED](/doc_source/vx2/HowToUseNodered.md)  

### Point for creating PD Handler
For creating custom PD Handler, only 3 steps are necessary.
1. Get data from devices
1. Create JSON data
1. Send JSON data to PD Repeater with abstract UNIX domain socket

## Settings
1. For user device settings  
    1. Move to [Service] -> [Basic] tab and click **Basic functions** Link  
    ![service_basic_iotdata_nodered](/image/webui/service_basic_iotdata_nodered.png)
    1. Move to [User Dev. regist.] tab  
    ![basic_udr_default](/image/webui/basic_udr_default.png)
    1. Write **User Note** on User device and click **Save** button on Operation  
    Remember and note **Device number** on List
    ![basic_udr_after_settings](/image/webui/basic_udr_after_settings.png)
1. IoT Data settings  
    1. Move to [IoT Data] -> [App settings] tab  
    1. Check **Display the default application start-up control settings menu** on Application Start-up control  
    1. Select **Enable** on Default Application Start-up control -> **PD Repeater**  
    Select **Disable** on the others
    1. Select **Enable** on Application Start-up control -> **PD Repeater**  
    Select **Disable** on the others
    1. Click **Save** button on Operation  
    ![iotdata_app_only_repeater](/image/webui/iotdata_app_only_repeater.png)
    1. Move to [Tx/Rx settings] tab  
    1. Select **Enable** on Tx/Rx settings -> **UNIX domain socket(lsocket)**  
    1. Edit the value of **Interval[sec]**  
    60 -> 0  
    1. Select **Enable** on Device setting(user definition)
    1. Check **lsocket** on Device setting(user definition) -> Tx/Rx setting
    1. Click **Save** button on Operation  
    ![iotdata_txrx_lsocket_userdev](/image/webui/iotdata_txrx_lsocket_userdev.png)
1. Node-RED settings  
    1. Move to [Node-RED] tab and click **Link** button on Operation  
    1. Drug and drop **ipc** node from **input** to flowsheet  
    ![nodered_ipc](/image/webui/nodered_ipc.png)  
    1. Double click **ipc** node  
    ![nodered_ipc_edit](/image/webui/nodered_ipc_edit.png)  
    1. Edit as belows and push **Done** button 
    ![nodered_ipc_after_edit_for_custom_handler](/image/webui/nodered_ipc_after_edit_for_custom_handler.png)  
    1. Drug and drop **debug** node from **output** to flowsheet  
    ![nodered_debug_for_custom_handler](/image/webui/nodered_debug_for_custom_handler.png)  
    1. Connect **ipc** node and **debug** node  
    ![nodered_ipc_debug_for_custom_handler](/image/webui/nodered_ipc_debug_for_custom_handler.png)  
    1. Click **Deploy** button  
    1. Click **debug** tab on right side   
