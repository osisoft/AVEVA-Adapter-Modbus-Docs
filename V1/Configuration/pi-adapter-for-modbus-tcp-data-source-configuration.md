---
uid: PIAdapterForModbusTCPDataSourceConfiguration
---

# PI Adapter for Modbus TCP data source configuration

To use the adapter, you must configure the data source from which it polls data.

## Configure Modbus TCP data source

**Note:** You cannot modify Modbus TCP data source configurations manually. You must use the REST endpoints to add or edit the configuration.

Complete the following steps to configure a Modbus TCP data source:

1. Use any text editor to create a file that contains a Modbus TCP data source in the JSON format.
    - For content structure, see [Modbus TCP data source examples](#modbus-tcp-data-source-examples).
    - For a table of all available parameters, see [Modbus TCP data source parameters](#modbus-tcp-data-source-parameters).
2. Save the file. For example, `ConfigureDataSource.json`.
3. Use any of the [Configuration tools](xref:ConfigurationTools) capable of making HTTP requests run a `PUT` command with the contents of the file to the following endpoint: `http://localhost:5590/api/v1/configuration/<adapterId>/DataSource/`.

    **Note:** The following example uses Modbus1 as the adapter component name. For more information on how to add a component, see [System components configuration](xref:SystemComponentsConfiguration).

    `5590` is the default port number. If you selected a different port number, replace it with that value.

    Example using `curl`:

    **Note:** Run this command from the same directory where the file is located.

    ```bash
    curl -d "@ConfigureDataSource.json" -H "Content-Type: application/json" -X PUT "http://localhost:5590/api/v1/configuration/Modbus1/DataSource"
    ```

## Modbus TCP data source schema

The full schema definition for the Modbus data source configuration is in the `Modbus_DataSource_schema.json` file located in one of the following folders:

Windows: `%ProgramFiles%\OSIsoft\Adapters\Modbus\Schemas`

Linux:  `/opt/OSIsoft/Adapters/Modbus/Schemas`

## Modbus TCP data source parameters

The following parameters are available for configuring a Modbus TCP data source.

| Parameter                |Required       | Type      | Description  |
|--------------------------|-----------|-----------|---------------------------------------------------|
| **Devices**               | Required          | Array of objects | List of Modbus devices that this adapter instance reads. All devices read by the adapter share the common configuration defined in this table. For the properties that a device is comprised of, see the [Devices](#devices) table.|
| **StreamIdPrefix**        | Optional          | `string` | Specifies what prefix is used for Stream IDs. The naming convention is `StreamIdPrefix.StreamId`. An empty string means no prefix will be added to the Stream IDs and names. A `null` value defaults to ComponentID followed by a period. <br><br>Example: `Modbus1.{DeviceId}.{UnitId}.{RegisterType}.{RegisterOffset}`<br><br>**Note:** Every time you change the StreamIdPrefix of a configured adapter, for example when you delete and add a data source, you need to restart the adapter for the changes to take place. New streams are created on adapter restart and pre-existing streams are no longer updated.<br><br>Allowed value: any string<br>Default value: `null` |
| **DefaultStreamIdPattern** | Optional          | `string` | Naming pattern used for creating Stream IDs when it is not specified for a data item. <br><br>Default value:<br> `{DeviceId}.{UnitId}.{RegisterType}.{RegisterOffset}`. |
| **ConnectTimeout**        | Optional          | `string` | Parameter to specify the TimeSpan to wait when the adapter is trying to connect to the data source. * <br><br>Minimum value: `00:00:01`<br>Maximum value: `00:00:30` <br>Default value: `00:00:05` |
| **ReconnectInterval**     | Optional          | `string` | Parameter to specify the TimeSpan to wait before retrying to connect to the data source when the data source is offline. * <br><br>Minimum value: `00:00:00.1`<br>Maximum value: `00:00:30` <br>Default value: `00:00:01` |
|**RequestTimeout**         | Optional          | `string` | Parameter to specify the TimeSpan that the adapter waits for a pending request before marking it as timeout and dropping the request. * <br><br>Minimum value: must be positive <br> Maximum value: 48 hours or `02:00:00:00`<br>Default value: `00:00:10` |
|**DelayBetweenRequests**   | Optional          | `string` | Parameter to specify the minimum TimeSpan between two successive requests sent to the data source. * <br><br>Minimum value: `00:00:00`<br>Maximum value: `00:00:01` <br>Default value: `00:00:00` |
|**MaxResponseDataLength**  | Optional          | number | Parameter to limit the maximum length (in bytes) of data that can be read within one transaction. This feature is provided to support devices that limit the number of bytes that can be returned. If there is no device limitation, the request length should be the maximum length of `250` bytes. <br><br>Minimum value: `2`<br> Maximum value: `250`<br>Default value: `250` |
|**SimultaneousRequests**  | Optional          | number | Parameter to allow multiple simultaneous reads from a single IP address and port combination to prevent scan overruns when a lot of data is being read from a single device. <br><br>Minimum value: `1`<br>Maximum value: `16`<br>Default value: `1`|

\* **Note:** You can also specify timespans as numbers in seconds. For example, `"RequestTimeout": 25` specifies 25 seconds, or `"RequestTimeout": 125.5` specifies 2 minutes and 5.5 seconds.

### Devices

The following parameters are available for configuring the 'Devices' parameter of a Modbus TCP data source.

| Parameter                |Required       | Type      | Description  |
|--------------------------|-----------|-----------|---------------------------------------------------|
| **Id**             | Required  | `string` | The ID of the device that is used in data selection to associate a register with a device. |
| **IpAddress**         | Required  | `string` | The IP address of the device from which the data is collected using the Modbus TCP protocol. Host name is not supported. |
| **Port**                  | Optional  | number | The TCP port of the target device that listens for and responds to Modbus TCP requests. The value ranges from `0` to `65535`. If you do not configure it, the default TCP port is `502`, which is the default port for Modbus TCP protocol. |

## Modbus TCP data source examples

The following are examples of valid Modbus TCP data source configurations:

### Minimal data source configuration

```json
{
    "Devices":
    [
        {
            "Id": "Device1",
            "IpAddress": "127.0.0.1"
        }
    ]
}
```

### Complete data source configuration

```json
{
    "Devices":
    [
        {
            "Id": "Device1",
            "IpAddress": "127.0.0.1",
            "Port": 502
        },
        {
            "Id": "Device2",
            "IpAddress": "127.0.0.2",
            "Port": 502
        },
        {
            "Id": "Device3",
            "IpAddress": "127.0.0.3",
            "Port": 502
        }
    ],
    "StreamIdPrefix": "my.prefix",
    "DefaultStreamIdPattern": "{DeviceId}.{UnitId}.{RegisterType}.{RegisterOffset}",
    "ConnectTimeout": "00:00:05",
    "ReconnectInterval": "00:00:01",
    "RequestTimeout": "00:00:10",
    "DelayBetweenRequests": "00:00:00.5",
    "MaxResponseDataLength": 125,
    "SimultaneousRequests": 1
}
```

## REST URLs

| Relative URL | HTTP verb | Action |
| ------------ | --------- | ------ |
| api/v1/configuration/_ComponentId_/DataSource | `GET` | Retrieves the Modbus TCP data source configuration |
| api/v1/configuration/_ComponentId_/DataSource  | `POST` | Creates the Modbus TCP data source configuration |
| api/v1/configuration/_ComponentId_/DataSource | `PUT` | Configures or updates the Modbus TCP data source configuration |
| api/v1/configuration/_ComponentId_/DataSource | `DELETE` | Deletes the Modbus TCP data source configuration |

**Note:** Replace `ComponentId` with the ID of your Modbus TCP component. For example, `Modbus1`.
