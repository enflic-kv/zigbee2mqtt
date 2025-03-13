# Zigbee2Mqtt powered by compose

Zigbee2MQTT is an open-source project that allows users to control and monitor Zigbee devices in their smart homes without the need for proprietary gateway hardware. It utilizes a Zigbee radio and a small software device, called a coordinator, to communicate with Zigbee devices and translate their messages to MQTT, an open and standard protocol for IoT devices. This enables users to connect and control Zigbee devices with a wide range of home automation software and services, such as Home Assistant, Node-RED, or openHAB. Zigbee2MQTT supports a wide range of Zigbee devices from various manufacturers and provides advanced features, such as OTA firmware updates, device pairing, and network visualization. Additionally, Zigbee2MQTT is free to use, and it runs on various hardware platforms, including Raspberry Pi, Docker, and even some Zigbee routers.

## Requirements

* docker >= 17.12.0+
* docker-compose

## Quick Start

1. Install [docker-compose](https://docs.docker.com/compose/install/) on the docker host.
1. Clone this repo.
1. Navigate to directory,  `cd zigbee2mqtt`
1. Optionally, change default credentials in the `.env` file.
1. Navigate to `conf/` directory and update the `configuration.yaml` fiel accordingly with the mqtt broker settings and serial port.
1. Run the following command from the root:

```bash
docker-compose up -d
```

1. To stop the app, run the following command from the root of the cloned repo:

```bash
docker-compose down
```

## Environments

This Compose file contains the following environment variables:

| Variables | Default |
| --------- | -------- |
| IMAGE_VERSION | latest |
| CONTAINER_NAME | zigbee2mqtt-container |
| UI_PORT | 8080 |
| USB_PORT | /dev/ttyUSB0 |
| EXTERNAL_NETWORK | ily-network |
