# WebSocket node connection

This document provides an overview of the configuration and state structure for a WebSocket-based application. The configurations and states are organized into categories such as config, intervals, light, location, network, device, and state. Each category contains various parameters that define the settings and operational status of the application.


WebSocket Application Configuration and State Overview
This document provides an overview of the configuration and state structure for a WebSocket-based application. The configurations and states are organized into categories such as config, intervals, light, location, network, device, and state. Each category contains various parameters that define the settings and operational status of the application.

## get-nodes

The `get-nodes` command is used to request the list of all currently powered nodes in the network. This command is essential for network administrators to get an overview of active devices and their statuses. When this command is sent, the server responds with details about each powered node, including their configuration and state.

**Command object structured**

```javascript
var cmd_get_nodes = {
    command: 'get-nodes',
    data: {}
  }
```
**Response JSON**
```json
[
{
  "config": {
    "datetime": {
      "save": true,
      "sntp_server": "pool.ntp.org",
      "sync_to_unixtime": 0,
      "sync_with_sntp": false,
      "timezone": "CET-1CEST,M3.5.0,M10.5.0/3",
      "updated": true
    },
    "intervals": {
      "read": 5000,
      "save": true,
      "send": 30000,
      "store": 60000,
      "updated": true
    },
    "light": {
      "blink_color": {
        "blink_color_error": false,
        "blink_color_r": 255,
        "blink_color_g": 255,
        "blink_color_b": 255,
        "blink_color_w": 255
      },
      "blink_duration": 500,
      "blink_time": 500,
      "blink_type": 0,
      "color": {
        "error": false,
        "r": 255,
        "g": 255,
        "b": 255,
        "w": 255
      },
      "mode": 0,
      "restart_mode": 1,
      "save": true,
      "updated": false
    },
    "location": {
      "category_id": 0,
      "family_id": 0,
      "gps_position": {
        "altitude": 0,
        "error": false,
        "latitude": 0,
        "longitude": 0
      },
      "group_id": 0,
      "location_id": 0,
      "location_name": "",
      "save": true,
      "updated": false
    },
    "network": {
      "mesh_authmode": 6,
      "mesh_channel": 11,
      "mesh_channel_switch": 0,
      "mesh_config": {
        "assoc_expire_ms": 30000,
        "attempt_count": 30,
        "backoff_rssi": -98,
        "beacon_interval_ms": 100,
        "capacity_num": 100,
        "cnx_rssi": -118,
        "data_drop_enable": true,
        "max_connection": 6,
        "max_layer": 101,
        "max_layer_deprecated": 0,
        "monitor_duration_ms": 30000,
        "monitor_ie_count": 10,
        "passive_scan_ms": 300,
        "retransmit_enable": true,
        "root_conflicts_enable": false,
        "root_healing_ms": 6000,
        "scan_min_count": 10,
        "select_rssi": -78,
        "switch_rssi": -98,
        "topology": 1,
        "vote_max_count": 15,
        "vote_percentage": 90,
        "xon_qsize": 64
      },
      "mesh_id": "999988",
      "mesh_node_type": 2,
      "mesh_pass": "password",
      "mesh_root_type": 1,
      "mesh_router_switch": 0,
      "mesh_updated": false,
      "ping_interval": 15000,
      "ping_threshold": 3,
      "save": true,
      "updated": true,
      "wifi_ap_authmode": 6,
      "wifi_ap_channel": 11,
      "wifi_ap_pass": "password",
      "wifi_ap_ssid": "BridgeAP",
      "wifi_ap_updated": false,
      "wifi_sta_authmode": 6,
      "wifi_sta_channel": 11,
      "wifi_sta_pass": "8165044699",
      "wifi_sta_ssid": "TP-Link_C49C",
      "wifi_sta_updated": false,
      "save": true,
      "updated": true,
      "version": 1
    },
    "device": {
      "api_version": 14132,
      "atecc_serial_str": "",
      "chip_cores": 1,
      "chip_features": 82,
      "chip_id": 13,
      "chip_revision": 0,
      "device_id": 0,
      "factory_datetime": "",
      "factory_registered": false,
      "firmware_version": "1.0.2",
      "idf_datetime": "Jun 21 2024 - 09:35:47",
      "idf_version": "v5.2.2-172-gb63fd4eaee",
      "model": "ST-INE-002-004",
      "name": "ST-INE-002-004",
      "serial_number": "",
      "token": "",
      "mac_address": "40:4c:ca:45:1e:08"
    },
    "state": {
      "mesh": {
        "mesh_childs": 0,
        "mesh_childs_total": 0,
        "mesh_connected": true,
        "mesh_init": true,
        "mesh_layer": 2,
        "mesh_mac": "39:39:39:39:38:38",
        "mesh_parent_rssi": -77,
        "parent_addr": "00:00:00:6c:f3:85",
        "root_addr": "90:38:0c:ac:5f:0d"
      }
    },
    "sensors": {
      "accel": {
        "error": false,
        "x": -0.0328180007636547,
        "y": -0.17470400035381317,
        "z": 0.9808800220489502
      },
      "ambient": {
        "air_quality": 0,
        "altitude": 0,
        "error": false,
        "humidity": 0,
        "pressure": 0,
        "temperature": 0
      },
      "battery": {
        "adc_imon": 11,
        "capacity": 0,
        "charge_current": 0,
        "error": false,
        "input_charge": 106.25,
        "input_current_limit": 800,
        "input_voltage": 11960,
        "is_powered": true,
        "junction_temperature": 45.38869857788086,
        "status0": 27136,
        "status1": 32,
        "system_voltage": 8360,
        "total_cells": 2,
        "voltage_per_cell": 3595
      },
      "compass": {
        "error": false,
        "x": 0,
        "y": 0,
        "z": 0
      },
      "gps": {
        "altitude": 0,
        "error": false,
        "latitude": 0,
        "longitude": 0
      },
      "gyros": {
        "error": false,
        "x": 0,
        "y": 0,
        "z": 0
      },
      "lux_color": {
        "b": 255,
        "error": false,
        "g": 255,
        "r": 255,
        "w": 255
      },
      "noise": {
        "db": 0,
        "error": false,
        "mv": 0,
        "raw": 0
      }
    },
    "total_errors": 2,
    "total_reads": 0,
    "total_sents": 0,
    "total_stores": 0,
    "total_time": 12,
    "unixtime": 94173
  }
}
]
```


