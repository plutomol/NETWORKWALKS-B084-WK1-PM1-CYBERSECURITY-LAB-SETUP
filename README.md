##  Project Overview

This **`project`** involves establishing a virtual cybersecurity and penetration-testing laboratory using VirtualBox and Kali Linux.

The **`primary objective`** is to build a secure and controlled virtual environment for conducting cybersecurity experiments, including network scanning, reconnaissance, vulnerability assessment, and various penetration-testing activities.

The laboratory is configured using a private virtual network, allowing additional virtual machines to be integrated in the future. These machines will serve as target systems for conducting authorized security testing, practical exercises, and hands-on cybersecurity experiments.

**⚠️ Important:** This lab is used for systems that have explicit permission to test. This lab or its tools are not used to attack unauthorized systems.

##  Lab Configuration

| ** Component** | ** Configuration** |
|:---|:---|
|  Host OS | Windows 11 Home |
|  Host RAM | 8 GB |
|  Processor | Intel Celeron |
|  Hypervisor | VirtualBox 7.2 |
|  Security OS | Kali Linux 2026.2 |
|  Kali RAM | 2048 MB |
|  Virtual Network | NAT Network |
|  Network Address | `10.0.0.0/24` |
|  Kali IP Address | `10.0.0.2/24` |
|  Default Gateway | `10.0.0.1` |
|  DNS Server | `8.8.8.8` |
|  Future VM Range | `10.0.0.3–10.0.0.99` |

##  Lab Setup Procedure

### Step 1: Install 7-Zip
7-Zip was installed to extract the Kali Linux virtual machine package, which may be distributed in `.7z` archive format.

- **Tool:** 7-Zip

### Step 2: Install VirtualBox
VirtualBox was installed as the hypervisor to create and manage virtual machines.

- **Tool:** Oracle VirtualBox

### Step 3: Create the NAT Network
A private NAT Network was created in VirtualBox to allow virtual machines to communicate with each other while maintaining network isolation from the host environment.

