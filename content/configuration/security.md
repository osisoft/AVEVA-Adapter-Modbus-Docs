---
uid: PIAdapterForModbusSecurity
---

# Security 

When determining Modbus TCP security practices with regards to REST APIs, you should consider the following practice. To keep the adapter secure, it should only be installed on machines that restrict access to administrators only. REST APIs are bound to localhost, meaning that only requests coming from within the machine will be accepted. 

## Modbus protocol

The Modbus TCP adapter does not currently support transport layer security between the adapter and the data source. This means that Modbus traffic will be unprotected. If you wish to protect this traffic, other measures, such as a VPN connection, air-gapped control network, or SSH tunnel, must be taken. 