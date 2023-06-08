---
uid: SystemRequirements
---

# System requirements

[!include[product](../_includes/inline/product-name.md)] is supported on a variety of platforms and processors. Install kits are available for the following platforms:

| Operating System | Platform | Installation Kit | Processor(s) |
|-------------------|-------------|----------------------------------|-------------|
| Windows 10 Enterprise <br>Windows 10 IoT Enterprise | x64 | <code>[!include[installer](../_includes/inline/installer-name.md)]-x64_.msi</code>     | Intel/AMD 64-bit processors |
| Debian 10, 11<br>Ubuntu 20.04, 22.04 | x64 | <code>[!include[installer](../_includes/inline/installer-name.md)]-x64_.deb</code>     | Intel/AMD 64-bit processors |
| Debian 10, 11<br>Ubuntu 22.04 | ARM32 | <code>[!include[installer](../_includes/inline/installer-name.md)]-arm_.deb</code>  | ARM 32-bit processors |
| Debian 10<br>Ubuntu 22.04 | ARM64 | <code>[!include[installer](../_includes/inline/installer-name.md)]-arm64_.deb</code>  | ARM 64-bit processors |

Alternatively, you can use tar.gz files with binaries to build your own custom installers or containers for Linux. For more information on installing the adapter with Docker containers, see <xref:InstallUsingDocker>.

## Visual C++ 2022 Redistributables
 
It is recommended that you install [VC143 redistributables](https://learn.microsoft.com/en-us/cpp/windows/latest-supported-vc-redist) prior to [!include[product](../_includes/inline/product-name.md)] installation. 
 
[!include[product](../_includes/inline/product-name.md)] installer includes these as part of a merge module. However, they do not receive automatic updates from Microsoft unless installed manually. 

## PI Web API compatibility

This version of [!include[product](../_includes/inline/product-name.md)] is compatible with PI Web API 2021 and later.
