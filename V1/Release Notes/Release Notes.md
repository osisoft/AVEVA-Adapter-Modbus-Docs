---
uid: releaseNotes
---

# Release Notes

PI Adapter for Modbus TCP<br>
© 2020 OSIsoft, LLC. All rights reserved. <!--*This section may be removed if this note is part of a broader manual.*-->

## Overview

This represents the initial standalone release for PI Adapter for Modbus TCP. This product collects time series data and relevant metadata from Modbus TCP devices and sends it to configured OMF endpoints such as PI Web API and OSIsoft Cloud Services. PI Adapter for Modbus TCP can also collect health and diagnostics information. It supports buffering, polled data collection, and various Windows and Linux-based operating systems as well as containerization.

For more information see [PI Adapter for Modbus overview](xref:PIAdapterforModbusTCPoverview).

## Known Issues

There are no known issues at this time.

### Operating Systems and Distribution Kit Files

| Operating System | Installation Kit | Processor(s) |
|-------------------|----------------------------------|-------------|
| Windows 10 x64 (any version)| `Modbus_win10-x64.msi`     | Intel/AMD 64-bit processors |
| Debian 9 or later x64 | `Modbus_linux-x64.deb`     | Intel/AMD 64-bit processors |
| Debian 9 or later arm32 | `Modbus_linux-arm.deb`  | Arm 32-bit processors |
| Debian 9 or later arm64 | `Modbus_linux-arm64.deb`  | Arm 64-bit processors |

No additional executable files (.msi, .exe, etc.) are included within the setup. For more information, see [System Requirements](xref:SystemRequirements).

### Installation

Refer to the [Install the adapter](xref:InstallTheAdapter) instructions.

### Uninstallation

Refer to the [Uninstall the adapter](xref:UninstallTheAdapter) instructions.

## Security Information and Guidance

### OSIsoft’s Commitment

Because the PI System often serves as a barrier protecting control system networks and mission-critical infrastructure assets, OSIsoft is committed to (1) delivering a high-quality product and (2) communicating clearly what security issues have been addressed. This release of PI Adapter for Modbus TCP is the highest quality and most secure version of the PI Adapter for Modbus TCP released to date. OSIsoft's commitment to improving the PI System is ongoing, and each future version should raise the quality and security bar even further.

### Vulnerability Communication

The practice of publicly disclosing internally discovered vulnerabilities is consistent with the Common Industrial Control System Vulnerability Disclosure Framework developed by the Industrial Control Systems Joint Working Group (ICSJWG). Despite the increased risk posed by greater transparency, OSIsoft is sharing this information to help you make an informed decision about when to upgrade to ensure your PI System has the best available protection.

For more information, refer to [OSIsoft’s Ethical Disclosure Policy (https://www.osisoft.com/ethical-disclosure-policy)](https://www.osisoft.com/ethical-disclosure-policy).

To report a security vulnerability, refer to [OSIsoft's Report a Security Vulnerability (https://www.osisoft.com/report-a-security-vulnerability)](https://www.osisoft.com/report-a-security-vulnerability).

### Vulnerability Scoring

OSIsoft has selected the Common Vulnerability Scoring System (CVSS) to quantify the severity of security vulnerabilities for disclosure. To calculate the CVSS scores, OSIsoft uses the National Vulnerability Database (NVD) calculator maintained by the National Institute of Standards and Technology (NIST).  OSIsoft uses High, Medium and Low categories to aggregate the CVSS Base scores. This removes some of the opinion related errors of CVSS scoring.  As noted in the CVSS specification, Base score range from 0 for the lowest severity to 10 for the highest severity.

### Overview of New Vulnerabilities Found or Fixed

This section is intended to provide relevant security-related information to guide your installation or upgrade decision. OSIsoft is proactively disclosing aggregate information about the number and severity of PI Adapter for Modbus TCP security vulnerabilities that are fixed in this release.

No security-related information is applicable to this release.

## Technical Support and Resources

<!--*This section may be removed if the information is  captured within a separate topic in the same manual.*-->

For technical assistance, contact OSIsoft Technical Support at +1 510-297-5828 or log a case through the OSIsoft Customer Portal. Additionally, the Contact Us page on the portal offers contact options for customers outside of the United States.

When you contact OSIsoft Technical Support, be prepared to provide this information:

* Product name, version, and build numbers
* Computer platform (CPU type, operating system, and version number)
* Time that the difficulty started
* Log files at that time
* Details of any environment changes prior to the start of the issue
* Summary of the issue, including any relevant log files during the time the issue occurred

The PI Square community has resources to help you with your technical questions. PI Developers Club program offers specific services to developers and system integrators.
