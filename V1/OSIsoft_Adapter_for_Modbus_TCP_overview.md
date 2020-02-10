---
uid: OSIsoftAdapterForModbusTCPOverview
---

# OSIsoft Adapter for Modbus TCP overview

Modbus TCP is a commonly available communication protocol used for connecting and transmitting information between industrial electronic devices. 

All adapters are developed operating system-agnostic. You can add a single adapter during installation. For more information, see [Installation](xref:Installation). 

The Modbus TCP adapter is configured with data source and data selection JSON files. It polls Modbus TCP slave devices, and transfers time series data from the data source devices to a defined endpoint. Polling is based on the measurement configuration provided, and models the register measurements in a Modbus TCP data source. The Modbus TCP adapter communicates with any device conforming to the Modbus TCP/IP protocol through a gateway or router. 
