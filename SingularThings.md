# WebSocket lamp connection

This document provides an overview of the configuration and state structure for a WebSocket-based application. The configurations and states are organized into categories such as config, intervals, light, location, network, device, and state. Each category contains various parameters that define the settings and operational status of the application.


WebSocket Application Configuration and State Overview
This document provides an overview of the configuration and state structure for a WebSocket-based application. The configurations and states are organized into categories such as config, intervals, light, location, network, device, and state. Each category contains various parameters that define the settings and operational status of the application.

## Configuration (config)
### DateTime
The DateTime configuration handles settings related to date and time, including synchronization with an SNTP server.
- save: A boolean indicating if the settings should be saved (true).
- sntp_server: The address of the SNTP server ("pool.ntp.org").
- sync_to_unixtime: Indicates whether to sync to Unix time (0).
- sync_with_sntp: A boolean indicating whether to sync with the SNTP server (false).
- timezone: The timezone setting ("CET-1CEST,M3.5.0,M10.5.0/3").
- updated: A boolean indicating if the configuration has been updated (true).

### Intervals
This section defines various time intervals for reading, sending, and storing data.

- read: Interval for reading data (5000 milliseconds).
- save: A boolean indicating if the settings should be saved (true).
- send: Interval for sending data (30000 milliseconds).
- store: Interval for storing data (60000 milliseconds).
- updated: A boolean indicating if the configuration has been updated (true).

### Light
The Light configuration deals with the settings for light operations, such as blinking and color settings.

- blink_color: Defines the color for the blinking light.
- blink_color_b: Blue component (255).
- blink_color_error: Error flag (false).
- blink_color_g: Green component (255).
- blink_color_r: Red component (255).
- blink_color_w: White component (255).
- blink_duration: Duration of the blink (500 milliseconds).
- blink_time: Time between blinks (500 milliseconds).
- blink_type: Type of blink (0).
- color: Main color settings.
     - b: Blue component (255).
     - error: Error flag (false).
     - g: Green component (255).
     - r: Red component (255).
     - w: White component (255).
- mode: Operation mode (0).
- restart_mode: Mode for restart (1).
- save: A boolean indicating if the settings should be saved (true).
- updated: A boolean indicating if the configuration has been updated (false).

### Location
The Location configuration includes settings for location identification and GPS position.

- category_id: Category identifier (0).
- family_id: Family identifier (0).
- gps_position: GPS position settings.
    - altitude: Altitude (0).
    - error: Error flag (false).
    - latitude: Latitude (0).
    - longitude: Longitude (0).
- group_id: Group identifier (0).
- location_id: Location identifier (0).
- location_name: Name of the location ("").
- save: A boolean indicating if the settings should be saved (true).
- updated: A boolean indicating if the configuration has been updated (false).


### Network
The Network configuration includes settings related to network operations, including mesh network settings and WiFi configurations.

- mesh_authmode: Mesh network authentication mode (6).
- mesh_channel: Mesh network channel (11).
- mesh_channel_switch: Channel switch flag (0).
- mesh_config: Detailed mesh network configuration.
    - assoc_expire_ms: Association expiration time (30000 milliseconds).
    - attempt_count: Number of connection attempts (30).
    - backoff_rssi: Backoff RSSI value (-98).
    - beacon_interval_ms: Beacon interval (100 milliseconds).
    - capacity_num: Capacity number (100).
    - cnx_rssi: Connection RSSI value (-118).
    - data_drop_enable: Data drop enable flag (true).
    - max_connection: Maximum number of connections (6).
    - max_layer: Maximum network layer (101).
    - max_layer_deprecated: Deprecated maximum network layer (0).
    - monitor_duration_ms: Monitor duration (30000 milliseconds).
    - monitor_ie_count: Monitor IE count (10).
    - passive_scan_ms: Passive scan duration (300 milliseconds).
    - retransmit_enable: Retransmit enable flag (true).
    - root_conflicts_enable: Root conflicts enable flag (false).
    - root_healing_ms: Root healing duration (6000 milliseconds).
    - scan_min_count: Minimum scan count (10).
    - select_rssi: Select RSSI value (-78).
    - switch_rssi: Switch RSSI value (-98).
    - topology: Network topology (1).
    - vote_max_count: Maximum vote count (15).
    - vote_percentage: Vote percentage (90).
    - xon_qsize: XON queue size (64).
- mesh_id: Mesh network identifier ("999988").
- mesh_node_type: Type of mesh node (2).
- mesh_pass: Mesh network password ("password").
- mesh_root_type: Type of mesh root (1).
- mesh_router_switch: Router switch flag (0).
- mesh_updated: Mesh configuration updated flag (false).
- ping_interval: Ping interval (15000 milliseconds).
- ping_threshold: Ping threshold (3).
- save: A boolean indicating if the settings should be saved (true).
- updated: A boolean indicating if the configuration has been updated (true).
- wifi_ap_authmode: WiFi AP authentication mode (6).
- wifi_ap_channel: WiFi AP channel (11).
- wifi_ap_pass: WiFi AP password ("password").
- wifi_ap_ssid: WiFi AP SSID ("BridgeAP").
- wifi_ap_updated: WiFi AP configuration updated flag (false).
- wifi_sta_authmode: WiFi STA authentication mode (6).
- wifi_sta_channel: WiFi STA channel (11).
- wifi_sta_pass: WiFi STA password ("8165044699").
- wifi_sta_ssid: WiFi STA SSID ("TP-Link_C49C").
- wifi_sta_updated: WiFi STA configuration updated flag (false).
-save:
-update:
-version:

