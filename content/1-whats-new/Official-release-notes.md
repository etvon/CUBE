+++
title = 'Official Release Note'
date = 2024-03-05T17:50:29+08:00
draft = false
+++


#### V1.13.3 (2024.1.31)  

**Optimizations:**  
- Optimized the display of SNZB-06P detection time interval.  

**Bug Fixes:**  
- Fixed an issue where the volume list was empty in some cases.  
- Fixed an issue where Tailscale's UI could not be displayed in some cases.  

#### V1.13.2 (2024.1.23)  

**New Features:**  
- Custom language is available. Now your iHost can display in the language you want by uploading language files, check it under Settings menu.  

**Optimizations:**  
- Optimized the UI of the Smart Security page.  
- Optimized the firmware update process.  
- Added 'About' menu to installed add-ons page.

**Bug Fixes:**  
- Fixed the issue where add-ons couldn't load the Web UI.  
- Fixed the bug that Matter Bridge could not initialize after restarting iHost in muted state.  
- Fixed an issue where the names of devices synchronized via Matter Bridge changed after iHost was restarted.  

#### V1.13.0 (2023.12.26)

**New Features:**  
- Now you can drag and drop the scence actions to rearrange their order.  
- Support for adding SNZB-03P Motion Sensor, SNZB-04P Door/Window Sensor, and NSPanelP-Router.  
- Paral-sync add-on now supports SNZB-03P Motion Sensor, SNZB-04P Door/Window Sensor, SNZB-02D Temp.&Humi. Sensor, and TRVZB Thermostatic Remote Valve (please update Paral-sync add-on to the latest version on its detail page).  
- eWeLink Smart Home add-on now supports cloud control of some devices and LAN control of more sensor and light sub-devices of SONOFF Zigbee Bridge Pro. (please update eWeLink Smart Home add-on to the latest version on its detail page).

**Optimizations:**  
- Increased the limit of CAST dashboards to 10.  
- Optimized logic for adding, deleting, and synchronizing RF remote controllers in eWeLink Smart Home add-on.  
- Sidebar UI design optimized. Added an entry to open add-on page in a new window.

**Bug Fixes:**  
- Resolved the issue where the same device couldn't repeatedly be used as scene actions in a scene.  
- Fixed the bug where Temp.&Humi. sensors couldn't save 1 decimal place as scene triggers.  
- Fixed the occasional pairing issue with Matter Bridge.  
- Resolved the problem where device names changed in Matter-supported platforms after iHost was restarted.