### Configuration (config)
#### DateTime
The DateTime configuration handles settings related to date and time, including synchronization with an SNTP server.
- save: A boolean indicating if the settings should be saved.
  
- sntp_server: The address of the SNTP server.
  
- sync_to_unixtime: Indicates whether to sync to Unix time.

- sync_with_sntp: A boolean indicating whether to sync with the SNTP server.

- timezone: The timezone setting.

- updated: A boolean indicating if the configuration has been updated.

#### Intervals
This section defines various time intervals for reading, sending, and storing data.

- read: Interval for reading data.

- save: A boolean indicating if the settings should be saved.

- send: Interval for sending data.

- store: Interval for storing data.

- updated: A boolean indicating if the configuration has been updated.

#### Light
The Light configuration deals with the settings for light operations, such as blinking and color settings.

- blink_color: Defines the color for the blinking light.

- blink_color_b: Blue component.

- blink_color_error: Error flag.

- blink_color_g: Green component.

- blink_color_r: Red component.

- blink_color_w: White component.

- blink_duration: Duration of the blink.

- blink_time: Time between blinks.

- blink_type: Type of blink.

- color: Main color settings.
     - b: Blue component.

     - error: Error flag.
     
     - g: Green component.
     
     - r: Red component.
     
     - w: White component.

- mode: Operation mode.

- restart_mode: Mode for restart.

- save: A boolean indicating if the settings should be saved.

- updated: A boolean indicating if the configuration has been updated.

#### Location
The Location configuration includes settings for location identification and GPS position.

- category_id: Category identifier.

- family_id: Family identifier.

- gps_position: GPS position settings.

    - altitude: Altitude.
    
    - error: Error flag.
    
    - latitude: Latitude.
    
    - longitude: Longitude.

- group_id: Group identifier.

- location_id: Location identifier.

- location_name: Name of the location.

- save: A boolean indicating if the settings should be saved.

- updated: A boolean indicating if the configuration has been updated.


#### Network
The Network configuration includes settings related to network operations, including mesh network settings and WiFi configurations.

- mesh_authmode: Mesh network authentication mode.

- mesh_channel: Mesh network channel.

- mesh_channel_switch: Channel switch flag.

- mesh_config: Detailed mesh network configuration.

    - assoc_expire_ms: Association expiration time.
    
    - attempt_count: Number of connection attempts.
    
    - backoff_rssi: Backoff RSSI value.
    
    - beacon_interval_ms: Beacon interval.
    
    - capacity_num: Capacity number.
    
    - cnx_rssi: Connection RSSI value.
    
    - data_drop_enable: Data drop enable flag.
    
    - max_connection: Maximum number of connections.
    
    - max_layer: Maximum network layer.
    
    - max_layer_deprecated: Deprecated maximum network layer.
    
    - monitor_duration_ms: Monitor duration.
    
    - monitor_ie_count: Monitor IE count.
    
    - passive_scan_ms: Passive scan duration.
    
    - retransmit_enable: Retransmit enable flag.
    
    - root_conflicts_enable: Root conflicts enable flag.
    
    - root_healing_ms: Root healing duration.
    
    - scan_min_count: Minimum scan count.
    
    - select_rssi: Select RSSI value.
    
    - switch_rssi: Switch RSSI value.
    
    - topology: Network topology.
    
    - vote_max_count: Maximum vote count.
    
    - vote_percentage: Vote percentage.
    
    - xon_qsize: XON queue size.

