# How To Get BLE Beacon Data

## Overview
This documentation shows how to get BLE beacon data.  
Data flow is below:  
PD Handler BLE C -> PD Repeater -> Node-RED

## Preparation
* [Quick Start](/doc_source/vx2/QuickStart.md)  
* [How To Use Node-RED](/doc_source/vx2/HowToUseNodered.md)  

## Settings
1. Bluetooth settings  
    1. Move to [Service] -> [Basic] tab  
    Click **Basic functions** Link  
    ![service_basic](/image/webui/service_basic.png)  
    transit to below screen  
    Check if **To be use** is selected  
    ![basic_bt_if](/image/webui/basic_bt_if.png)  
    Check if the hci is **up** on the [State] tab  
    ![basic_state](/image/webui/basic_state.png)  
    1. Check Bluetooth HCI  
    Move to [BLE registration] tab and click BLE device detection button  
    ![basic_ble_registration](/image/webui/basic_ble_registration.png)  
    After detection time, transit to below screen  
    If devices are displayed as below, Bluetooth HCI works properly  
    ![basic_ble_registration_after_detection](/image/webui/basic_ble_registration_after_detection.png)  

1. IoT data control settings
    1. App settings
        1. Move to [Service] -> [Basic] tab and click **IoT Data** Link  
        ![service_basic_iot_data](/image/webui/service_basic_iot_data.png)  
        transit to below screen  
        ![iot_data_app_settings_default](/image/webui/iot_data_app_settings_default.png)  
        1. Check **The default use application mode display** on Application Start-up control  
        1. Select **To be use** on Default Application Start-up control -> **PD Repeater**  
        1. Select **To be use** on Default Application Start-up control -> **PD Handler BLE**  
        1. Select **To be use** on Application Start-up control -> **PD Repeater**  
        1. Select **To be use** on Application Start-up control -> **PD Handler BLE**  
        1. Click **Save** button on Operation  
    1. Tx/Rx settings
        1. Move to [IoT data] -> [Tx/Rx setting] tab  
        ![iot_data_tx_rx_setting](/image/webui/iot_data_tx_rx_setting.png)  
        1. Select **To be use** on Tx/Rx setting -> **UNIX domain socket(lsocket)**  
        ![iot_data_tx_rx_setting_lsocket](/image/webui/iot_data_tx_rx_setting_lsocket.png)  
        1. Edit the value of **Interval[sec]**  
        60 -> 0  
        1. Check **To be use** on Beacon transmission settings
        ![iot_data_tx_rx_setting_beacon](/image/webui/iot_data_tx_rx_setting_beacon.png)  
        1. Edit the value of **Duplication control time interval[msec]**  
        60000 -> 0  
        1. Check **lsocket** on Beacon transmission settings -> Tx/Rx setting
        ![iot_data_tx_rx_setting_device](/image/webui/iot_data_tx_rx_setting_device.png)  
        1. Click **Save** button on Operation  

1. Node-RED settings  
    1. Drug and drop **ipc** node from **input** to flowsheet  
    ![nodered_ipc](/image/webui/nodered_ipc.png)  
    1. Double click **ipc** node  
    ![nodered_ipc_edit](/image/webui/nodered_ipc_edit.png)  
    1. Edit as belows and push **Done** button 
    ![nodered_ipc_after_edit](/image/webui/nodered_ipc_after_edit.png)  
    1. Drug and drop **debug** node from **output** to flowsheet  
    ![nodered_debug](/image/webui/nodered_debug.png)  
    1. Connect **ipc** node and **debug** node  
    ![nodered_ipc_debug](/image/webui/nodered_ipc_debug.png)  
    1. Click **Deploy** button  
    1. Click **debug** tab on right side   
    ![nodered_finish_settings](/image/webui/nodered_finish_settings.png)  
    If successful, JSON data will be displayed on **debug** tab  

## Reference
* [OpenBlocks IoT Web UI Setup Guide]()
