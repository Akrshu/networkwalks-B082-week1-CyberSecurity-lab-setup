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
