---
uid: OSIsoftAdapterForModbusTCPPrinciplesOfOperation
---

# OSIsoft Adapter for Modbus TCP principles of operation

This topic provides an operational overview of the Modbus TCP adapter, focusing on streams creation. 

## Adapter configuration
In order for the Modbus TCP adapter to be ready for data collection, you need to configure the adapter by defining the following:

- Data source: Provide the data source from which the adapter should collect data.
- Data selection: Perform selection of Modbus TCP items to which the adapter should subscribe for data.
- Logging: Set up the logging attributes to manage the adapter logging behavior.

For more details, see [OSIsoft Adapter for Modbus TCP data source configuration](xref:OSIsoftAdapterForModbusTCPDataSourceConfiguration) and [OSIsoft Adapter for Modbus TCP data selection configuration](xref:OSIsoftAdapterForModbusTCPDataSelectionConfiguration).

## Connection
The Modbus TCP adapter communicates with the Modbus TCP devices through the TCP/IP network by sending request packets that are constructed based on the data selection configurations, and collects the response packets returned by the devices. 

## Stream creation
From the parsed data selection configurations, the Modbus TCP adapter creates types, streams and data based on the information provided. For each measurement in the data selection configuration, a stream is created in the Edge Data Store to store time series data.

## Data collection
The Modbus TCP adapter collects data from the Modbus TCP devices at the polling rates that you specify. The rates are set in each of the data selection configurations and can range from 0 milliseconds (as fast as possible) up to 1 day per polling. The adapter automatically optimizes the data collection process by grouping the requests to reduce the I/O load imposed to the Modbus TCP networks.

## Streams by Modbus TCP adapter
For each data selection configuration, the Modbus TCP adapter creates a stream with two properties. The properties are described in the following table:

| Property name | Data type | Description |
|---------------|-----------|-------------|
| Timestamp     | String    | The response time of the stream data from the Modbus TCP device. |
| Value         | Specified by the data selection | The value of the stream data from the Modbus TCP device. | 

There is a unique identifier (Stream ID) for each stream created for the selected measurement. If a custom stream ID is specified for the measurement in the data selection configuration, the Modbus TCP adapter will use that stream ID to create the stream. Otherwise, the connector constructs the stream ID using the following format: 
```
<Adapter Component ID>.<Unit ID>.<Register Type>.<Register Offset> 
```
**Note:** Naming convention is affected by StreamIdPrefix and ApplyPrefixToStreamID settings in data source configuration. For more information, see [OSIsoft Adapter for Modbus TCP data source configuration](xref:OSIsoftAdapterForModbusTCPDataSourceConfiguration).
