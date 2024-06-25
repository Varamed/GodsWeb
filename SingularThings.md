#WebSocket lamp connection

This document provides an overview of the configuration and state structure for a WebSocket-based application. The configurations and states are organized into categories such as config, intervals, light, location, network, device, and state. Each category contains various parameters that define the settings and operational status of the application.


WebSocket Application Configuration and State Overview
This document provides an overview of the configuration and state structure for a WebSocket-based application. The configurations and states are organized into categories such as config, intervals, light, location, network, device, and state. Each category contains various parameters that define the settings and operational status of the application.

##Configuration (config)
###DateTime
The DateTime configuration handles settings related to date and time, including synchronization with an SNTP server.
-save: A boolean indicating if the settings should be saved (true).
-sntp_server: The address of the SNTP server ("pool.ntp.org").
-sync_to_unixtime: Indicates whether to sync to Unix time (0).
-sync_with_sntp: A boolean indicating whether to sync with the SNTP server (false).
-timezone: The timezone setting ("CET-1CEST,M3.5.0,M10.5.0/3").
-updated: A boolean indicating if the configuration has been updated (true).