## Device
The Device section provides information about the hardware and software of the device.

- api_version: API version (14132).
- atecc_serial_str: Serial string for ATECC chip ("").
- chip_cores: Number of chip cores (1).
- chip_features: Chip features (82).
- chip_id: Chip identifier (13).
- chip_revision: Chip revision (0).
- device_id: Device identifier (0).
- factory_datetime: Factory date and time ("").
- factory_registered: Factory registered flag (false).
- firmware_version: Firmware version ("1.0.2").
- idf_datetime: IDF date and time ("Jun 21 2024 - 09:35:47").
- idf_version: IDF version ("v5.2.2-172-gb63fd4eaee").
- model: Device model ("ST-INE-002-004").
- name: Device name ("ST-INE-002-004").
- serial_number: Device Serial number ("").
- token: Device token ("").
- mac_address: Device MAC adress.

## State
The State section provides real-time information about the device's operational status, including network status and sensor readings.


WebSocket Application Configuration and State Overview
This document provides an overview of the configuration and state structure for a WebSocket-based application. The configurations and states are organized into categories such as config, intervals, light, location, network, device, and state. Each category contains various parameters that define the settings and operational status of the application.

Configuration (config)
DateTime
The DateTime configuration handles settings related to date and time, including synchronization with an SNTP server.

save: A boolean indicating if the settings should be saved (true).
sntp_server: The address of the SNTP server ("pool.ntp.org").
sync_to_unixtime: Indicates whether to sync to Unix time (0).
sync_with_sntp: A boolean indicating whether to sync with the SNTP server (false).
timezone: The timezone setting ("CET-1CEST,M3.5.0,M10.5.0/3").
updated: A boolean indicating if the configuration has been updated (true).
Intervals
This section defines various time intervals for reading, sending, and storing data.

read: Interval for reading data (5000 milliseconds).
save: A boolean indicating if the settings should be saved (true).
send: Interval for sending data (30000 milliseconds).
store: Interval for storing data (60000 milliseconds).
updated: A boolean indicating if the configuration has been updated (true).
Light
The Light configuration deals with the settings for light operations, such as blinking and color settings.

blink_color: Defines the color for the blinking light.
blink_color_b: Blue component (255).
blink_color_error: Error flag (false).
blink_color_g: Green component (255).
blink_color_r: Red component (255).
blink_color_w: White component (255).
blink_duration: Duration of the blink (500 milliseconds).
blink_time: Time between blinks (500 milliseconds).
blink_type: Type of blink (0).
color: Main color settings.
b: Blue component (255).
error: Error flag (false).
g: Green component (255).
r: Red component (255).
w: White component (255).
mode: Operation mode (0).
restart_mode: Mode for restart (1).
save: A boolean indicating if the settings should be saved (true).
updated: A boolean indicating if the configuration has been updated (false).
Location
The Location configuration includes settings for location identification and GPS position.

category_id: Category identifier (0).
family_id: Family identifier (0).
gps_position: GPS position settings.
altitude: Altitude (0).
error: Error flag (false).
latitude: Latitude (0).
longitude: Longitude (0).
group_id: Group identifier (0).
location_id: Location identifier (0).
location_name: Name of the location ("").
save: A boolean indicating if the settings should be saved (true).
updated: A boolean indicating if the configuration has been updated (false).
Network
The Network configuration includes settings related to network operations, including mesh network settings and WiFi configurations.

