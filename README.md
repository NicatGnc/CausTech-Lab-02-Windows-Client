# Lab 02 — Windows 11 Domain Client

## 1. Overview

This lab documents the creation and configuration of a Windows 11 client workstation for the CausTech Technologies Active Directory environment.

The objective was to install Windows 11 in Oracle VirtualBox, configure the network settings, join the existing Active Directory domain, and verify connectivity to the domain controller.

## 2. Virtual Machine Configuration

A new virtual machine was created in Oracle VirtualBox for the Windows 11 client.

**Key tasks:**

* Selected the Windows 11 installation ISO.
* Allocated RAM and CPU resources.
* Configured virtual disk storage.

![Windows 11 Virtual Machine Configuration](screenshots/01.png)
![Windows 11 Virtual Machine Configuration2](screenshots/02.png)
![Windows 11 Virtual Machine Configuration3](screenshots/03.png)

## 3. Windows 11 Installation

The Windows 11 installation process was started after configuring the virtual machine.

The setup included selecting the installation language and regional format, choosing the installation option, and selecting the Windows image to install.

**Key tasks:**

* Selected language and regional preferences.
* Chose the Windows installation option.
* Selected the Windows image edition.
* Started the Windows 11 installation.

![Windows 11 Installation](screenshots/05.png)
![Windows 11 Installation](screenshots/07.png)
![Windows 11 Installation](screenshots/09.png)
![Windows 11 Installation](screenshots/11.png)

## 4. Initial Windows 11 Setup

During the initial setup, Windows 11 requested regional information before continuing with the configuration.

The workstation was prepared for use in the CausTech lab environment.

**Key tasks:**

* Completed the region selection.
* Continued through the initial Windows setup.

![Windows 11 Initial Setup](screenshots/12.png)

## 5. Client Network Configuration

The Windows 11 workstation was configured with a static IPv4 address and DNS settings to communicate with the existing domain controller.

**Key tasks:**

* Configured the client's static IP address.
* Set the appropriate subnet mask.
* Configured DNS to use the domain controller.
* Prepared the workstation for domain joining.

**Domain controller:** `DC01`
**Domain:** `caustech.local`
**DNS server:** `192.168.10.10`

![Windows 11 Static IP and DNS Configuration](screenshots/16.png)

## 6. Joining the Active Directory Domain

After configuring the network settings, the Windows 11 workstation was joined to the existing `caustech.local` domain.

The process required domain credentials and a restart to complete the configuration.

**Key tasks:**

* Connected the workstation to `caustech.local`.
* Submitted the required domain credentials.
* Confirmed the restart request after joining the domain.
* Restarted the workstation to apply the changes.

![Joining the Active Directory Domain](screenshots/18.png)
![Joining the Active Directory Domain2](screenshots/20.png)

## 7. Domain and Connectivity Verification

After restarting, PowerShell or Command Prompt was used to verify the logged-in account and test connectivity to the domain controller.

The `whoami` command identifies the current user context. The `ping` command checks IP connectivity to the specified destination.

**Commands used:**

```cmd
whoami
ping 192.168.10.10
```

**Key tasks:**

* Verified the signed-in account using `whoami`.
* Tested connectivity to DC01 using `ping`.
* Reviewed the results of the verification commands.

![Domain Sign-In and Connectivity Verification](screenshots/21.png)
![Domain Sign-In and Connectivity Verification2](screenshots/22.png)

## 8. Results and Project Notes

This lab documents the preparation of a Windows 11 workstation and its integration into the CausTech Technologies Active Directory environment.

**Work covered:**

* Created a Windows 11 virtual machine.
* Installed Windows 11.
* Configured a static IP address and DNS.
* Joined the workstation to `caustech.local`.
* Verified the user context and tested connectivity to the domain controller.

DHCP configuration and testing are reserved for **Lab 03**.

This is a personal home lab created for hands-on learning and IT portfolio development. CausTech Technologies is a fictional company.

**Related project:** 
[Lab 01 — Windows Server & Active Directory](https://github.com/NicatGnc/CausTech-Lab-01-Active-Directory) 
[Lab 03 — DHCP Server](https://github.com/NicatGnc/CausTech-Lab-03-DHCP-Server)
