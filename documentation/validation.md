# Lab 02 — Validation and Testing

## Purpose

This document records the validation checks performed on the Windows 11 domain client in the CausTech Technologies lab.

## Environment

* **Client:** `CLIENT01`
* **Domain Controller:** `DC01`
* **Domain:** `caustech.local`
* **Domain Controller IP:** `192.168.10.10`
* **Virtual Network:** `CausTech-LAN`

## Validation Checklist

| Test                           | Expected Result                                | Status |
| ------------------------------ | ---------------------------------------------- | ------ |
| Static IP configuration        | Client uses the configured static IPv4 address | Passed |
| DNS configuration              | DNS points to `192.168.10.10`                  | Passed |
| Domain membership              | Client is joined to `caustech.local`           | Passed |
| Domain user sign-in            | Domain account signs in successfully           | Passed |
| User verification              | `whoami` displays the expected domain user     | Passed |
| Domain controller connectivity | Ping to `192.168.10.10` succeeds               | Passed |

## Results

All listed validation checks completed successfully. The Windows 11 client was configured, joined to the CausTech Active Directory domain, and verified for domain-user sign-in and connectivity to the domain controller.

## Conclusion

The Windows 11 domain client was successfully integrated into the CausTech Technologies lab environment. DHCP configuration and testing will be documented separately in Lab 03.