mesh_authmode: Mesh network authentication mode (6).
mesh_channel: Mesh network channel (11).
mesh_channel_switch: Channel switch flag (0).
mesh_config: Detailed mesh network configuration.
assoc_expire_ms: Association expiration time (30000 milliseconds).
attempt_count: Number of connection attempts (30).
backoff_rssi: Backoff RSSI value (-98).
beacon_interval_ms: Beacon interval (100 milliseconds).
capacity_num: Capacity number (100).
cnx_rssi: Connection RSSI value (-118).
data_drop_enable: Data drop enable flag (true).
max_connection: Maximum number of connections (6).
max_layer: Maximum network layer (101).
max_layer_deprecated: Deprecated maximum network layer (0).
monitor_duration_ms: Monitor duration (30000 milliseconds).
monitor_ie_count: Monitor IE count (10).
passive_scan_ms: Passive scan duration (300 milliseconds).
retransmit_enable: Retransmit enable flag (true).
root_conflicts_enable: Root conflicts enable flag (false).
root_healing_ms: Root healing duration (6000 milliseconds).
scan_min_count: Minimum scan count (10).
select_rssi: Select RSSI value (-78).
switch_rssi: Switch RSSI value (-98).
topology: Network topology (1).
vote_max_count: Maximum vote count (15).
vote_percentage: Vote percentage (90).
xon_qsize: XON queue size (64).
mesh_id: Mesh network identifier ("999988").
mesh_node_type: Type of mesh node (2).
mesh_pass: Mesh network password ("password").
mesh_root_type: Type of mesh root (1).
mesh_router_switch: Router switch flag (0).
mesh_updated: Mesh configuration updated flag (false).
ping_interval: Ping interval (15000 milliseconds).
ping_threshold: Ping threshold (3).
save: A boolean indicating if the settings should be saved (true).
updated: A boolean indicating if the configuration has been updated (true).
wifi_ap_authmode: WiFi AP authentication mode (6).
wifi_ap_channel: WiFi AP channel (11).
wifi_ap_pass: WiFi AP password ("password").
wifi_ap_ssid: WiFi AP SSID ("BridgeAP").
wifi_ap_updated: WiFi AP configuration updated flag (false).
wifi_sta_authmode: WiFi STA authentication mode (6).
wifi_sta_channel: WiFi STA channel (11).
wifi_sta_pass: WiFi STA password ("8165044699").
wifi_sta_ssid: WiFi STA SSID ("TP-Link_C49C").
wifi_sta_updated: WiFi STA configuration updated flag (false).
Device (device)
The Device section provides information about the hardware and software of the device.

api_version: API version (14132).
atecc_serial_str: Serial string for ATECC chip ("").
chip_cores: Number of chip cores (1).
chip_features: Chip features (82).
chip_id: Chip identifier (13).
chip_revision: Chip revision (0).
device_id: Device identifier (0).
factory_datetime: Factory date and time ("").
factory_registered: Factory registered flag (false).
firmware_version: Firmware version ("1.0.2").
idf_datetime: IDF date and time ("Jun 21 2024 - 09:35:47").
idf_version: IDF version ("v5.2.2-172-gb63fd4eaee").
model: Device model ("ST-INE-002-004").
name: Device name ("ST-INE-002-004").
serial_number: Serial number ("").
token: Device token ("").
State (state)
The State section provides real-time information about the device's operational status, including network status and sensor readings.

### Mesh
- mesh_childs: Number of mesh children (0).
- mesh_childs_total: Total number of mesh children (0).
- mesh_connected: Mesh connected status (true).
- mesh_init: Mesh initialization status (true).
- mesh_layer: Mesh network layer (2).
- mesh_mac: Mesh MAC address ("39:39:39:39:38:38").
- mesh_parent_rssi: Mesh parent RSSI value (-75).
- parent_addr: Parent address ("00:00:00:6c:f3:85").
- root_addr: Root address ("90:38:0c:ac:5f:0d").

### Sensors
- accel: Accelerometer data.
    - error: Error flag (false).
    - x: X-axis value (-0.042090002447366714).
    - y: Y-axis value (-0.19971400499343872).
    - z: Z-axis value (0.97856205701828).
- ambient: Ambient sensor data.
    - air_quality: Air quality (0).
    - altitude: Altitude (0).
    - error: Error flag (false).
    - humidity: Humidity (0).
    - pressure: Pressure (0).
    - temperature: Temperature (0).
- battery: Battery status.
    - adc_imon: ADC current monitoring (16).
    - capacity: Battery capacity (0).
    - charge_current: Charge current (0).
    - error: Error flag (false).
    - input_charge: Input charge (112.5).
    - input_current_limit: Input current limit (800).
    - input_voltage: Input voltage (11960).
    - is_powered: Power status (true).
    - junction_temperature: Junction temperature (45.95899963378906).
    - status0: Status register 0 (27136).
    - status1: Status register 1 (32).
    - system_voltage: System voltage (8340).
    - total_cells: Total number of cells (2).
    - voltage_per_cell: Voltage per cell (3595).
- compass: Compass data.
    - error: Error flag (false).
    - x: X-axis value (0).
    - y: Y-axis value (0).
    - z: Z-axis value (0).
- gps: GPS data.
    - altitude: Altitude (0).
    - error: Error flag (false).
    - latitude: Latitude (0).
    - longitude: Longitude (0).
- gyros: Gyroscope data.
    - error: Error flag (false).
    - x: X-axis value (0).
    - y: Y-axis value (0).
    - z: Z-axis value (0).
- lux_color: Light color sensor data.
    - b: Blue component (255).
    - error: Error flag (false).
    - g: Green component (255).
    - r: Red component (255).
    - w: White component (255).
- noise: Noise sensor data.
    - db: Noise level in decibels (0).
    - error: Error flag (false).
    - mv: Millivolt value (0).
    - raw: Raw sensor value (0).
- total_errors: Total number of errors (2).
- total_reads: Total number of reads (0).
- total_sents: Total number of sends (0).
- total_stores: Total number of stores (0).
- total_time: Total operational time (12 seconds).
- unixtime: Unix time (94583).


