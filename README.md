**OLA trigger configs to be used with Broadlink RM 3 Mini or RM 4 Mini to send infrared commands using DMX (Art-Net, sACN or via DMX input)**  
Contact me for support if you wish to use [LIRC](https://www.lirc.org/) or [PiIR](https://pypi.org/project/PiIR/) instead or need support to add another remote control.




**Requirements**

* [OLA](https://www.openlighting.org/ola)
* [Node-RED](https://nodered.org)
* [simple-broadlink node](https://flows.nodered.org/node/node-red-contrib-simple-broadlink) **
* [curl](https://curl.haxx.se)
* [Broadlink RM 3/4 Mini device](https://www.ibroadlink.com)

  
** = It seems that installing the node via the palette in Node-RED is not functioning correctly.  
Install it from the terminal in your .node-red directory using the following command:  
`npm install --no-audit --no-update-notifier --no-fund --save --save-prefix=~ --omit=dev --engine-strict node-red-contrib-simple-broadlink@0.0.8`  

**Available config files:** 

* [Uyuni Lighting LED candles](uyuni/uyuni.conf)
* More is coming soon...  

**Installation**

* Setup your Broadlink RM 3/4 Mini with the official app and connect it to your local network
* Download the config.conf and edit the hostname/IP address to match your Node-RED instance's address
* Download the [ir-remote.json](ir-remote.json) file, import it into Node-RED and edit the hostname/IP address to match your Broadlink RM 3 Mini's address

[OLA trigger documentation](https://www.openlighting.org/ola/advanced-topics/ola-dmx-trigger/)

**Usage** 

* Before running ola_trigger, make sure that olad is running and the universe has been configured with a DMX512 source.  
The config file is provided on the command line:

`ola_trigger config.conf`

**DMX protocol** 

Check the actual config file for the DMX Protocol.  

![Uyuni LED candles and Broadlink RM3 Mini](https://raw.githubusercontent.com/gobo-ws/ola-trigger-ir-dmx/main/images/uyuni.webp)
