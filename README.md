# networkwalks-B082-week1-CyberSecurity-lab-setup
lab setup( for cybersecurity and ethical hacking practice )
<div align="center">

# 🛡️ Cybersecurity & Penetration Testing Lab

### 🔬 Hands-On Ethical Hacking & Network Security Environment

<p>
  <img src="https://img.shields.io/badge/Week%201-Completed-00C853?style=for-the-badge&logo=kalilinux&logoColor=white">
  <img src="https://img.shields.io/badge/Kali%20Linux-2026.2-557C94?style=for-the-badge&logo=kalilinux&logoColor=white">
  <img src="https://img.shields.io/badge/VirtualBox-Lab-183A61?style=for-the-badge&logo=virtualbox&logoColor=white">
  <img src="https://img.shields.io/badge/Network-10.0.0.0%2F24-FF6F00?style=for-the-badge&logo=cisco&logoColor=white">
</p>

<p>
  <b>⚠️ Authorized Security Testing Environment</b>
</p>

<p>
  A controlled virtual laboratory designed for learning<br>
  penetration testing, network security, vulnerability assessment,
  and ethical hacking.
</p>

</div>

---

## 🎯 Week 01 — Lab Foundation

> **Objective:** Build an isolated and reproducible cybersecurity environment
> containing an attacker machine, victim machine, and dedicated virtual network.

---

## 🏗️ Lab Architecture

```text
                         💻 HOST MACHINE
                               │
                               │
                     ┌─────────▼─────────┐
                     │   ORACLE VIRTUALBOX │
                     └─────────┬─────────┘
                               │
                     ┌─────────▼─────────┐
                     │    NAT NETWORK     │
                     │    10.0.0.0/24     │
                     └─────────┬─────────┘
                               │
                ┌──────────────┴──────────────┐
                │                             │
       ┌────────▼────────┐           ┌────────▼────────┐
       │   🐉 KALI LINUX │           │   🪟 WINDOWS    │
       │    ATTACKER     │           │     VICTIM     │
       │                 │           │                 │
       │   10.0.0.10     │           │   10.0.0.20     │
       └─────────────────┘           └─────────────────┘
                │                             │
                └─────────── 🔐 ─────────────┘
                     Controlled Testing


## 📋 Week 01 Progress

<div align="center">

| Task | Status |
|:---|:---:|
| ⚙️ Install Oracle VirtualBox | ✅ Completed |
| 📦 Download Kali Linux Virtual Machine | ✅ Completed |
| 🗜️ Extract Kali VirtualBox Image | ✅ Completed |
| 🐉 Import Kali Linux VM | ✅ Completed |
| 🌐 Create NAT Network | ✅ Completed |
| 🔧 Configure Kali Network | ✅ Completed |
| 🪟 Setup Windows Victim VM | ✅ Completed |
| 🔗 Verify Kali ↔ Windows Connectivity | ✅ Completed |
| 📸 Create VM Snapshots | ✅ Completed |
| 🧪 Verify Isolated Lab Environment | ✅ Completed |

</div>

---
