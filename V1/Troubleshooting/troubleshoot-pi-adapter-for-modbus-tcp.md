---
uid: TroubleshootPIAdapterForModbusTCP
---

# Troubleshoot PI Adapter for Modbus TCP

If you encounter issues with PI Adapter for Modbus TCP, you can attempt to troubleshoot on your own before contacting OSIsoft Technical Support. Start by checking the adapter's configuration, connectivity, and logs. The following sections provide more details.

## Check configurations

1. In the [data source configuration](xref:PIAdapterForModbusTCPDataSourceConfiguration), verify that each configured device's IP address and port are correct.
2. In the [data selection configuration](xref:PIAdapterForModbusTCPDataSelectionConfiguration), verify that each configured data selection item is correct.

    1. For the **DeviceId**, verify that the referenced device exists in the data source configuration.
    2. For the **UnitId**, verify that the correct UnitId number is referenced. <br> A wrong UnitId number can cause the adapter to request data from a different or non-existent device.
    3. For the **RegisterType**, verify that the correct RegisterType number or string is referenced.<br>A wrong RegisterType number or string can cause the adapter to not read the correct register groups.
    4. For the **RegisterOffset**, verify that the correct RegisterOffset number is referenced.<br>A wrong RegisterOffset number can cause the adapter to request or incorrectly interpret data locations, which results in unexpected values or out-of-range errors.
    5. For the **DataTypeCode**, verify that the correct DataTypeCode number is referenced. A wrong DataTypeCode number can cause unexpected values or out-of-range errors.
    6. For the **ScheduleId**, verify that the referenced schedule exists.
    7. If you configured **DataFilterId**, verify that the referenced data filter exists.
    8. If you configured **BitMap**, verify that the BitMap is correct.<br>A wrong bitmap can cause unexpected values.

3. In the [egress endpoints configuration](xref:EgressEndpointsConfiguration), verify that each configured endpoint's **Endpoint** property and credentials are correct (For a PI server or EDS endpoint **UserName** and **Password**, for an OCS endpoint **ClientId** and **ClientSecret**).

## Check connectivity

1. Verify that there are active connections to the data source and egress endpoints.
2. If you configured a health endpoint, use it to determine the status of the adapter.<br>For more information, see [Health and diagnostics](xref:HealthAndDiagnostics).

## Check logs

1. To isolate the issue, check the adapter and endpoint logs.
2. Optional: Change the log level of the adapter to receive more information and context.<br>For more information, see [Logging configuration](xref:LoggingConfiguration).

## Simulators

Download an online Modbus simulator, for example *Mod_RSSim*, and use it to troubleshoot the adapter as data source.
