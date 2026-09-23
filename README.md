# Aashif-B083-WK1-CYBERSECURITY-LAB-SETUP
### VMware Workstation & Kali Linux

![VMware](https://img.shields.io/badge/VMware-Workstation-blue)
![Kali Linux](https://img.shields.io/badge/Kali-Linux-557C94?logo=kalilinux&logoColor=white)
![Networking](https://img.shields.io/badge/Networking-Static%20IPv4-informational)
![Status](https://img.shields.io/badge/Status-%20done-orange)

## 📌 Project Overview

This project documents my Week 1 cybersecurity laboratory setup using **VMware Workstation** and **Kali Linux**.

The goal was to configure the Kali Linux virtual machine with a manual IPv4 address and verify the network interface configuration from the Linux terminal. The screenshots in this repository are captured from my own Kali Linux environment.

## 🎯 Objectives

- Set up a Kali Linux virtual machine in VMware Workstation
- Access the network configuration settings
- Configure a manual IPv4 address
- Configure the default gateway
- Verify the assigned IP address from the terminal
- Check the network interface state using Linux commands
- Document the configuration with screenshots

## 🛠️ Tools & Technologies

| Component | Technology |
|---|---|
| Hypervisor | VMware Workstation |
| Operating System | Kali Linux 2026.2 |
| Network Interface | `eth0` |
| IPv4 Address | `10.0.0.2/24` |
| Gateway | `10.0.0.1` |
| Configuration | Manual / Static IPv4 |

## 🌐 Network Configuration

The following manual IPv4 configuration was applied to the Kali Linux VM:

| Parameter | Value |
|---|---|
| IPv4 Address | `10.0.0.2` |
| Prefix / Netmask | `/24` |
| Netmask | `255.255.255.0` |
| Gateway | `10.0.0.1` |
| Interface | `eth0` |
| DHCP | Manual configuration |

## 🔧 Configuration Steps

### 1. Open Network Configuration

I accessed the network configuration tools in Kali Linux to modify the wired connection settings.

![Network Configuration](Screenshots/01_Network_Configuration_Access.png)<img width="960" height="540" alt="01_Network_Configuration_Access" src="https://github.com/user-attachments/assets/1d516847-4ccf-4799-8482-fcb37a0cc8c9" />


### 2. Configure Static IPv4

The wired connection was configured with the following values:

- **Method:** Manual
- **Address:** `10.0.0.2`
- **Netmask:** `/24`
- **Gateway:** `10.0.0.1`

![Static IP Configuration](Screenshots/02_Static_IP_Configuration.png)<img width="960" height="540" alt="02_Static_IP_Configuration" src="https://github.com/user-attachments/assets/21b61e26-8de0-4da1-8dfc-f4f92d3831ac" />


### 3. Verify the IP Address

The `ip a` command was used to inspect the network interfaces and verify the configured IPv4 address.

```bash
ip a
```

The `eth0` interface showed:

```text
inet 10.0.0.2/24
```

![IP Address Verification](Screenshots/03_IP_Address_Verification.png)<img width="960" height="540" alt="03_IP_Address_Verification" src="https://github.com/user-attachments/assets/74fa2ec7-6ee5-4e6c-8c41-3557a1aff2d9" />


### 4. Verify Interface State

The interface configuration was also checked from the terminal. The following command was used during the setup to bring the interface down for verification:

```bash
sudo ifconfig eth0 down
```

The interface state was then checked with:

```bash
ip a
```

![Interface Status Verification](Screenshots/04_Interface_Status_Verification.png)<img width="960" height="540" alt="04_Interface_Status_Verification" src="https://github.com/user-attachments/assets/53dab9ce-e5f2-4666-9a88-290048560bb2" />


## 💻 Useful Commands

### View IP configuration

```bash
ip a
```

### View routing table

```bash
ip route
```

### View interface status

```bash
ip link show eth0
```

### Bring the interface up

```bash
sudo ip link set eth0 up
```

### Bring the interface down

```bash
sudo ifconfig eth0 down
```

> **Note:** Only use network configuration and security-testing commands in systems and lab environments that you own or have explicit permission to use.

## 📂 Project Structure

```text
NETWORKWALKS-B083-WK1-PM1-CYBERSECURITY-LAB-SETUP/
│
├── README.md
│
└── Screenshots/
    ├── 01_Network_Configuration_Access.png
    ├── 02_Static_IP_Configuration.png
    ├── 03_IP_Address_Verification.png
    └── 04_Interface_Status_Verification.png
```

## 🔍 Skills Practiced

- Kali Linux
- Linux networking
- IPv4 configuration
- Static IP addressing
- Network interface management
- Linux terminal commands
- Virtual machine networking
- Basic cybersecurity lab setup

## 👤 Author

**Aashif Rahman**

Cybersecurity | VAPT | SOC | Linux | Networking

## Disclaimer

This repository is created for **educational and cybersecurity lab purposes**. All security testing should be performed only on systems, networks, and virtual environments that you own or have explicit authorization to test.

---

### 🛡️ Learn. Practice. Secure.
