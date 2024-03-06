+++
title = 'Node-red'
date = 2024-03-05T18:19:09+08:00
draft = false
+++

### Install and Run

* Go to the Docker menu and install Node-red, if it is not there, click the add button to add.
* Click the RUN button to run the Node-red, keep parameters default.

![nodered1](nodered1.jpg)

### Open the webUI of Node-red
* After running, click the 'More info' to go to its detail page.
* Click the 'Show in new window' button upper right to open its web console on a new tab.

![nodered2](nodered2.jpg)

### Install the ewelink-cube palette
* On the Node-red page, click the menu upper right, click 'Manage palette'.
* Switch to 'Install' tab and search for 'ewelink-cube', install the 'node-red-contrib-ewelink-cube'.

![nodered3](nodered3.jpg)


### Get iHost access token
* Drag and drop the 'get-devices' node and 'debug' node, connect them.
* Double click on the 'get-devices' to edit.


![nodered4](nodered4.jpg)

* Click the edit button to add a new server.

![nodered5](nodered5.jpg)

* Enter your iHost IP and click the search button, then click 'GET TOKEN'

![nodered6](nodered6.jpg)

* Go back to iHost page and Click Allow.

![nodered7](nodered7.jpg)

* Click Add and select All device, save the settings.

![nodered8](nodered8.jpg)

* Add an 'inject' node and click the Deploy button upper right.

![nodered9](nodered9.jpg)

* Click on the inject node and you'll see the output under debug tab.

![nodered10](nodered10.jpg)

* For other nodes, you can switch to the info tab to check the description.

![nodered11](nodered11.jpg)




