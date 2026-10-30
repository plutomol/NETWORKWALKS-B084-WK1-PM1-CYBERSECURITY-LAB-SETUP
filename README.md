##  Project Overview

This **`project`** involves establishing a virtual cybersecurity and penetration-testing laboratory using VirtualBox and Kali Linux.

The **`primary objective`** is to build a secure and controlled virtual environment for conducting cybersecurity experiments, including network scanning, reconnaissance, vulnerability assessment, and various penetration-testing activities.

The laboratory is configured using a private virtual network, allowing additional virtual machines to be integrated in the future. These machines will serve as target systems for conducting authorized security testing, practical exercises, and hands-on cybersecurity experiments.

**⚠️ Important:** This lab is used for systems that have explicit permission to test. This lab or its tools are not used to attack unauthorized systems.

##  Lab Architecture
<img width="1365" height="767" alt="image" src="https://github.com/user-attachments/assets/f0a138aa-f4f5-4be5-bd3c-ffc703712e23" />



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

<img width="1365" height="767" alt="image" src="https://github.com/user-attachments/assets/d62087e6-b92f-4f48-b080-6aae982b00c2" />


### Step 5. Configure the Kali Linux Network
The Kali Linux network configuration was checked and configured with a consistent IPv4 address.


**Used configuration:**

| **Configuration** | **Value** |
|:---|:---|
| IP Address | `10.0.0.2` |
| Subnet Mask | `255.255.255.0` (`/24`) |
| Gateway | `10.0.0.1` |
| DNS | `8.8.8.8` |

A consistent IP address makes it easier to document the lab and reference the Kali machine in future exercises.


**Internet was working:**

Google was opened to test internet connection !

<img width="1276" height="739" alt="image" src="https://github.com/user-attachments/assets/9ac6fa57-7f9b-42a8-99dd-ec5ff65231a2" />


## Step 6: Create a Clean VM Snapshot

After completing the initial configuration, a VirtualBox snapshot was created.

**Used Snapshot Name:**
`Clean Kali Linux in initial state - with Network Setup`

This snapshot represents the clean baseline of the laboratory environment.

If a future exercise changes or damages the VM configuration, the virtual machine can be restored to this baseline, allowing the laboratory environment to return to its original state.


## Lab Verification

| Status | Test | Command | Expected Result |
|:---:|---|---|---|
| ✅ | Check IP Address | `ip a` | Correct Kali IP displayed |
| 📡 | Test Gateway | `ping 10.0.0.1` | Successful replies |
| 🌍 | Test Internet Connectivity | `ping 8.8.8.8` | Successful replies |


## Problems Encountered & Solutions

**Following problem is encountered:**

### Problem 1: Difficulty Locating the Extracted Kali Linux File

While extracting the Kali Linux `.7z` archive, the extraction destination was not clearly noted. As a result, it became difficult to locate the extracted virtual machine files.

**Solution:**

- Always check and note the extraction destination before starting the extraction process.
- Extract the Kali Linux archive to a clearly identifiable folder.
- Use a dedicated directory for virtual machines to keep files organized.

**Example Directory:**

```
VirtualBox/
└── Kali-Linux/
    ├── Kali-Linux.vbox
    └── Kali-Linux.vdi
```
    


## 💡 What I Learned

Through this project, I learned how to create and configure a virtual environment for cybersecurity practice.

The most important concepts I learned include:

### 1. NAT Network

A standard NAT configuration and a NAT Network serve different purposes.

A NAT Network allows multiple VMs connected to the same virtual network to communicate with one another while providing Network Address Translation (NAT) for external connectivity.

This makes it useful for building a multi-machine cybersecurity laboratory.

### 2. Virtual Machine Networking

I learned how VirtualBox virtual network adapters connect virtual machines to different types of networks and how network configuration affects communication between machines.

### 3. Static IP Configuration

I learned how to configure and verify IPv4 addressing, subnet masks, gateways, and DNS settings in Kali Linux.

### 4. VM Snapshots

I learned that a clean snapshot should be created before performing risky or experimental activities.

This provides a known-good recovery point for future cybersecurity exercises.

### 5. Documentation

I learned that documenting commands, configurations, screenshots, problems, and solutions is an important part of a professional cybersecurity project.


##  Tools & Resources

The following tools and resources were used during this project:

| Tool / Resource | Purpose | Download Link |
|:---|:---|:---|
| 7-Zip | Extracting the Kali Linux `.7z` archive | [Download 7-Zip](https://7-zip.org/download.html) |
| Oracle VirtualBox | Creating and managing virtual machines | [Download VirtualBox](https://virtualbox.org/wiki/Downloads) |
| Kali Linux | Linux distribution for cybersecurity practice | [Download Kali Linux](https://kali.org/get-kali) |



# 🙏 Acknowledgments

- **Mentor:** [Waqas Karim] – For technical guidance and support.
- **Platform:** [Networkwalks] – For guidance and encouragement.
- **Special Thanks:** To everyone who supported me throughout this learning journey.