- mesh_id: Mesh network identifier.

- mesh_node_type: Type of mesh node.

- mesh_pass: Mesh network password.

- mesh_root_type: Type of mesh root.

- mesh_router_switch: Router switch flag.

- mesh_updated: Mesh configuration updated flag.

- ping_interval: Ping interval.

- ping_threshold: Ping threshold.

- save: A boolean indicating if the settings should be saved.

- updated: A boolean indicating if the configuration has been updated.

- wifi_ap_authmode: WiFi AP authentication mode.

- wifi_ap_channel: WiFi AP channel.

- wifi_ap_pass: WiFi AP password.

- wifi_ap_ssid: WiFi AP SSID.

- wifi_ap_updated: WiFi AP configuration updated flag.

- wifi_sta_authmode: WiFi STA authentication mode.

- wifi_sta_channel: WiFi STA channel.

- wifi_sta_pass: WiFi STA password.

- wifi_sta_ssid: WiFi STA SSID.

- wifi_sta_updated: WiFi STA configuration updated flag.

- save:XXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXX

- update:XXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXX

- version:XXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXX

### Device
The Device section provides information about the hardware and software of the device.

- api_version: API version.

- atecc_serial_str: Serial string for ATECC chip.

- chip_cores: Number of chip cores.

- chip_features: Chip features.

- chip_id: Chip identifier.

- chip_revision: Chip revision.

- device_id: Device identifier.

- factory_datetime: Factory date and time.

- factory_registered: Factory registered flag.

- firmware_version: Firmware version.

- idf_datetime: IDF date and time.

- idf_version: IDF version.

- model: Device model.

- name: Device name.

- serial_number: Device Serial number.

- token: Device token.

- mac_address: Device MAC adress.


### State
The State section provides real-time information about the device's operational status, including network status and sensor readings.

#### Mesh
- mesh_childs: Number of mesh children.

- mesh_childs_total: Total number of mesh children.

- mesh_connected: Mesh connected status.

- mesh_init: Mesh initialization status.

- mesh_layer: Mesh network layer.

- mesh_mac: Mesh MAC address.

- mesh_parent_rssi: Mesh parent RSSI value.

- parent_addr: Parent address.

- root_addr: Root address.

#### Sensors
- accel: Accelerometer data.

    - error: Error flag.
    
    - x: X-axis value.
    
    - y: Y-axis value.
    
    - z: Z-axis value.

- ambient: Ambient sensor data.

    - air_quality: Air quality.
    
    - altitude: Altitude.
    
    - error: Error flag.
    
    - humidity: Humidity.
    
    - pressure: Pressure.
    
    - temperature: Temperature.

- battery: Battery status.

    - adc_imon: ADC current monitoring.
    
    - capacity: Battery capacity .
    
    - charge_current: Charge current.
    
    - error: Error flag.
    
    - input_charge: Input charge.
    
    - input_current_limit: Input current limit.
    
    - input_voltage: Input voltage.
    
    - is_powered: Power status.
    
    - junction_temperature: Junction temperature.
    
    - status0: Status register 0.
    
    - status1: Status register 1.
    
    - system_voltage: System voltage.
    
    - total_cells: Total number of cells.
    
    - voltage_per_cell: Voltage per cell.

- compass: Compass data.

    - error: Error flag.
    
    - x: X-axis value.
    
    - y: Y-axis value.
    
    - z: Z-axis value.

- gps: GPS data.
    
    - altitude: Altitude.
    
    - error: Error flag.

    - latitude: Latitude.
      
    - longitude: Longitude.

- gyros: Gyroscope data.
    
    - error: Error flag.
    
    - x: X-axis value.
    
    - y: Y-axis value.
    
    - z: Z-axis value.

- lux_color: Light color sensor data.
    
    - b: Blue component.
    
    - error: Error flag.
    
    - g: Green component.
    
    - r: Red component.
    
    - w: White component.

- noise: Noise sensor data.
    
    - db: Noise level in decibels.
    
    - error: Error flag.
    
    - mv: Millivolt value.
    
    - raw: Raw sensor value.

- total_errors: Total number of errors.

- total_reads: Total number of reads.

- total_sents: Total number of sends.

- total_stores: Total number of stores.

- total_time: Total operational time.

- unixtime: Unix time.

