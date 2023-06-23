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

## Visual C++ Redistributable
For Windows installations, the Microsoft Visual C++ Redistributable for Visual Studio 2015, 2017, 2019, and 2022 is required and installed by the [!include[product](../_includes/inline/product-name.md)] installation kit.
 
It is recommended that you manually install the [latest supported Microsoft Visual C++ Redistributable](https://learn.microsoft.com/en-us/cpp/windows/latest-supported-vc-redist) prior to [!include[product](../_includes/inline/product-name.md)] installation in order to receive automatic updates.

## PI Web API compatibility

This version of [!include[product](../_includes/inline/product-name.md)] is compatible with PI Web API 2021 and later.
