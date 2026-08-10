# networkwalks-B082-week1-CyberSecurity-lab-setup
lab setup( for cybersecurity and ethical hacking practice )
# 🔐 Cybersecurity & Ethical Hacking — Practical Lab

<p align="center">

![Kali Linux](https://img.shields.io/badge/Kali%20Linux-2026.2-557C94?style=for-the-badge&logo=kalilinux&logoColor=white)

![VirtualBox](https://img.shields.io/badge/Oracle%20VirtualBox-Lab-183A61?style=for-the-badge&logo=virtualbox&logoColor=white)

![Networking](https://img.shields.io/badge/Networking-10.0.0.0%2F24-blue?style=for-the-badge)

![Status](https://img.shields.io/badge/Week%201-Completed-success?style=for-the-badge)

</p>

<p align="center">
  <b>A hands-on cybersecurity laboratory built for learning networking, penetration testing and ethical hacking in a controlled virtual environment.</b>
</p>

---

## 📌 Table of Contents

- [🎯 Objective](#-objective)
- [🛡️ Why an Isolated Lab](#️-why-an-isolated-lab)
- [🏗️ Lab Architecture](#️-lab-architecture)
- [💻 Environment](#-environment)
- [🌐 Network Configuration](#-network-configuration)
- [⚙️ Week 1 Setup](#️-week-1-setup)
- [🧪 Verification & Testing](#-verification--testing)
- [📸 Screenshots](#-screenshots)
- [⚠️ Problems & Solutions](#️-problems--solutions)
- [💾 Snapshot & Recovery Strategy](#-snapshot--recovery-strategy)
- [🧠 What I Learned](#-what-i-learned)
- [🧰 Tools Used](#-tools-used)
- [🚀 Next Steps](#-next-steps)
- [👨‍💻 Author](#-author)
- [⚠️ Disclaimer](#️-disclaimer)

---

# 🎯 Objective

The objective of this project is to build a controlled cybersecurity laboratory for practicing:

- 🔐 Cybersecurity fundamentals
- 🌐 Computer networking
- 🐉 Kali Linux
- 🧪 Penetration testing
- 🔎 Network reconnaissance
- 🛡️ Ethical hacking

The lab is designed using virtual machines so that security experiments can be performed safely without affecting real-world systems or networks.

---

# 🛡️ Why an Isolated Lab?

Cybersecurity experiments may involve activities such as network scanning, service enumeration and security testing.

Performing these activities on systems without authorization can cause:

- Unwanted network traffic
- Service disruption
- Security alerts
- Accidental damage
- Legal and ethical issues

Therefore, this project uses an **isolated virtual laboratory** where the machines are intentionally created for security testing.

This provides a safe environment for learning and experimentation.

> ⚠️ All testing in this project is intended only for systems that I own or have explicit permission to test.

---

# 🏗️ Lab Architecture

The planned laboratory consists of an attacker machine and controlled victim environments.

```text
                         HOST MACHINE
                         Windows PC
                              │
                              ▼
                    ┌──────────────────┐
                    │    VirtualBox    │
                    │  Virtualization  │
                    └────────┬─────────┘
                             │
                             ▼
                    ┌──────────────────┐
                    │    CyberLab      │
                    │  NAT Network     │
                    │  10.0.0.0/24     │
                    └────────┬─────────┘
                             │
              ┌──────────────┼──────────────┐
              │              │              │
              ▼              ▼              ▼
        ┌──────────┐   ┌──────────┐   ┌──────────┐
        │   Kali   │   │ Windows  │   │ Android  │
        │ Attacker │   │  Victim  │   │  Victim  │
        └──────────┘   └──────────┘   └──────────┘
        10.0.0.2/24       Planned         Planned

---

# 💻 Environment

## 🖥️ Host Machine

| Component | Details |
|:--|:--|
| Operating System | Windows |
| Virtualization Platform | Oracle VirtualBox |
| Lab Type | Isolated Virtual Cybersecurity Lab |

---

## 🐉 Kali Linux — Attacker Machine

| Component | Details |
|:--|:--|
| Operating System | Kali Linux 2026.2 |
| Architecture | AMD64 |
| Virtualization | Oracle VirtualBox |
| Role | Attacker Machine |
| IP Address | `10.0.0.2/24` |

---

# 🌐 Network Configuration

The cybersecurity laboratory uses a dedicated **VirtualBox NAT Network** to provide controlled communication between the virtual machines.

## 🔵 CyberLab Network

```text
┌──────────────────────────────────────┐
│              CyberLab                │
├──────────────────────────────────────┤
│ Network      : 10.0.0.0/24           │
│ Subnet Mask  : 255.255.255.0         │
│ DHCP         : Disabled              │
│ Kali IP      : 10.0.0.2              │
└──────────────────────────────────────┘
---

# 🔗 Resources & References

### 🐉 Kali Linux

Official Kali Linux documentation and downloads were used for the virtual machine setup.

🔗 [Kali Linux — Official Website](https://www.kali.org/)

---

### 📦 Oracle VirtualBox

VirtualBox was used as the virtualization platform for creating and managing the cybersecurity lab.

🔗 [Oracle VirtualBox — Official Website](https://www.virtualbox.org/)

---

### 🗜️ 7-Zip

7-Zip was used to extract the downloaded Kali Linux VirtualBox image.

🔗 [7-Zip — Official Website](https://www.7-zip.org/)

---

### 🎓 Training & Lab Instructions

This laboratory was developed as part of the practical cybersecurity training and instructor-provided Week 1 lab instructions.

**Training:** NetworkWalks Academy

---

> 📚 **Note:**  
> All tools and resources were used for educational and authorized cybersecurity laboratory practice.
