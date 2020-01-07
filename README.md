homebridge-irobot-roomba690
=========

This [Homebridge](https://homebridge.io/) plugin is a fork of [**homebridge-roomba690**](https://github.com/gbro115/homebridge-roomba690).

**homebridge-roomba690** works great in most circumstances, but occasionally it may block all the other accessories in a Homebridge instance. When the plugin fails to connect to Roomba, or it just takes too long to get the response, other accessories will also become unresponsive because HAP (HomeKit Accessory Protocol) only allows one concurrent request per connection. Please check [One accessory blocks the whole homebridge](https://github.com/nfarina/homebridge/issues/948) for more information.

This plugin implements a timeout limit of 5 seconds. If it cannot get the response in 5 seconds, it will throw an error and avoid blocking other accessories.

The configuration of this plugin would be the exactly the same as **homebridge-roomba690**. To use this plugin, you need to uninstall **homebridge-roomba690** first.
