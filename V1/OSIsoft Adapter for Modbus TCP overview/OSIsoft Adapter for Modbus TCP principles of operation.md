---
uid: OSIsoftAdapterForModbusTCPPrinciplesOfOperation
---

# OSIsoft Adapter for Modbus TCP principles of operation

This adapters's operations focus on data collection and stream creation.

## Adapter configuration

For the Modbus TCP adapter to start data collection, configure the following:

- Data source: Provide the data source from which the adapter should collect data.
- Data selection: Perform selection of Modbus TCP items to which the adapter should subscribe for data.
- Logging: Set up the logging attributes to manage the adapter logging behavior.

For more details, see [OSIsoft Adapter for Modbus TCP data source configuration](xref:OSIsoftAdapterForModbusTCPDataSourceConfiguration) and [OSIsoft Adapter for Modbus TCP data selection configuration](xref:OSIsoftAdapterForModbusTCPDataSelectionConfiguration).

## Connection

The adapter communicates with the Modbus TCP devices through the TCP/IP network by sending request packets that are constructed based on the data selection configurations, and collects the response packets returned by the devices.

## Data collection

The adapter collects data from the Modbus TCP devices at the polling rates that you specify. The rates are set in each of the data selection configurations and can range from 0 milliseconds (as fast as possible) up to 1 day per polling. The adapter automatically optimizes the data collection process by grouping the requests to reduce the I/O load imposed to the Modbus TCP networks.

### Data types

The adapter converts readings from single or multiple registers into the data types specified by the data type code and populates the value into streams.

The following table lists all data types with their corresponding type codes supported by the adapter.

| Data type code | Data type name | Value type | Register type | Description |
|----------------|----------------|------------|---------------|-------------|
| 1              | Boolean        | Boolean       | Bool          | 0 = false <br> 1 = true
| 10             | Int16          | Int16      | Bool/16-bit   | Read 1 Modbus TCP register and interpret as a 16-bit integer. Bytes [BA] read from the device are stored as [AB]. |
| 20             | UInt16         | UInt16     | Bool/16-bit   | Read 1 Modbus TCP register and interpret as an unsigned 16-bit integer. Bytes [BA] read from the device are stored as [AB]. |
| 30             | Int32          | Int32      | 16-bit/32-bit | Read 32 bits from the Modbus TCP device and interpret as a 32-bit integer. Bytes [DCBA] read from the device are stored as [ABCD]. |
| 31             | Int32ByteSwap  | Int32      | 16-bit/32-bit | Read 32 bits from the Modbus TCP device and interpret as a 32-bit integer. Bytes [BADC] read from the device are stored as [ABCD]. |
| 100            | Float32        | Float32    | 16-bit/32-bit | Read 32 bits from the Modbus TCP device and interpret as a 32-bit float. Bytes [DCBA] read from the device are stored as [ABCD]. |
| 101            | Float32ByteSwap | Float32   | 16-bit/32-bit | Read 32 bits from the Modbus TCP device and interpret as a 32-bit float. Bytes [BADC] read from the device are stored as [ABCD]. |
| 110            | Float64        | Float64    | 16-bit/32-bit | Read 64 bits from the Modbus TCP device and interpret as a 64-bit float. Bytes [HGFEDCBA] read from the device are stored as [ABCDEFGH]. |
| 111            | Float64ByteSwap | Float64   | 16-bit/32-bit | Read 64 bits from the Modbus TCP device and interpret as a 64-bit float. Bytes [BADCFEHG] read from the device are stored as [ABCDEFGH]. |
| 1001 - 1250    | String         | String     | 16-bit/32-bit | 1001 reads a one-character string, 1002 reads a two-character string, and 1003 reads a three-character string and so on. Bytes [AB] are interpreted as "AB". |
| 2001 - 2250    | StringByteSwap | String     | 16-bit/32-bit | 2001 reads a one-character string, 2002 reads a two-character string, and 2003 reads a three-character string and so on. Bytes [BA] are interpreted as "AB". |

## Stream creation

From the parsed data selection configurations, the adapter creates types, streams and data based on the information provided. For each measurement in the data selection configuration, a stream is created to store time series data.

### Streams by Modbus TCP adapter

For each data selection configuration, the adapter creates a stream with two properties, which are described in the following table:

| Property name | Data type | Description |
|---------------|-----------|-------------|
| Timestamp     | String    | The response time of the stream data from the Modbus TCP device. |
| Value         | Specified by the data selection | The value of the stream data from the Modbus TCP device. |

Certain metadata are sent with each stream created. Metadata common for every adapter type are

- **componentId**: Specifies the type of adapter, for example _Modbus_
- **componentType**: Specifies the data source, for example _Modbus1_

Each stream created for the selected measurement has a unique identifier (Stream ID). If a custom stream ID is specified for the measurement in the data selection configuration, the adapter will use that stream ID to create the stream. Otherwise, the connector constructs the stream ID using the following format:

```code
<Adapter Component ID>.<Unit ID>.<Register Type>.<Register Offset>
```

**Note:** Naming convention is affected by StreamIdPrefix and ApplyPrefixToStreamID settings in data source configuration. For more information, see [OSIsoft Adapter for Modbus TCP data source configuration](xref:OSIsoftAdapterForModbusTCPDataSourceConfiguration).
