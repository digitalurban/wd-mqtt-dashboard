# MQTT Weather Dashboard 

Dashboard to display environmental data from Weather Display MQTT Output - the code is editable for other MQTT feeds.

![Screen](https://github.com/ucl-casa-ce/wd-mqtt-dashboard/blob/master/Screenshot%202020-01-20%20at%2011.49.16.png)

The dashboard builds on the paho.mqtt.javascript file https://github.com/eclipse/paho.mqtt.javascript with the addition of decoding of the MQTT feed.

## Requirements


Requires an MQTT Broker - such as Mosquitto  - see https://obrienlabs.net/how-to-setup-your-own-mqtt-broker/ 
Weather Display (http://www.weather-display.com/index.php) with MQTT set to publish (setup/advanced/LEDSignMQTT) - put in your broker details, tick send MQTT data - press 'test send'. 

You should see the data coming into your MQTT feed. 

Note - MQTT Box is a good option to check and monitor feeds (http://workswithweb.com/mqttbox.html).

The dashboard uses Weather Icons - download from https://erikflowers.github.io/weather-icons/ and copy the folder to your web server.

### Setting up files 

Edit mqttwd_dashboard.html  to reflect you own MQTT broker details as per the comments

var host="your mqtt broker"; //Add in your broker address
var port=9001; //normally 9001

Copy the file to your webserver mqttwd_dashboard.html 
Copy dashboardmqtt.css to your css folder (most likely /css). Change the path accordingly to match your settings.

Your page will update when any MQTT is received.


