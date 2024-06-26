# Conexión de nodo WebSocket

Este documento ofrece un resumen de la configuración y la estructura de estado para la conexión por WebSocket a los nodos. Las configuraciones y estados están organizados en categorías como config, intervals, light, location, network, device y state. Cada categoría contiene varios parámetros que definen los ajustes y el estado operativo de los nodos.

# Comandos

1. [get-nodes](#get-nodes)
2. [get-node](#get-node)
3. [init](#init)
4. [set-network](#set-network)
   
## get-nodes

El comando `get-nodes` se utiliza para solicitar la lista de todos los nodos actualmente alimentados en la red. Este comando es esencial para los administradores de red para obtener una visión general de los dispositivos activos y sus estados. Cuando se envía este comando, el servidor responde con detalles sobre cada nodo alimentado, incluyendo su configuración y estado actual.

**command y data**
```json
{
  "command": "get-nodes",
  "data": {}
}
```
**Ejemplo de respuesta JSON**
```json
{
"command": "get-nodes"
"data":{
 "node_data":[
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
],
"node_data_size": 2,
"node_list": [
    "40:4c:ca:45:1e:08",
    "40:4c:ca:4b:35:a4"
  ],
"node_list_size": 3
}
}
```
## command
acción realizada.

## data
Datos de todos los nodos visibles
  
### node_data
#### config
configuración general del dispositivo

##### DateTime
Configuración relacionada con la fecha y hora del dispositivo.

- save: Indica si se guarda la configuración.
  
- sntp_server: Servidor SNTP utilizado para la sincronización de tiempo.
  
- sync_to_unixtime: Valor de tiempo UNIX al que se sincroniza.

- sync_with_sntp: Indica si la sincronización con SNTP está activada.

- timezone: Zona horaria configurada en formato de reglas de cambio de horario.

- updated: Indica si la configuración ha sido actualizada.

##### Intervals
Configuración de intervalos de tiempo para operaciones periódicas.

- read: Intervalo de lectura de datos.

- save: Indica si se guardan los intervalos configurados.

- send: Intervalo de envío de datos.

- store: Intervalo de almacenamiento de datos.

- updated: Indica si la configuración de intervalos ha sido actualizada.

##### Light
Configuración de la luz o iluminación.

- blink_color: Configuración del parpadeo de color.

  - blink_color_b: Valor de azul para el color del parpadeo.

  - blink_color_error: Indica si hay un error en el color del parpadeo.

  - blink_color_g: Valor de verde para el color del parpadeo.

  - blink_color_r: Valor de rojo para el color del parpadeo.

  - blink_color_w: Valor de blanco para el color del parpadeo.

- blink_duration: Duración del parpadeo en milisegundos.

- blink_time: Tiempo de inicio del parpadeo en milisegundos.

- blink_type: Tipo de parpadeo.

- color: Configuración del color de la luz.
  
     - b: Valor de azul para la luz.

     - error: Indica si hay un error en el color de la luz.
     
     - g: Valor de verde para la luz.
     
     - r: Valor de rojo para la luz.
     
     - w: Valor de blanco para la luz.

- mode: Modo de la luz.

- restart_mode: Modo de reinicio.

- save: Indica si se guarda la configuración de luz.

- updated: Indica si la configuración de luz ha sido actualizada.

##### Location
Configuración de la ubicación.

- category_id: ID de la categoría de ubicación.

- family_id: ID de la familia de ubicación.

###### gps_position
Posición GPS.

- altitude: Altitud GPS.
    
- error: Indica si hay un error en la posición GPS.
    
- latitude: Latitud GPS.
    
- longitude: Longitud GPS.

- group_id: ID del grupo.

- location_id: ID de la ubicación.

- location_name: Nombre de la ubicación.

- save: Indica si se guarda la configuración de ubicación.

- updated: Indica si la configuración de ubicación ha sido actualizada.


##### Network
Configuración de red.

- mesh_authmode: Modo de autenticación de malla.

- mesh_channel: Canal de malla.

- mesh_channel_switch: Interruptor de cambio de canal de malla.

##### mesh_config
Valores detallados en la configuración de malla

 - assoc_expire_ms: Tiempo de expiración de asociación.
    
 - attempt_count: Número de intentos de conexión.
    
 - backoff_rssi: Valor de RSSI de retroceso.
    
 - beacon_interval_ms: ntervalo de baliza.
    
 - capacity_num: Número de capacidad.
    
 - cnx_rssi: Valor de RSSI de conexión.
    
 - data_drop_enable: Indicador de habilitación de descarte de datos.
    
 - max_connection: Número máximo de conexiones.
    
 - max_layer: Máxima capa de red.
    
 - max_layer_deprecated: Capa máxima de red (obsoleta).
    
 - monitor_duration_ms: Duración de monitoreo.
    
 - monitor_ie_count: Cantidad de elementos de información de monitoreo.
    
 - passive_scan_ms: Duración de escaneo pasivo.
    
 - retransmit_enable: Indicador de habilitación de retransmisión.
    
 - root_conflicts_enable: Indicador de habilitación de conflictos de raíz.
    
 - root_healing_ms: Duración de recuperación de raíz.
    
 - scan_min_count: Cantidad mínima de escaneos.
    
 - select_rssi: Valor de RSSI de selección.
    
 - switch_rssi: Valor de RSSI de cambio.
    
 - topology: Topología de red.
    
 - vote_max_count: Número máximo de votos.
    
 - vote_percentage: Porcentaje de votos.
    
 - xon_qsize: Tamaño de la cola XON.



- mesh_id: ID de la malla.

- mesh_node_type: Tipo de nodo de malla.

- mesh_pass: Contraseña de la malla.

- mesh_root_type: Tipo de raíz de malla.

- mesh_router_switch: Interruptor de enrutador de malla.

- mesh_updated: Indica si la configuración de malla ha sido actualizada.

- ping_interval: Intervalo de ping.

- ping_threshold: Umbral de ping.

- save: Indica si se guarda la configuración de red.

- updated: Indica si la configuración de red ha sido actualizada.

- wifi_ap_authmode: Modo de autenticación del punto de acceso WiFi.

- wifi_ap_channel: Canal del punto de acceso WiFi.

- wifi_ap_pass: Contraseña del punto de acceso WiFi.

- wifi_ap_ssid: SSID del punto de acceso WiFi.

- wifi_ap_updated: Indica si la configuración del punto de acceso WiFi ha sido actualizada.

- wifi_sta_authmode: Modo de autenticación de la estación WiFi.

- wifi_sta_channel: Canal de la estación WiFi.

- wifi_sta_pass: Contraseña de la estación WiFi.

- wifi_sta_ssid: SSID de la estación WiFi.

- wifi_sta_updated: Indica si la configuración de la estación WiFi ha sido actualizada.

- save: Indica si la configuración correspondiente se debe guardar o no.

- update: Indica si ha habido una actualización reciente en la configuración.

- version: Versión de la configuración de red.

#### Device
La sección de Device proporciona información sobre el hardware y software del dispositivo.

- api_version: Versión de la API.

- atecc_serial_str: Cadena serial para el chip ATECC.

- chip_cores: Número de núcleos del chip.

- chip_features: Características del chip.

- chip_id: Identificador del chip.

- chip_revision: Revisión del chip.

- device_id: Identificador del dispositivo.

- factory_datetime: Fecha y hora de fabricación.

- factory_registered: Indicador de registro en fábrica.

- firmware_version: Versión del firmware.

- idf_datetime: Fecha y hora del IDF.

- idf_version: Versión del IDF.

- model: Modelo del dispositivo.

- name: Nombre del dispositivo.

- serial_number: Número de serie del dispositivo.

- token: Token del dispositivo.

- mac_address: Dirección MAC del dispositivo.


#### State
La sección de State proporciona información en tiempo real sobre el estado operativo del dispositivo, incluido el estado de la red y las lecturas de sensores.

##### Mesh

- mesh_childs: Número de hijos en la malla.

- mesh_childs_total: Número total de hijos en la malla.

- mesh_connected: Estado de conexión de la malla.

- mesh_init: Estado de inicialización de la malla.

- mesh_layer: Capa de red de la malla.

- mesh_mac: Dirección MAC de la malla.

- mesh_parent_rssi: Valor de RSSI del padre de la malla.

- parent_addr: Dirección del padre.

- root_addr: Dirección de la raíz.

##### Sensors

###### accel
Datos del acelerómetro.

- error: Indicador de error.
    
- x: Valor del eje X.
    
- y: Valor del eje Y.
    
- z: Valor del eje Z.

###### ambient
Datos del sensor ambiental.

- air_quality: Calidad del aire.
    
- altitude: Altitud.
    
- error: Indicador de error.
    
- humidity: Humedad.
    
- pressure: Presión.
    
- temperature: Temperatura.

###### battery
Estado de la batería.

- adc_imon: Monitoreo actual del ADC.

- capacity: Capacidad de la batería.

- charge_current: Corriente de carga.

- error: Indicador de error.

- input_charge: Carga de entrada.

- input_current_limit: Límite de corriente de entrada.

- input_voltage: Voltaje de entrada.

- is_powered: Estado de alimentación.

- junction_temperature: Temperatura de la unión.

- status0: Registro de estado 0.

- status1: Registro de estado 1.

- system_voltage: Voltaje del sistema.

- total_cells: Número total de celdas.

- voltage_per_cell: Voltaje por celda.

###### compass
Datos del sensor de brújula.

- error: Indicador de error.

- x: Valor del eje X.

- y: Valor del eje Y.

- z: Valor del eje Z.

###### gps
Datos del GPS.
    
-altitude: Altitud.

-error: Indicador de error.

-latitude: Latitud.

-longitude: Longitud.

###### gyros
Datos del giroscopio.
    
- error: Indicador de error.

- x: Valor del eje X.

- y: Valor del eje Y.

- z: Valor del eje Z.

###### lux_color
Datos del sensor de color de luz.
    
- b: Componente azul.

- error: Indicador de error.

- g: Componente verde.

- r: Componente rojo.

- w: Componente blanco.

###### noise
Datos del sensor de ruido.
    
- db: Nivel de ruido en decibelios.
  
- error: Indicador de error.

- mv: Valor en milivoltios.

- raw: Valor crudo del sensor.

- total_errors: Número total de errores.

- total_reads: Número total de lecturas.

- total_sents: Número total de envíos.

- total_stores: Número total de almacenamientos.

- total_time: Tiempo total de funcionamiento.

- unixtime: Tiempo Unix.

### node_data_size
Es un número que indica la cantidad de elementos en node_data

### node_list
contiene una lista de direcciones MAC que identifican los nodos.

### node_list_size
Es un número que indica la cantidad de elementos en node_list (contando el bridge).









## get-node
El comando `get-node` se utiliza para obtener información detallada sobre un nodo específico en la red mediante su dirección MAC única. Este comando es fundamental para recopilar datos exhaustivos sobre un dispositivo IoT particular, incluyendo detalles como el ID del dispositivo, número de serie (si está disponible), configuración de red específica, estado operativo actual (como su capa en una red de malla), y otros parámetros relevantes.

**command y data**
```json
{
  "command": "get-node",
  "data": {
    "mac_address": ""
  }
}
```
**Ejemplo de respuesta JSON**
```json
{
  "mac_address": "40:4c:ca:45:1e:08",
  "device": {
    "device_id": 0,
    "serial_number": "",
    "model": "ST-INE-002-004",
    "name": "ST-INE-002-004",
    "token": "",
    "atecc_serial_str": "",
    "firmware_version": "1.0.2",
    "idf_version": "v5.2.2-185-g018409d99b",
    "idf_datetime": "Jun 25 2024 - 09:42:41",
    "api_version": 12596,
    "chip_id": 13,
    "chip_features": 82,
    "chip_revision": 0,
    "chip_cores": 1,
    "factory_registered": false,
    "factory_datetime": ""
  },
  "config": {
    "version": 1,
    "updated": true,
    "save": true,
    "datetime": {
      "updated": true,
      "save": true,
      "sync_to_unixtime": 0,
      "timezone": "CET-1CEST,M3.5.0,M10.5.0/3",
      "sync_with_sntp": false,
      "sntp_server": "pool.ntp.org"
    },
    "location": {
      "updated": false,
      "save": true,
      "category_id": 0,
      "group_id": 0,
      "family_id": 0,
      "location_id": 0,
      "location_name": "",
      "gps_position": {
        "error": false,
        "latitude": 0,
        "longitude": 0,
        "altitude": 0
      }
    },
    "network": {
      "updated": true,
      "save": true,
      "ping_interval": 15000,
      "ping_threshold": 3,
      "wifi_ap_updated": false,
      "wifi_ap_ssid": "BridgeAP",
      "wifi_ap_pass": "password",
      "wifi_ap_authmode": 6,
      "wifi_ap_channel": 11,
      "wifi_sta_updated": false,
      "wifi_sta_ssid": "TP-Link_C49C",
      "wifi_sta_pass": "8165044699",
      "wifi_sta_authmode": 6,
      "wifi_sta_channel": 11,
      "mesh_updated": false,
      "mesh_id": "999999",
      "mesh_pass": "password",
      "mesh_authmode": 6,
      "mesh_channel": 11,
      "mesh_channel_switch": 0,
      "mesh_router_switch": 0,
      "mesh_root_type": 1,
      "mesh_node_type": 2,
      "mesh_config": {
        "vote_percentage": 90,
        "vote_max_count": 15,
        "backoff_rssi": -98,
        "scan_min_count": 10,
        "root_conflicts_enable": false,
        "root_healing_ms": 6000,
        "capacity_num": 100,
        "max_layer_deprecated": 0,
        "max_connection": 10,
        "assoc_expire_ms": 30000,
        "beacon_interval_ms": 100,
        "passive_scan_ms": 300,
        "monitor_duration_ms": 30000,
        "cnx_rssi": -118,
        "select_rssi": -78,
        "switch_rssi": -98,
        "attempt_count": 30,
        "monitor_ie_count": 10,
        "xon_qsize": 64,
        "retransmit_enable": true,
        "data_drop_enable": true,
        "max_layer": 101,
        "topology": 1
      }
    },
    "light": {
      "updated": false,
      "save": true,
      "mode": 0,
      "color": {
        "error": false,
        "r": 255,
        "g": 255,
        "b": 255,
        "w": 255
      },
      "blink_type": 0,
      "blink_time": 500,
      "blink_duration": 500,
      "blink_color": {
        "blink_color_error": false,
        "blink_color_r": 255,
        "blink_color_g": 255,
        "blink_color_b": 255,
        "blink_color_w": 255
      },
      "restart_mode": 1
    },
    "intervals": {
      "updated": true,
      "save": true,
      "read": 5000,
      "store": 60000,
      "send": 30000
    }
  },
  "state": {
    "mesh": {
      "mesh_init": true,
      "mesh_connected": true,
      "mesh_mac": "39:39:39:39:39:39",
      "mesh_layer": 2,
      "mesh_childs": 0,
      "mesh_childs_total": 0,
      "mesh_parent_rssi": -32,
      "parent_addr": "01:30:75:8a:b2:9e",
      "root_addr": "30:c9:22:9b:c7:e1"
    },
   "sensors": {
      "unixtime": 1719314604,
      "total_time": 12,
      "total_errors": 2,
      "total_reads": 0,
      "total_stores": 0,
      "total_sents": 0,
      "battery": {
        "error": false,
        "is_powered": true,
        "total_cells": 2,
        "input_voltage": 11960,
        "input_charge": 118.75,
        "system_voltage": 8340,
        "input_current_limit": 800,
        "voltage_per_cell": 3595,
        "charge_current": 0,
        "juntion_temperature": 41.39659881591797,
        "status0": 27136,
        "status1": 32,
        "adc_imon": 11,
        "capacity": 0
      },
      "ambient": {
        "error": false,
        "temperature": 0,
        "humidity": 0,
        "pressure": 0,
        "altitude": 0,
        "air_quality": 0
      },
      "lux_color": {
        "error": false,
        "r": 255,
        "g": 255,
        "b": 255,
        "w": 255
      },
      "noise": {
        "error": false,
        "raw": 0,
        "mv": 0,
        "db": 0
      },
      "accel": {
        "error": false,
        "x": -0.034404002130031586,
        "y": -0.28255200386047363,
        "z": 0.963312029838562
      },
      "gyros": {
        "error": false,
        "x": 0,
        "y": 0,
        "z": 0
      },
      "compass": {
        "error": false,
        "x": 0,
        "y": 0,
        "z": 0
      },
      "gps": {
        "error": false,
        "latitude": 0,
        "longitude": 0,
        "altitude": 0
      }
    }
  }
}
```
### mac_address
Es la dirección MAC del dispositivo.

### device
contiene información detallada sobre un dispositivo específico.

- device_id: Un identificador único para el dispositivo.

- serial_number: El número de serie del dispositivo.

- model: El modelo del dispositivo.

- name: El nombre del dispositivo, que en este caso es el mismo que el modelo.

- token: Un token de seguridad para autenticar el dispositivo.

- atecc_serial_str: El número de serie del chip ATECC (un chip de seguridad).

- firmware_version: La versión del firmware instalado en el dispositivo.

- idf_version: La versión del ESP-IDF (Espressif IoT Development Framework) utilizada.

- idf_datetime: La fecha y hora de compilación del ESP-IDF.

- api_version: La versión de la API utilizada por el dispositivo.

- chip_id: Un identificador del chip utilizado en el dispositivo.

- chip_features: Las características del chip, representadas en un valor numérico.

- chip_revision: La revisión del chip.

- chip_cores: El número de núcleos del chip.

- factory_registered: Indica si el dispositivo ha sido registrado en la fábrica.

- factory_datetime: La fecha y hora de registro en la fábrica.


### config
configuración general del dispositivo

- version: La versión de la configuración del dispositivo.

- updated: Indica si la configuración ha sido actualizada recientemente.

- save: Indica si la configuración debe ser guardada.

#### datetime
Configuración relacionada con la fecha y hora del dispositivo.

- updated: Indica si la configuración de fecha y hora ha sido actualizada recientemente.

- save: Indica si la configuración de fecha y hora debe ser guardada.

- sync_to_unixtime: El tiempo UNIX al cual sincronizar.

- timezone: La zona horaria del dispositivo.

- sync_with_sntp: Indica si debe sincronizarse con un servidor SNTP.

- sntp_server: El servidor SNTP para la sincronización de la hora.
 
#### location
configuración de ubicación del dispositivo

- updated: Indica si la configuración de ubicación ha sido actualizada recientemente.

- save: Indica si la configuración de ubicación debe ser guardada.

- category_id: El ID de la categoría de ubicación.

- group_id: El ID del grupo de ubicación.

- family_id: El ID de la familia de ubicación.

- location_id: El ID de la ubicación específica.

- location_name: El nombre de la ubicación.

##### gps_position
Contiene información de la posición GPS.

- error: Indica si hay un error en la posición GPS.

- latitude: La latitud de la ubicación.

- longitude: La longitud de la ubicación.

- altitude: La altitud de la ubicación.
 
#### network
configuración de red del dispositivo

- updated: Indica si la configuración de red ha sido actualizada recientemente.

- save: Indica si la configuración de red debe ser guardada.

- ping_interval: Intervalo de ping en milisegundos.

- ping_threshold: Umbral de ping antes de considerar la conexión caída.

- wifi_ap_updated: Indica si la configuración del punto de acceso Wi-Fi ha sido actualizada.

- wifi_ap_ssid: El SSID del punto de acceso Wi-Fi.

- wifi_ap_pass: La contraseña del punto de acceso Wi-Fi.

- wifi_ap_authmode: El modo de autenticación del punto de acceso Wi-Fi.

- wifi_ap_channel: El canal del punto de acceso Wi-Fi.

- wifi_sta_updated: Indica si la configuración de la estación Wi-Fi ha sido actualizada.

- wifi_sta_ssid: El SSID de la estación Wi-Fi.

- wifi_sta_pass: La contraseña de la estación Wi-Fi.

- wifi_sta_authmode: El modo de autenticación de la estación Wi-Fi.

- wifi_sta_channel: El canal de la estación Wi-Fi.

- mesh_updated: Indica si la configuración de la red mesh ha sido actualizada.

- mesh_id: El ID de la red mesh.

- mesh_pass: La contraseña de la red mesh.

- mesh_authmode: El modo de autenticación de la red mesh.

- mesh_channel: El canal de la red mesh.

- mesh_channel_switch: Indica si el cambio de canal en la red mesh está habilitado.

- mesh_router_switch: Indica si el cambio de router en la red mesh está habilitado.

- mesh_root_type: El tipo de nodo raíz en la red mesh.

- mesh_node_type: El tipo de nodo en la red mesh.

##### mesh_config

- vote_percentage: Porcentaje de votos requerido para tomar decisiones en la red mesh.

- vote_max_count: Número máximo de votos permitidos.

- backoff_rssi: Nivel de RSSI para el retroceso.

- scan_min_count: Número mínimo de escaneos antes de tomar decisiones.

- root_conflicts_enable: Indica si está habilitada la resolución de conflictos de nodos raíz.

- root_healing_ms: Tiempo en milisegundos para la curación de nodos raíz.

- capacity_num: Número de capacidad para la red mesh.

- max_layer_deprecated: Máximo número de capas (obsoleto).

- max_connection: Número máximo de conexiones permitidas.

- assoc_expire_ms: Tiempo en milisegundos para la expiración de asociaciones.

- beacon_interval_ms: Intervalo de beacon en milisegundos.

- passive_scan_ms: Duración del escaneo pasivo en milisegundos.

- monitor_duration_ms: Duración del monitoreo en milisegundos.

- cnx_rssi: Nivel de RSSI para la conexión.

- select_rssi: Nivel de RSSI para la selección.

- switch_rssi: Nivel de RSSI para el cambio.

- attempt_count: Número de intentos permitidos.

- monitor_ie_count: Número de IE a monitorear.

- xon_qsize: Tamaño de la cola XON.

- retransmit_enable: Indica si la retransmisión está habilitada.

- data_drop_enable: Indica si el abandono de datos está habilitado.

- max_layer: Número máximo de capas permitido.

- topology: La topología de la red mesh.
  
#### light
configuración de la luz del dispositivo, incluyendo los colores, el parpadeo y el modo de reinicio.

- updated: Indica si la configuración de la luz ha sido actualizada recientemente.

- save: Indica si la configuración de la luz debe ser guardada.

- mode: El modo de operación de la luz.

- color: Contiene la configuración del color de la luz.

- error: Indica si hay un error en la configuración del color.

- r: Valor de rojo en la configuración del color.

- g: Valor de verde en la configuración del color.

- b: Valor de azul en la configuración del color.

- w: Valor de blanco en la configuración del color.

- blink_type: El tipo de parpadeo de la luz.

- blink_time: Tiempo de parpadeo en milisegundos.

- blink_duration: Duración del parpadeo en milisegundos.

- blink_color: Contiene la configuración del color del parpadeo.

- blink_color_error: Indica si hay un error en la configuración del color del parpadeo.

- blink_color_r: Valor de rojo en la configuración del color del parpadeo.

- blink_color_g: Valor de verde en la configuración del color del parpadeo.

- blink_color_b: Valor de azul en la configuración del color del parpadeo.

- blink_color_w: Valor de blanco en la configuración del color del parpadeo.

- restart_mode: El modo de operación después de reiniciar.

#### intervals
configuración de los intervalos de tiempo para diferentes operaciones del dispositivo, como leer, almacenar y enviar datos.

- updated: Indica si la configuración de los intervalos ha sido actualizada recientemente.

- save: Indica si la configuración de los intervalos debe ser guardada.

- read: Intervalo de lectura en milisegundos.

- store: Intervalo de almacenamiento en milisegundos.

- send: Intervalo de envío en milisegundos.

### state
estado actual del dispositivo en la red mesh

#### mesh
estado actual del dispositivo en la red mesh.

- mesh_init: Indica si la red mesh ha sido inicializada.

- mesh_connected: Indica si el dispositivo está conectado a la red mesh.

- mesh_mac: La dirección MAC del dispositivo en la red mesh.

- mesh_layer: La capa del dispositivo en la red mesh.

- mesh_childs: El número de nodos hijos conectados directamente al dispositivo.

- mesh_childs_total: El número total de nodos hijos en la red mesh.

- mesh_parent_rssi: Nivel de RSSI del nodo padre.

- parent_addr: La dirección del nodo padre en la red mesh.

- root_addr: La dirección del nodo raíz en la red mesh.


#### sensors
Datos recogidos por varios sensores del dispositivo.

- unixtime: Marca de tiempo UNIX actual.

- total_time: Tiempo total de funcionamiento de los sensores en segundos.

- total_errors: Número total de errores detectados por los sensores.

- total_reads: Número total de lecturas realizadas por los sensores.

- total_stores: Número total de almacenamientos realizados por los sensores.

- total_sents: Número total de envíos realizados por los sensores.

##### battery

- error: Indica si hay un error en los datos de la batería.

- is_powered: Indica si el dispositivo está alimentado.

- total_cells: Número total de celdas de la batería.

- input_voltage: Voltaje de entrada en milivoltios.

- input_charge: Carga de entrada en amperios-hora.

- system_voltage: Voltaje del sistema en milivoltios.

- input_current_limit: Límite de corriente de entrada en amperios.

- voltage_per_cell: Voltaje por celda en milivoltios.

- charge_current: Corriente de carga en amperios.

- juntion_temperature: Temperatura de la unión en grados Celsius.

- status0: Estado de la batería (0).

- status1: Estado de la batería (1).

- adc_imon: Corriente medida por el ADC.

- capacity: Capacidad de la batería.
  
##### ambient

- error: Indica si hay un error en los datos ambientales.

- temperature: Temperatura ambiente en grados Celsius.

- humidity: Humedad ambiente en porcentaje.

- pressure: Presión atmosférica en Pascales.

- altitude: Altitud en metros sobre el nivel del mar.

- air_quality: Calidad del aire.
  
##### lux_color

- error: Indica si hay un error en los datos de luz y color.

- r: Valor de rojo en la configuración del color.

- g: Valor de verde en la configuración del color.

- b: Valor de azul en la configuración del color.

- w: Valor de blanco en la configuración del color.

##### noise

- error: Indica si hay un error en los datos de ruido.

- raw: Valor crudo del ruido.

- mv: Valor en milivoltios del ruido.

- db: Nivel de decibelios del ruido.
  
##### accel

- error: Indica si hay un error en los datos del acelerómetro.

- x: Aceleración en el eje X.

- y: Aceleración en el eje Y.

- z: Aceleración en el eje Z.
  
##### gyros

- error: Indica si hay un error en los datos del giroscopio.

- x: Velocidad angular en el eje X.

- y: Velocidad angular en el eje Y.

- z: Velocidad angular en el eje Z.

##### compass

- error: Indica si hay un error en los datos del magnetómetro.

- x: Valor del campo magnético en el eje X.

- y: Valor del campo magnético en el eje Y.

- z: Valor del campo magnético en el eje Z.

##### gps

- error: Indica si hay un error en los datos del GPS.

- latitude: Latitud geográfica.

- longitude: Longitud geográfica.

- altitude: Altitud sobre el nivel del mar.






## init
`init` es el primer comando o mensaje enviado por un cliente WebSocket para iniciar la conexión con un servidor WebSocket, facilitando así la comunicación bidireccional en tiempo real entre ambos extremos.

**command y data**
```json
{
  "command": "init",
  "data": {
    "protocol": 1,
    "security_token": ""
  }
}
```
**Ejemplo de respuesta JSON**
```json
{
  "device": {
    "device_id": 114,
    "serial_number": "0450-D0B7-7017-DC22",
    "model": "ST-INE-003-002",
    "name": "Visualfy Bridge",
    "token": "1c62ef10f4a492b8638c5169359b54aa95984296c2b2149cb7b18441d1352fab",
    "atecc_serial_str": "",
    "firmware_version": "1.0.4",
    "idf_version": "v5.2.2-185-g018409d99b",
    "idf_datetime": "",
    "api_version": 1,
    "chip_id": 1,
    "chip_features": 50,
    "chip_revision": 301,
    "chip_cores": 2,
    "factory_registered": true,
    "factory_datetime": "2024-05-09 18:12:12"
  },
  "config": {
    "test_mode": "TEST_MODE_NONE",
    "datetime": {
      "save": true,
      "sync_to_unixtime": 1719314785,
      "timezone": "CET-1CEST,M3.5.0,M10.5.0/3",
      "sync_with_sntp": true,
      "sntp_server": "pool.ntp.org",
      "unixtime": 1719317151,
      "datetime": "2024-06-25 14:05:51"
    },
    "location": {
      "save": false,
      "category_id": 0,
      "group_id": 0,
      "family_id": 0,
      "location_id": 0,
      "gps_position": {
        "error": false,
        "latitude": 0,
        "longitude": 0,
        "altitude": 0
      }
    },
    "network": {
      "save": true,
      "ping_interval": 15000,
      "ping_threshold": 3,
      "wifi_ap_ssid": "BridgeAP",
      "wifi_ap_pass": "password",
      "wifi_ap_authmode": 6,
      "wifi_ap_channel": 11,
      "wifi_sta_ssid": "TP-Link_C49C",
      "wifi_sta_pass": "8165044699",
      "wifi_sta_authmode": 6,
      "wifi_sta_channel": 11,
      "mesh_id": "999999",
      "mesh_pass": "password",
      "mesh_authmode": 6,
      "mesh_channel": 11,
      "mesh_channel_switch": 0,
      "mesh_router_switch": 0,
      "mesh_root_type": 1,
      "mesh_node_type": 2
    },
    "intervals_bridge": {
      "save": true,
      "read": 5000,
      "store": 60000,
      "send": 5000
    },
    "intervals_node": {
      "save": true,
      "read": 5000,
      "store": 60000,
      "send": 30000
    },
    "server": {
      "https_active": false,
      "task_stack_size": 24576,
      "task_priority": 18,
      "task_core_id": 1,
      "recv_wait_timeout": 2000,
      "send_wait_timeout": 2000
    }
  },
  "state": {
    "current_millis": 0,
    "last_millis": 0,
    "unixtime": 0,
    "unixtime_synced": false,
    "is_gpio_init": true,
    "is_i2c_init": false,
    "is_spi_init": false,
    "is_nvs_init": true,
    "is_lfs_pub_init": true,
    "is_lfs_prv_init": true,
    "is_tcpip_init": true,
    "is_netbios_init": true,
    "is_mdns_init": true,
    "is_sntp_init": true,
    "is_ws_started": true,
    "is_ws_https": false,
    "eth_init": true,
    "eth_connected": true,
    "eth_clients": 0,
    "eth_mac": "30:c9:22:9b:c7:e3",
    "eth_state": 0,
    "eth_has_internet": false,
    "wifi_sta_init": true,
    "wifi_sta_connected": false,
    "wifi_sta_retry_num": 0,
    "wifi_sta_clients": 0,
    "wifi_sta_mac": "30:c9:22:9b:c7:e0",
    "wifi_sta_state": 0,
    "wifi_ap_init": false,
    "wifi_ap_connected": false,
    "wifi_ap_countdown": 0,
    "wifi_ap_clients": 0,
    "wifi_ap_mac": "30:c9:22:9b:c7:e1",
    "wifi_ap_state": 0,
    "bt_mac": "30:c9:22:9b:c7:e2"
  }
}
```
### device

- device_id: Identificador único del dispositivo.

- serial_number: Número de serie del dispositivo.

- model: Modelo del dispositivo.

- name: Nombre asignado al dispositivo.

- token: Token de seguridad del dispositivo.

- atecc_serial_str: Cadena de número de serie del módulo de seguridad ATECC.

- firmware_version: Versión del firmware actual del dispositivo.

- idf_version: Versión del ESP-IDF (Espressif IoT Development Framework).

- idf_datetime: Fecha y hora de compilación del ESP-IDF.

- api_version: Versión de la API utilizada.

- chip_id: ID del chip principal del dispositivo.

- chip_features: Características específicas del chip.

- chip_revision: Revisión del chip.

- chip_cores: Número de núcleos del chip.

- factory_registered: Indica si el dispositivo está registrado en fábrica.

- factory_datetime: Fecha y hora de registro en fábrica.
  
### config

- test_mode: Modo de prueba del dispositivo.
  
#### datetime

- save: Indica si la configuración de fecha y hora se guarda.

- sync_to_unixtime: Hora Unix a la que se sincroniza el dispositivo.

- timezone: Zona horaria configurada para el dispositivo.

- sync_with_sntp: Indica si el dispositivo se sincroniza con un servidor SNTP.

- sntp_server: Servidor SNTP utilizado para la sincronización de hora.

- unixtime: Hora Unix actual del dispositivo.

- datetime: Fecha y hora actual del dispositivo.

#### location

- save: Indica si la configuración de ubicación se guarda.

- category_id: ID de la categoría de ubicación.

- group_id: ID del grupo de ubicación.

- family_id: ID de la familia de ubicación.

- location_id: ID de la ubicación.

#### gps_position

- error: Indica si hay un error en los datos del GPS.

- latitude: Latitud actual del dispositivo.

- longitude: Longitud actual del dispositivo.

- altitude: Altitud actual del dispositivo.

#### network

- save: Indica si la configuración de red se guarda.

- ping_interval: Intervalo de tiempo entre pings en milisegundos.

- ping_threshold: Umbral de pings fallidos antes de considerar que hay un problema.

- wifi_ap_ssid: SSID del punto de acceso WiFi del dispositivo.

- wifi_ap_pass: Contraseña del punto de acceso WiFi del dispositivo.

- wifi_ap_authmode: Modo de autenticación del punto de acceso WiFi.

- wifi_ap_channel: Canal del punto de acceso WiFi.

- wifi_sta_ssid: SSID de la red WiFi a la que se conecta el dispositivo.

- wifi_sta_pass: Contraseña de la red WiFi a la que se conecta el dispositivo.

- wifi_sta_authmode: Modo de autenticación de la red WiFi a la que se conecta el dispositivo.

- wifi_sta_channel: Canal de la red WiFi a la que se conecta el dispositivo.

- mesh_id: Identificador de la red Mesh.

- mesh_pass: Contraseña de la red Mesh.

- mesh_authmode: Modo de autenticación de la red Mesh.

- mesh_channel: Canal de la red Mesh.

- mesh_channel_switch: Indica si la conmutación de canal Mesh está activada.

- mesh_router_switch: Indica si la conmutación de enrutador Mesh está activada.

- mesh_root_type: Tipo de nodo raíz en la red Mesh.

- mesh_node_type: Tipo de nodo en la red Mesh.

#### intervals_bridge

- save: Indica si los intervalos del bridge se guardan.

- read: Intervalo de lectura en milisegundos.

- store: Intervalo de almacenamiento en milisegundos.

- send: Intervalo de envío en milisegundos.

#### intervals_node

- save: Indica si los intervalos del nodo se guardan.

- read: Intervalo de lectura en milisegundos.

- store: Intervalo de almacenamiento en milisegundos.

- send: Intervalo de envío en milisegundos.

#### server

- https_active: Indica si el servidor HTTPS está activo.

- task_stack_size: Tamaño de la pila de tareas del servidor.

- task_priority: Prioridad de la tarea del servidor.

- task_core_id: ID del núcleo en el que se ejecuta la tarea del servidor.

- recv_wait_timeout: Tiempo de espera para recibir datos en milisegundos.

- send_wait_timeout: Tiempo de espera para enviar datos en milisegundos.

### state

- current_millis: Tiempo actual en milisegundos.

- last_millis: Último tiempo registrado en milisegundos.

- unixtime: Tiempo Unix actual.

- unixtime_synced: Indica si el tiempo Unix está sincronizado.

- is_gpio_init: Indica si la inicialización GPIO está completa.

- is_i2c_init: Indica si la inicialización I2C está completa.

- is_spi_init: Indica si la inicialización SPI está completa.

- is_nvs_init: Indica si la inicialización NVS (Non-Volatile Storage) está completa.

- is_lfs_pub_init: Indica si la inicialización de LFS (Little File System) pública está completa.

- is_lfs_prv_init: Indica si la inicialización de LFS privada está completa.

- is_tcpip_init: Indica si la inicialización de TCP/IP está completa.

- is_netbios_init: Indica si la inicialización de NetBIOS está completa.

- is_mdns_init: Indica si la inicialización de mDNS está completa.

- is_sntp_init: Indica si la inicialización de SNTP (Simple Network Time Protocol) está completa.

- is_ws_started: Indica si el servicio WebSocket está iniciado.

- is_ws_https: Indica si el servicio WebSocket está utilizando HTTPS.

- eth_init: Indica si la interfaz Ethernet está inicializada.

- eth_connected: Indica si la interfaz Ethernet está conectada.

- eth_clients: Número de clientes conectados a través de Ethernet.

- eth_mac: Dirección MAC de la interfaz Ethernet.

- eth_state: Estado de la interfaz Ethernet.

- eth_has_internet: Indica si la interfaz Ethernet tiene conexión a Internet.

- wifi_sta_init: Indica si la inicialización de la estación WiFi está completa.

- wifi_sta_connected: Indica si la estación WiFi está conectada.

- wifi_sta_retry_num: Número de intentos de conexión WiFi.

- wifi_sta_clients: Número de clientes conectados a la estación WiFi.

- wifi_sta_mac: Dirección MAC de la estación WiFi.

- wifi_sta_state: Estado de la estación WiFi.

- wifi_ap_init: Indica si la inicialización del punto de acceso WiFi está completa.

- wifi_ap_connected: Indica si el punto de acceso WiFi está conectado.

- wifi_ap_countdown: Contador para el punto de acceso WiFi.

- wifi_ap_clients: Número de clientes conectados al punto de acceso WiFi.

- wifi_ap_mac: Dirección MAC del punto de acceso WiFi.

- wifi_ap_state: Estado del punto de acceso WiFi.

- bt_mac: Dirección MAC del dispositivo Bluetooth.
  
## set-network
El comando `set-network` tiene como objetivo actualizar la configuración de red. La función valida y procesa cada campo de configuración individualmente, actualizando la configuración interna si los datos son válidos. El JSON devuelto consistirá en booleanos que indican si cada valor ha sido modificado dentro de la configuración.

**command y data**
```json
{
  "command": "set-network",
  "data": {
    "save": true,
    "ping_interval": 30,
    "ping_threshold": 5,
    "wifi_ap_ssid": "MySSID",
    "wifi_ap_pass": "MyPassword",
    "wifi_ap_authmode": 3,
    "wifi_ap_channel": 6,
    "wifi_sta_ssid": "MySSID",
    "wifi_sta_pass": "MyPassword",
    "wifi_sta_authmode": 3,
    "wifi_sta_channel": 11,
    "mesh_id": "123456",
    "mesh_pass": "MeshPassword",
    "mesh_authmode": 3,
    "mesh_channel": 1,
    "mesh_channel_switch": 3,
    "mesh_backoff_rssi": -80,
    "mesh_max_capacity": 10,
    "mesh_max_connection": 5,
    "mesh_max_layer": 3
  }
}

```
**Ejemplo de respuesta JSON**
```json 
{
  "save": true,
  "ping_interval": true,
  "ping_threshold": true,
  "wifi_ap_ssid": true,
  "wifi_ap_pass": true,
  "wifi_ap_authmode": true,
  "wifi_ap_channel": true,
  "wifi_sta_ssid": true,
  "wifi_sta_pass": true,
  "wifi_sta_authmode": true,
  "wifi_sta_channel": true,
  "mesh_id": true,
  "mesh_pass": true,
  "mesh_authmode": true,
  "mesh_channel": true,
  "mesh_channel_switch": true,
  "mesh_backoff_rssi": true,
  "mesh_max_capacity": true,
  "mesh_max_connection": true,
  "mesh_max_layer": true
}
```
### data
- save: Indica si se debe guardar la configuración actualizada.
  
- ping_interval: Intervalo de tiempo en segundos entre los pings de mantenimiento de red.
  
- ping_threshold: Umbral mínimo de ping para considerar que la conexión está estable.

- wifi_ap_ssid: Nombre del SSID para el punto de acceso Wi-Fi.

- wifi_ap_pass: Contraseña del punto de acceso Wi-Fi.

- wifi_ap_authmode: Modo de autenticación del punto de acceso Wi-Fi.

- wifi_ap_channel: Canal de transmisión del punto de acceso Wi-Fi.

- wifi_sta_ssid: Nombre del SSID para la estación Wi-Fi (cliente).

- wifi_sta_pass: Contraseña para la conexión como estación Wi-Fi.

- wifi_sta_authmode: Modo de autenticación para la conexión como estación Wi-Fi.

- wifi_sta_channel: Canal de transmisión para la conexión como estación Wi-Fi.

- mesh_id: Identificador único para la red mesh.

- mesh_pass: Contraseña para la red mesh.

- mesh_authmode: Modo de autenticación para la red mesh.

- mesh_channel: Canal de transmisión para la red mesh.

- mesh_channel_switch: Configuración de cambio de canal para la red mesh.

- mesh_backoff_rssi: Valor de RSSI de retroceso para la red mesh.

- mesh_max_capacity: Capacidad máxima de la red mesh.

- mesh_max_connection: Número máximo de conexiones simultáneas en la red mesh.

- mesh_max_layer: Número máximo de capas en la red mesh.
