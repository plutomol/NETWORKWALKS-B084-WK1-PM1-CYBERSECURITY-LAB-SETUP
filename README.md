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

<img width="955" height="586" alt="1-Screenshot-Vbox-NAT-Configuration" src="https://github.com/user-attachments/assets/da8503f3-31a8-4f3d-94b9-acead6c96561" />

A **NAT Network** was selected because multiple virtual machines connected to the same NAT Network can communicate with one another while also having outbound network connectivity.


This will allow future attacker and target VMs to communicate within the lab.

### Step 4: Import Kali Linux

The Kali Linux virtual machine was downloaded from the official Kali Linux website and imported into VirtualBox.

**Extracting kali .7zip file**

<img width="584" height="390" alt="2-Screenshot-Extract-Kali-7zip" src="https://github.com/user-attachments/assets/88224044-364b-44bd-a9bb-91e4af202890" />




The virtual machine's network adapter was configured with the following settings:

**Network Adapter Configuration:**

| **Component** | **Configuration** |
|:---|:---|
| Adapter | Adapter 1 |
| Attached to | NAT Network |
| Network Name | `NatNetwork` |
| Adapter Type | Intel PRO/1000 MT Desktop |

**Virtual Machine Resources:**

| **Component** | **Allocation** |
|:---|:---|
| RAM | 2048 MB |

