# HomeAssistant Config


[![GitHub stars](https://img.shields.io/github/stars/alesus97/HomeAssistant)](https://github.com/alesus97/HomeAssistant)
[![GitHub last commit](https://img.shields.io/github/last-commit/alesus97/HomeAssistant)](https://github.com/alesus97/HomeAssistant/commits/master)
[![HA Version](https://img.shields.io/badge/Running%20Home%20Assistant-0.118.2%20-darkblue)](https://github.com/home-assistant/home-assistant/releases/latest)
# Devices


| Device  | Image|Quantity | Connection | Home Assistant | Notes |
| -------------| ------ | :---: | ------------- | ------------- | ------------- |
| [Sonoff Mini](https://amzn.to/2HlmcED) | ![](https://i.ibb.co/rd2Bb1L/41-WVzq-Dw7-TL-AC-SX425.jpg) | 3 | Wi-Fi | [MQTT]| [DIY](https://tasmota.github.io/docs/Sonoff-DIY/)  jumper [Tasmota] flashed|
| [Sonoff Dual](https://amzn.to/2UIeJCw) | ![](https://i.ibb.co/Dw1w9yz/Sonoff-Dual.jpg) |2 | Wi-Fi| [MQTT]| Hardware [Tasmota] flashed|
| [Blitzwolf BW-SHP2](https://amzn.to/336IQIy) | ![](https://i.ibb.co/2sbbsmy/Blitzwolf-BW-SHP2.jpg) |2 | Wi-Fi| [MQTT]| [Tasmota] flashed with [tuya-convert](https://github.com/ct-Open-Source/tuya-convert)|
| [Wifi RGB Controller](https://amzn.to/397N1Yt) | ![](https://i.ibb.co/P5f90mg/rgb-Controller.jpg) | 1 | Wi-Fi| [Flux Led](https://www.home-assistant.io/integrations/flux_led/) | Led strip RGB controller|
| [Xiaomi Aqara Multisensor](https://amzn.to/35N2JWE) |![](https://i.ibb.co/hskTfq3/aqara-Multisensor.jpg) | 1 | Zigbee| [deConz]| Temperature, humidity, pressure and battery sensor|
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

### Installation

Dillinger requires [Node.js](https://nodejs.org/) v4+ to run.

Install the dependencies and devDependencies and start the server.

```sh
$ cd dillinger
$ npm install -d
$ node app
```

For production environments...

```sh
$ npm install --production
$ NODE_ENV=production node app
```

### Plugins

Dillinger is currently extended with the following plugins. Instructions on how to use them in your own application are linked below.

| Plugin | README |
| ------ | ------ |
| Dropbox | [plugins/dropbox/README.md][PlDb] |
| GitHub | [plugins/github/README.md][PlGh] |
| Google Drive | [plugins/googledrive/README.md][PlGd] |
| OneDrive | [plugins/onedrive/README.md][PlOd] |
| Medium | [plugins/medium/README.md][PlMe] |
| Google Analytics | [plugins/googleanalytics/README.md][PlGa] |


### Development

Want to contribute? Great!

Dillinger uses Gulp + Webpack for fast developing.
Make a change in your file and instantaneously see your updates!

Open your favorite Terminal and run these commands.

First Tab:
```sh
$ node app
```

Second Tab:
```sh
$ gulp watch
```

(optional) Third:
```sh
$ karma test
```
#### Building for source
For production release:
```sh
$ gulp build --prod
```
Generating pre-built zip archives for distribution:
```sh
$ gulp build dist --prod
```
### Docker
Dillinger is very easy to install and deploy in a Docker container.

By default, the Docker will expose port 8080, so change this within the Dockerfile if necessary. When ready, simply use the Dockerfile to build the image.

```sh
cd dillinger
docker build -t <youruser>/dillinger:${package.json.version} .
```
This will create the dillinger image and pull in the necessary dependencies. Be sure to swap out `${package.json.version}` with the actual version of Dillinger.

Once done, run the Docker image and map the port to whatever you wish on your host. In this example, we simply map port 8000 of the host to port 8080 of the Docker (or whatever port was exposed in the Dockerfile):

```sh
docker run -d -p 8000:8080 --restart=always --cap-add=SYS_ADMIN --name=dillinger <youruser>/dillinger:${package.json.version}
```

Verify the deployment by navigating to your server address in your preferred browser.

```sh
127.0.0.1:8000
```

#### Kubernetes + Google Cloud

See [KUBERNETES.md](https://github.com/joemccann/dillinger/blob/master/KUBERNETES.md)


### Todos

 - Write MORE Tests
 - Add Night Mode

License
----

MIT


**Free Softwar**

[//]: # (These are reference links used in the body of this note and get stripped out when the markdown processor does its job. There is no need to format nicely because it shouldn't be seen. Thanks SO - http://stackoverflow.com/questions/4823468/store-comments-in-markdown-syntax)

   [MQTT]: <https://www.home-assistant.io/integrations/mqtt/>
   [Tasmota]: <https://tasmota.github.io/docs/>
   [deConz]: <https://www.home-assistant.io/integrations/broadlink/>
   [HACS]: <https://hacs.xyz/docs/installation/manual>
   [Broadlink]: <https://www.home-assistant.io/integrations/broadlink/>
