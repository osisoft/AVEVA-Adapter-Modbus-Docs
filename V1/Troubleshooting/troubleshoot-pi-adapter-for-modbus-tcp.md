---
uid: TroubleshootPIAdapterForModbusTCP
---

# Troubleshoot PI Adapter for Modbus TCP

To troubleshoot issues with PI Adapter for Modbus TCP, you can check the adapter's configuration, connectivity, and logs, as detailed in the following sections. If you are unable to resolve issues with the adapter or need additional guidance, contact OSIsoft Technical Support.

## Check configurations

1. In the [data source configuration](xref:PIAdapterForModbusTCPDataSourceConfiguration), verify that each configured device's IP address and port are correct.
2. In the [data selection configuration](xref:PIAdapterForModbusTCPDataSelectionConfiguration), verify that each configured data selection item below is correct:

    1. **DeviceId** - Verify that the referenced device exists in the data source configuration.
    2. **UnitId** - Verify that the correct UnitId number is referenced. <br> A wrong UnitId number can cause the adapter to request data from a different or non-existent device.
    3. **RegisterType** - Verify that the correct RegisterType number or string is referenced.<br>A wrong RegisterType number or string can cause the adapter to not read the correct register groups.
    4. **RegisterOffset** - Verify that the correct RegisterOffset number is referenced.<br>A wrong RegisterOffset number can cause the adapter to request or incorrectly interpret data locations, which results in unexpected values or out-of-range errors.
    5. **DataTypeCode** - Verify that the correct DataTypeCode number is referenced.<br>A wrong DataTypeCode number can cause unexpected values or out-of-range errors.
    6. **ScheduleId** - Verify that the referenced schedule exists.
    7. **DataFilterId** - If configured, verify that the referenced data filter exists.
    8. **BitMap** - If configured, verify that the BitMap is correct.<br>A wrong BitMap can cause unexpected values.

3. In the [egress endpoints configuration](xref:EgressEndpointsConfiguration), verify that each configured endpoint's **Endpoint** property and credentials are correct. For a PI server or EDS endpoint, verify **UserName** and **Password**, for an OCS endpoint, verify **ClientId** and **ClientSecret**.

## Check connectivity

1. Verify there are active connections to the data source and egress endpoints.
2. If you configured a health endpoint, use it to determine the status of the adapter.<br>For more information, see [Health and diagnostics](xref:HealthAndDiagnostics).

## Check logs

1. Check the adapter and endpoint logs to isolate issues. 
2. Optional: Change the log level of the adapter to receive additional information and context.<br>For more information, see [Logging configuration](xref:LoggingConfiguration).

## Simulators

Download an online Modbus simulator, for example *Mod_RSSim* as a data source to troubleshoot the adapter.
