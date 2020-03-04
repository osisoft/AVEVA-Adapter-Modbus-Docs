---
uid: OSIsoftAdapterForModbusTCPSupportedFeatures
---

# OSIsoft Adapter for Modbus TCP supported features

For certain data types, the adapter supports applying bitmaps and applying data conversion.

## Bitmap application

The adapter supports applying bitmaps to the value converted from the readings from the Modbus TCP devices. A bitmap is a series of numbers used to extract and reorder bits from a word register. The format of the bitmap is uuvvwwxxyyzz, where uu, vv, ww, yy, and zz each refer to a single bit. A leading zero is required if the referenced bit is less than 10. The low-order bit is 01 and high-order bit is either 16 or 32. Up to 16 bits can be referenced for a 16-bit word (data types 10 and 20) and up to 32 bits can be referenced for a 32-bit word (data type 30 and 31). 

For example, the bitmap 0307120802 will map the second bit of the original word to the first bit of the new word, the eighth bit to the second bit, the twelfth bit to the third bit, and so on. The high-order bits of the new word are padded with zeros if they are not specified. 

Not all data types support applying bitmap. The data types supporting bitmap are: 
 - Int16 (Data type code 10) 
 - UInt16 (Data type code 20)
 - Int32 (Data type code 30 and 31) 
 
## Data conversion application 
 
The adapter supports applying data conversion to the value converted from reading the Modbus TCP devices. A conversion factor and conversion offset can be specified. The conversion factor is used for scaling the value up or down, and the conversion offset is used for shifting the value. The mathematical equation used in conversion is the following: 

 ```
 <After Conversion> = <Before Conversion> / Factor - Offset 
 ```

 Not all data types support applying data conversion. Data types that support data conversion are: 
 - Int16 (Data type code 10) 
 - UInt16 (Data type code 20) 
 - Int32 (Data type code 30 and 31) 
 - Float32 (Data type code 100 and 101) 

The value with data conversion applied will always be converted to the 32-bit float type to maintain the precision of the conversion factor and conversion offset.
