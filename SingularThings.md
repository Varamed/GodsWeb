# WebSocket lamp connection

This document provides an overview of the configuration and state structure for a WebSocket-based application. The configurations and states are organized into categories such as config, intervals, light, location, network, device, and state. Each category contains various parameters that define the settings and operational status of the application.


WebSocket Application Configuration and State Overview
This document provides an overview of the configuration and state structure for a WebSocket-based application. The configurations and states are organized into categories such as config, intervals, light, location, network, device, and state. Each category contains various parameters that define the settings and operational status of the application.

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

