# Home Assistant Add-on: owserver

[![Releases][version]][releases]

![amd64][amd64-shield]
![aarch64][aarch64-shield]
![armhf][armhf-shield]
![armv7][armv7-shield]
![i386][i386-shield]

The addon provides owserver to read 1-Wire devices over serial/i2c or usb device.


## About

This addon provides you owserver instance to read 1-Wire devices over serial/i2c/usb or ha7net device and exposing reading to Home Assistant via the native integration.

### Supported devices
Addon has been tested with
- [MERA-PROJEKT MP00206-P](http://www.meraprojekt.com.pl/mp00206-p.html)
- [ElabNET's Professional Busmaster PBM-01](https://shop.elabnet.de/en/1-wire/series/h/1-wire-professional-bus-master-pbm01-usb_812_2073)
- [HA7Net](https://www.embeddeddatasystems.com/HA7Net--Ethernet-1-Wire-Host-Adapter_p_22.html) 

but shoud work well with other serial/i2c/usb/ha7net/passive devices. Please let me know what device you're using so I will update device list for further reference.

## Installation and configuration

### Installation

1. Access your Home Assistant, go to **Add-ons** -> **Add-on Store** and add this URL as an additional repository: 
`https://github.com/domectrl/addon-repository`
1. Find the "owserver (1-Wire)" add-on and click the "INSTALL" button.
1. Configure the add-on and click on "START". With default configuration addon starts with fake (mocked) devices.
1. Add to Home Assistant through the Integrations. Go to Integrations, Add Integration, Choose 1-Wire
    - Host: `provide add-on's hostname (from add-on details page)`
    - Port: `4304` _(default)_
1. ... or use Home Asistant auto discovery (since 2025.2.0). Go to Integrations, find discovered addon and Add it.
1. That's it. On the integrations page wou will find 1-Wire integration with 1-Wire devices.

### Configuration
Please check the **[full documentation page](https://github.com/domectrl/hassio-owserver/blob/master/DOCS.md)**.

## Screenshots

![Integration setup 1](https://github.com/domectrl/hassio-owserver/raw/master/images/screenshot_setup1.png)
![Integration setup 2](https://github.com/domectrl/hassio-owserver/raw/master/images/screenshot_setup2.png)
![Integration setup 3](https://github.com/domectrl/hassio-owserver/raw/master/images/screenshot_setup3.jpg)
![Integrations page](https://github.com/domectrl/hassio-owserver/raw/master/images/screenshot_integrations.jpg)
![owhttpd](https://github.com/domectrl/hassio-owserver/raw/master/images/screenshot_owhttpd.jpg)

[version]: https://img.shields.io/badge/version-v0.7.4-blue.svg
[releases]: https://github.com/domectrl/hassio-owserver/releases
[addons-repository]: https://github.com/domectrl/addon-repository
[addons-repository-beta]: https://github.com/domectrl/addon-repository-beta
[addons-repository-edge]: https://github.com/domectrl/addon-repository-edge

[amd64-shield]: https://img.shields.io/badge/amd64-yes-green.svg
[aarch64-shield]: https://img.shields.io/badge/aarch64-yes-green.svg
[armhf-shield]: https://img.shields.io/badge/armhf-yes-green.svg
[armv7-shield]: https://img.shields.io/badge/armv7-yes-green.svg
[i386-shield]: https://img.shields.io/badge/i386-no-red.svg