# Special considerations for upgrdading existing installations of PI Adapter for Modbus

## Upgrading from version 1.4.x or older to version 1.5.x or newer

  ### Input32 and Holding32 Register Types
  In alignment with the Modbus specification, direct support for 32-bit registers has been removed from PI Adapter for Modbus TPC 1.5.x and later. Collecting 32-bit (or larger) values is still possible with PI Adapter for Modbus TPC 1.5.x by configuring different data type codes, where the values collected will be made up of two (or more) 16-bit registers. 

  ### Connect Timeout
  PI Adapter for Modbus should transparently maintain a TCP connection without users needing to worry about specific timeout configurations. Typically, a configurable application-layer level timeout (such as the `RequestTimeout` in the data source configuration) is sufficient to account for any special cases a modbus device may require. 

  However, if specific timeout settings at the TCP layer must be made, please refer to the OS documentation for potential adjustments. 

  ### Simultaneous Requests
  PI Adapter for Modbus TPC 1.5.x and later no longer supports a configurable number of simultaneous requests, as many Modbus devices do not allow multiple connections. In consideration of this change, PI Adapter for Modbus TPC 1.5.x and later includes significant performance improvements for single connections. Alternatively, users may configure multiple adapter components with the same device configuration or configure multiple devices with different hostnames that all resolve to the same physical Modbus device.
