# How To Create Custom PD Handler With Node.js

## Preparation
* [Quick Start](/doc_source/vx2/QuickStart.md)
* [How To Use Node-RED](/doc_source/vx2/HowToUseNodered.md)  
* [Overview And Settings For Creating Custom Handler](/doc_source/vx2/OverviewAndSettingsForCreatingCustomHandler.md)  

## Overview
Development Language : ***Node.js***  
Target Device : ***BLE beacon***  

### Point for creating PD Handler
For creating custom PD Handler, only 3 steps are necessary.
1. Get data from devices
1. Create JSON data
1. Send JSON data to PD Repeater with abstract UNIX domain socket

## Create custom PD Handler
1. Preparation
```
apt install git  
git clone https://github.com/plathome/custom-pd-handler-for-ble-beacon-nodejs.git
cd custom-pd-handler-for-ble-beacon-nodejs
npm install
```

1. Get BLE beacon data
```
node get-ble-beacon.js
```

2. Create JSON data
```
node create-json-data.js
```

3. Send JSON data to PD Repeater with abstract UNIX domain socket
```
node send-to-auds.js
```

## Check with Node-RED
Access to Node-RED
If successful, JSON data will be displayed on **debug** tab
