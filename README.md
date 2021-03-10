# HomeAssistant Config


[![GitHub stars](https://img.shields.io/github/stars/alesus97/HA)](https://github.com/alesus97/HA)
[![GitHub last commit](https://img.shields.io/github/last-commit/alesus97/HA)](https://github.com/alesus97/HA/commits/master)
[![HA Version](https://img.shields.io/badge/Running%20Home%20Assistant-2021.3.x%20-darkblue)](https://github.com/home-assistant/home-assistant/releases/latest)
# Devices


| Device  | Image|Quantity | Connection | Home Assistant | Notes |
| -------------| ------ | :---: | ------------- | ------------- | ------------- |
| [Sonoff Mini](https://amzn.to/2HlmcED) | ![](https://i.ibb.co/rd2Bb1L/41-WVzq-Dw7-TL-AC-SX425.jpg) | 3 | Wi-Fi | [MQTT]| [DIY](https://tasmota.github.io/docs/Sonoff-DIY/)  jumper [Tasmota] flashed|
| [Sonoff Dual](https://amzn.to/2UIeJCw) | ![](https://i.ibb.co/Dw1w9yz/Sonoff-Dual.jpg) |2 | Wi-Fi| [MQTT]| Hardware [Tasmota] flashed|
| [Blitzwolf BW-SHP2](https://amzn.to/336IQIy) | ![](https://i.ibb.co/2sbbsmy/Blitzwolf-BW-SHP2.jpg) |2 | Wi-Fi| [MQTT]| [Tasmota] flashed with [tuya-convert](https://github.com/ct-Open-Source/tuya-convert)|
| [Wifi RGB Controller](https://amzn.to/397N1Yt) | ![](https://i.ibb.co/P5f90mg/rgb-Controller.jpg) | 1 | Wi-Fi| [Flux Led](https://www.home-assistant.io/integrations/flux_led/) | Led strip RGB controller|
| [Xiaomi Aqara Multisensor](https://amzn.to/35N2JWE) |![](https://i.ibb.co/hskTfq3/aqara-Multisensor.jpg) | 5 | Zigbee| [deConz]| Temperature, humidity, pressure and battery sensor|
| [Broadlink RM3Mini](https://amzn.to/2IW48kU) |![](https://i.ibb.co/6Z01sk1/Broadlink-RM3-Mini.jpg) | 1 | Wi-Fi| [Broadlink]| Universal infrared remote|
| [Conbee II](https://amzn.to/2IW48kU) |![](https://i.ibb.co/Hzpr7Ph/conbee2-aquacolor2.jpg) | 1 | USB| [deConz] | USB Zigbee gateway|


# New Features!

  - **16.11.2020**: ESP32 and DS18B20 MQTT Temperature 
  - **23.11.2020**: Startup sync automation (Lights, Covers and Climate)
 

# Integration & Addons

In my comfiguration I use the following integrations

| Plugin |Type| Source|Note| Github Repo |
| ------|-----| --- |----| ------ |
| Auto-entities |Frontend|[HACS] |Used to auto fill battery card | https://github.com/thomasloven/lovelace-auto-entities |
| RGB Light Card |Frontend|[HACS]|Used to control RGB led strip with presets| https://github.com/bokub/rgb-light-card |
| Button Card |Frontend|[HACS]|Nota| https://github.com/custom-cards/button-card |
| Shutter Card |Frontend|[HACS]|Nota| https://github.com/Deejayfool/hass-shutter-card|
| Mini Climate Card |Frontend|[HACS]|Nota| https://github.com/artem-sedykh/mini-climate-card |
| Multiple Entity Row |Frontend|[HACS]|Nota| https://github.com/benct/lovelace-multiple-entity-row |
| Battery Entity Row |Frontend|[HACS]|Nota| https://github.com/benct/lovelace-battery-entity-row |
| Mini Media Player |Frontend|[HACS]|Nota| https://github.com/kalkih/mini-media-player |
| Vertical Stack In Card |Frontend|[HACS]|Nota| https://github.com/ofekashery/vertical-stack-in-card |
| Simple Thermostat |Frontend|[HACS]|Nota| https://github.com/nervetattoo/simple-thermostat |
| Mini Graph Card |Frontend|[HACS]| Nota|https://github.com/kalkih/mini-graph-card |
| SmartIR |Integration|[HACS]|Nota| https://github.com/smartHomeHub/SmartIR |
| Alexa Media Player |Integration|[HACS]| Nota|https://github.com/custom-components/alexa_media_player |
| Node-RED |Integration|[HACS]|Nota| https://github.com/zachowj/hass-node-red|


License
----

MIT


**Free Software**

[//]: # (These are reference links used in the body of this note and get stripped out when the markdown processor does its job. There is no need to format nicely because it shouldn't be seen. Thanks SO - http://stackoverflow.com/questions/4823468/store-comments-in-markdown-syntax)

   [MQTT]: <https://www.home-assistant.io/integrations/mqtt/>
   [Tasmota]: <https://tasmota.github.io/docs/>
   [deConz]: <https://www.home-assistant.io/integrations/broadlink/>
   [HACS]: <https://hacs.xyz/docs/installation/manual>
   [Broadlink]: <https://www.home-assistant.io/integrations/broadlink/>
