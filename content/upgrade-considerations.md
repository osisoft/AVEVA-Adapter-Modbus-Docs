# Special considerations for upgrdading existing installations of PI Adapter for Modbus

## Upgrading from version 1.4.x or older to version 1.5.x or newer

  ### Input32 and Holding32 Register Types
  32 bit registers are not part of the official Modbus specification. Support for these registers has been removed in an effort to better support users with Modbus devices that are compliant with the specification. 32-bit (or larger) values may still be collected by configuring different data type codes, but the values collected will be made up of 2 (or more) 16-bit registers. 

  ### Connect Timeout
  PI Adapter for Modbus should transparently mantain a TCP connection without users needing to worry about specific timeout configurations. Typically, a configurable application-layer level timeout (such as the `RequestTimeout` in the data source configuration) is sufficient to account for any special cases a modbus device may require. 

  However, if accomodations for specific timeouts at the TCP layer must be made, please refer to the OS documentation for potential adjustments. 

  ### Simultaneous Requests
  In versions prior to 1.5.x, PI Adapter for Modbus allowed a configurable number of requests to be made simultaneously. To achieve this behavior, PI Adapter for Modbus would create multiple connections to each configured device. Many Modbus devices do not allow multiple connections to be made. In version 1.5.x, performance with a single connection has been significantly improved, likely removing the need to make multiple connections a single device. 

  Users are unable to explicitly configure simultaneous requests in version 1.5.x; however, if this functionality is still needed, users may configure multiple adapter components with the same device configuration. Alternatively, it is possible to configure multiple devices with different hostnames that all resolve to the same physical modbus device. 
