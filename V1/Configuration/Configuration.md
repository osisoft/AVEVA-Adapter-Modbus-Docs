---
uid: ModbusConfiguration
---

# Configuration

PI Adapter for Modbus TCP provides configuration of data source and data selection.

The examples in the configuration topics use `curl`, a commonly available tool on both Windows and Linux. You can configure the adapter with any programming language or tool that supports making REST calls or with the EdgeCmd utility. For more information, see the [EdgeCmd utility documentation (https://osisoft.github.io/Edgecmd-Docs/V1.1/edgecmd-utility.html)](https://osisoft.github.io/Edgecmd-Docs/V1.1/edgecmd-utility.html). To validate successful configurations, you can perform data retrieval (`GET` commands) with a browser, if available, on your device.

For more information on PI Adapter configuration tools, see [Configuration tools](xref:ConfigurationTools).

## Quick start

Complete the following steps to establish a data flow from a Modbus TCP data source device to a data endpoint.

1. Configure one or several Modbus TCP system components.<br>See [System components configuration](xref:SystemComponentsConfiguration#add-a-system-component).

2. Configure a Modbus TCP data source for each Modbus TCP device.<br>See [PI Adapter for Modbus TCP data source configuration](xref:PIAdapterForModbusTCPDataSourceConfiguration#configure-modbus-tcp-data-source).

3. Configure a Modbus TCP data selection for each Modbus TCP data source.<br>See [PI Adapter for Modbus TCP data selection configuration](xref:PIAdapterForModbusTCPDataSelectionConfiguration#configure-modbus-tcp-data-selection).

4. Configure one or several egress endpoints.<br>See [Egress endpoints configuration](xref:EgressEndpointsConfiguration).
