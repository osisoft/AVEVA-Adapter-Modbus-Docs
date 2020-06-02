---
uid: OSIsoftAdapterForModbusTCPDataSourceConfiguration
---

# OSIsoft Adapter for Modbus TCP data source configuration

To use the adapter, you must configure the data source from which it polls data.

## Configure Modbus TCP data source

**Note:** You cannot modify Modbus TCP data source configurations manually. You must use the REST endpoints to add or edit the configuration.

Complete the following steps to configure a Modbus TCP data source:

1. Using any text editor, create a file that contains a Modbus TCP data source in the JSON format.
    - For content structure, see [Modbus TCP data source examples](#modbus-tcp-data-source-examples).
    - For a table of all available parameters, see [Modbus TCP data source parameters](#modbus-tcp-data-source-parameters).
    
2. Save the file. For example, `DataSource.config.json`.

3. Use any of the [Configuration tools](xref:ConfigurationTools) capable of making HTTP requests run a `PUT` command with the contents of that file to the following endpoint: `http://localhost:5590/api/v1/configuration/<adapterId>/DataSource/`.

    **Note:** The following example uses Modbus1 as the adapter component name. For more information on how to add a component, see [System components configuration](xref:SystemComponentsConfiguration).

    `5590` is the default port number. If you selected a different port number, replace it with that value.

    Example using `curl`:

    **Note:** Run this command from the same directory where the file is located.
    
    ```bash
    curl -d "@DataSource.config.json" -H "Content-Type: application/json" -X PUT "http://localhost:5590/api/v1/configuration/Modbus1/DataSource"
    ```

## Modbus TCP data source schema

The full schema definition for the Modbus data source configuration is in the `Modbus_DataSource_schema.json` file located in one of the files listed below:

Windows: `%ProgramFiles%\OSIsoft\Adapters\Modbus\Schemas`

Linux:  `/opt/OSIsoft/Adapters/Modbus/Schemas`

## Modbus TCP data source parameters

The following parameters are available for configuring a Modbus TCP data source.

| Parameter                |Required       | Type      | Description  |
|--------------------------|-----------|-----------|---------------------------------------------------|
| **Devices**               | Required          | Array of objects | List of Modbus devices that this adapter instance reads. All devices read by the adapter share the common configuration defined in this table. For the properties that a device is comprised of, see the [Devices](#devices) table.|
| **StreamIdPrefix**        | Optional          | `string` | Specifies what prefix is used for Stream IDs. The naming convention is StreamIdPrefix.StreamId. An empty string means no prefix is added to the Stream IDs and names. Null value defaults to ComponentID followed by a dot. <br><br>**Note:** Every time you change the StreamIdPrefix of a configured adapter, for example when you delete and add a data source, you need to restart the adapter for the changes to take place. New streams are created on adapter restart and pre-existing streams are no longer updated. |
| **DefaultStreamIdPattern** | Optional          | `string` | Naming pattern used for creating Stream IDs when it is not specified for a data item. By default, this value is <br> `{DeviceId}.{UnitId}.{RegisterType}.{RegisterOffset}`.|
| **ConnectTimeout**        | Optional          | `string` | Parameter to specify the TimeSpan to wait when the adapter is trying to connect to the data source. The value ranges from `1` sec to `30` sec, represented as TimeSpan strings 00:00:01 and 00:00:30, respectively. The default value is `5` sec, represented as 00:00:05.|
| **ReconnectInterval**     | Optional          | `string` | Parameter to specify the TimeSpan to wait before retrying to connect to the data source when the data source is offline. The value ranges from `100` ms to `30` sec, represented as TimeSpan strings 00:00:00.1 and 00:00:30, respectively. The default value is `1` sec, represented as 00:00:01. |
|**RequestTimeout**         | Optional          | `string` | Parameter to specify the TimeSpan that the adapter waits for a pending request before marking it as timeout and dropping the request. The default value is `10` sec, represented as the TimeSpan string 00:00:10. The value must be positive. There is no value range.|
|**DelayBetweenRequests**   | Optional          | `string` | Parameter to specify the minimum TimeSpan between two successive requests sent to the data source. The value ranges from `0` sec to `1` sec, represented as TimeSpan strings 00:00:00 and 00:00:01, respectively. The default value is `0` sec, represented as 00:00:00.|
|**MaxResponseDataLength**  | Optional          | number | Parameter to limit the maximum length (in bytes) of data that can be read within one transaction. This feature is provided to support devices that limit the number of bytes that can be returned. If there is no device limitation, the request length should be the maximum length of `250` bytes. The value ranges from `2` to `250`. The default value is `250`.|
|**SimultaneousRequests**  | Optional          | number | Parameter to allow multiple simultaneous reads from a single IP address and port combination to prevent scan overruns when a lot of data is being read from a single device. The value ranges from 1 to 16. The default value is 1.|

### Devices

The following parameters are available for configuring the 'Devices' parameter of a Modbus TCP data source.

| Parameter                |Required       | Type      | Description  |
|--------------------------|-----------|-----------|---------------------------------------------------|
| **Id**             | Required  | `string` | The Id of the device that is used in data selection to associate a register with a device. |
| **IpAddress**         | Required  | `string` | The IP address of the device from which the data is collected using the Modbus TCP protocol. Host name is not supported. |
| **Port**                  | Optional  | number | The TCP port of the target device that listens for and responds to Modbus TCP requests. The value ranges from `0` to `65535`. If you do not configure it, the default TCP port is `502`, which is the default port for Modbus TCP protocol. |

## Modbus TCP data source examples

The following are examples of valid Modbus TCP data source configurations:

**Minimum data source configuration:**

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

**Maximum data source configuration:**

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

**Note:** Replace `ComponentId` with the Id of your Modbus TCP component. For example, `Modbus1`.
