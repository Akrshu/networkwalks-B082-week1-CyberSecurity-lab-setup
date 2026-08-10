# networkwalks-B082-week1-CyberSecurity-lab-setup
lab setup( for cybersecurity and ethical hacking practice )
# 🔐 Cybersecurity & Ethical Hacking — Practical Lab

<p align="center">

![Kali Linux](https://img.shields.io/badge/Kali%20Linux-2026.2-557C94?style=for-the-badge&logo=kalilinux&logoColor=white)
![VirtualBox](https://img.shields.io/badge/VirtualBox-Lab-183A61?style=for-the-badge&logo=virtualbox&logoColor=white)
![Network](https://img.shields.io/badge/Network-10.0.0.0%2F24-blue?style=for-the-badge)
![Status](https://img.shields.io/badge/Week%201-Completed-success?style=for-the-badge)

</p>

<p align="center">
  <b>Hands-on cybersecurity laboratory for networking, ethical hacking and penetration-testing practice in a controlled virtual environment.</b>
</p>

<p align="center">
  🎓 <b>NetworkWalks Academy</b> &nbsp; • &nbsp;
  📚 <b>Batch B082</b> &nbsp; • &nbsp;
  🗓️ <b>Week 01</b>
</p>

---

# 📌 Table of Contents

- 🎯 [Purpose of the Lab](#-purpose-of-the-lab)
- 🛡️ [Why an Isolated Network?](#️-why-an-isolated-network)
- 🏗️ [Lab Architecture](#️-lab-architecture)
- 💻 [Lab Environment](#-lab-environment)
- 🌐 [Network Configuration](#-network-configuration)
- ⚙️ [Step-by-Step Setup](#️-step-by-step-setup)
- 🧪 [Verification Tests](#-verification-tests)
- 📸 [Screenshots](#-screenshots)
- ⚠️ [Problems & Solutions](#️-problems--solutions)
- 💾 [Snapshot & Backup Strategy](#-snapshot--backup-strategy)
- 🧠 [What I Learned](#-what-i-learned)
- 🧰 [Tools & Resources](#-tools--resources)
- 🎥 [Project Demo](#-project-demo)
- 🚀 [Next Steps](#-next-steps)
- 👨‍💻 [Author](#-author)
- ⚠️ [Disclaimer](#️-disclaimer)

---

# 🎯 Purpose of the Lab

The goal of this project is to build a **controlled cybersecurity laboratory** for practicing:

- 🔐 Cybersecurity fundamentals
- 🌐 Networking
- 🐉 Kali Linux
- 🧪 Penetration Testing
- 🔎 Network Reconnaissance
- 🛡️ Ethical Hacking

The lab provides a safe environment where security experiments can be performed on intentionally configured virtual machines.

---

# 🛡️ Why an Isolated Network?

Cybersecurity testing can involve network scanning, service enumeration and other activities that generate network traffic.

Using an isolated virtual network helps:

- 🔒 Prevent accidental interaction with real systems
- 🧪 Provide a controlled environment for experiments
- 🌐 Allow communication between intentionally configured VMs
- 🔄 Make the environment easy to reset and reproduce

> ⚠️ All security testing in this project is performed only on systems that I own or have explicit authorization to test.

---

# 🏗️ Lab Architecture

```text
                         🖥️ HOST MACHINE
                             Windows
                                │
                                ▼
                       ┌────────────────┐
                       │   VirtualBox   │
                       └───────┬────────┘
                               │
                               ▼
                    ┌────────────────────┐
                    │      CyberLab      │
                    │   NAT Network      │
                    │   10.0.0.0/24      │
                    └─────────┬──────────┘
                              │
              ┌───────────────┼───────────────┐
              │               │               │
              ▼               ▼               ▼
        ┌──────────┐    ┌──────────┐    ┌──────────┐
        │ 🐉 Kali  │    │ 🪟 Windows│    │ 📱 Android│
        │ Attacker │    │  Victim  │    │  Victim  │
        └──────────┘    └──────────┘    └──────────┘
        10.0.0.2/24       Planned          Planned
💻 Lab Environment
🖥️ Host Machine
Component	Details
Operating System	Windows
Virtualization	Oracle VirtualBox
Lab Type	Isolated Virtual Cybersecurity Lab
CPU	[ADD YOUR CPU]
RAM	[ADD YOUR RAM]
Storage	[ADD YOUR STORAGE]
VirtualBox Version	[ADD VERSION]
🐉 Kali Linux
Component	Details
OS	Kali Linux 2026.2
Architecture	AMD64
Platform	Oracle VirtualBox
Role	Attacker Machine
IP Address	10.0.0.2/24
🌐 Network Configuration
🔵 CyberLab NAT Network
Setting	Value
Network Type	NAT Network
Network Name	CyberLab
IP Range	10.0.0.0/24
Subnet Mask	255.255.255.0
DHCP	Disabled
Kali IP	10.0.0.2/24
Why this network?

The 10.0.0.0/24 private network provides predictable addressing and controlled communication between the laboratory machines.

⚙️ Step-by-Step Setup
01 — 📦 VirtualBox Setup

Oracle VirtualBox was used as the virtualization platform.

Why?

To run isolated operating-system environments required for the cybersecurity laboratory.

Status: 🟢 Completed

02 — 🐉 Kali Linux Deployment

A pre-built Kali Linux VirtualBox image was downloaded and imported.

Why?

The pre-built image provides a ready-to-use Kali environment and avoids unnecessary manual installation steps.

Status: 🟢 Completed

03 — 🌐 Create CyberLab Network

A NAT Network named CyberLab was created in VirtualBox.

Network : 10.0.0.0/24
DHCP    : Disabled

Why?

To provide a controlled network for the cybersecurity lab machines.

Status: 🟢 Completed

04 — 📡 Configure Kali IP

Kali was configured with:

IP Address  : 10.0.0.2
CIDR        : /24
Subnet Mask : 255.255.255.0

The configuration was checked using:

ip addr

Status: 🟢 Completed

🧪 Verification Tests
🔎 Test 01 — ip addr
ip addr

Purpose: Verify the Kali network interface and assigned IP.

Expected:

10.0.0.2/24

🟢 Result: PASS

🌍 Test 02 — Internet Connectivity
ping google.com

Purpose: Verify that the Kali VM has working internet connectivity.

🟢 Result: PASS

🔗 Test 03 — Gateway Connectivity
ping <GATEWAY-IP>

Purpose: Verify connectivity between Kali and the configured virtual network gateway.

🟡 Status: To be documented when gateway testing is performed.

🖥️ Test 04 — VM-to-VM Connectivity

After the Windows victim VM is configured:

ping <WINDOWS-IP>

Purpose: Verify communication between the Kali attacker and Windows victim.

🟡 Status: Planned for the next phase.

📸 Screenshots

Screenshots are included as evidence of the actual lab configuration.

🌐 CyberLab Network

Evidence: CyberLab NAT Network configured with 10.0.0.0/24.

🐉 Kali IP Configuration

Evidence: Kali configured with 10.0.0.2/24.

🌍 Internet Connectivity

Evidence: Internet connectivity verified using ping.

💾 Week 1 Snapshot

Evidence: Clean Week 1 recovery snapshot created.

⚠️ Problems & Solutions
Problem	Solution
Kali installer setup was taking unnecessary steps	Used the pre-built Kali VirtualBox image
VMware vs VirtualBox confusion	Followed the lab requirement and used Oracle VirtualBox
Large Kali VM download	Downloaded the complete archive and extracted it using 7-Zip

💡 Key Learning: Using the correct virtualization platform and VM image simplified the overall lab setup.

💾 Snapshot & Backup Strategy

After completing the Week 1 configuration, a clean snapshot was created:

📸 Kali-Week1-Complete

The snapshot provides a known-good recovery point before future cybersecurity experiments.

🟢 Clean Kali Environment
          │
          ▼
📸 Kali-Week1-Complete
          │
          ▼
🧪 Future Experiments
          │
     ┌────┴────┐
     ▼         ▼
   Success   Failure
                │
                ▼
          🔄 Restore
            Snapshot
                │
                ▼
          🟢 Clean State

⚠️ Snapshots are useful for VM recovery but should not replace independent backups of important files.

🧠 What I Learned
🌐 Networking
IPv4 addressing
CIDR notation
/24 subnetting
Static IP configuration
NAT Networks
Connectivity testing
🐧 Linux
Network interface inspection
ip addr
ping
Basic network configuration
🖥️ Virtualization
Virtual machine management
VirtualBox networking
Pre-built VM deployment
VM snapshots
Recovery points
🔐 Cybersecurity
Importance of isolated labs
Attacker/Victim architecture
Controlled security testing
Safe experimentation
Lab documentation
🧰 Tools & Resources
Tool / Resource	Purpose
🐉 Kali Linux	Security testing environment
📦 Oracle VirtualBox	Virtualization
🗜️ 7-Zip	VM archive extraction
🐧 Linux Terminal	Network configuration
ip addr	Interface inspection
ping	Connectivity testing
🔧 Git	Version control
🐙 GitHub	Project documentation
🎓 NetworkWalks Academy	Cybersecurity training
🎥 Project Demo

A short video demonstration of the Week 1 laboratory setup will be added here.

🎬 Demo Includes
VirtualBox lab environment
CyberLab network configuration
Kali Linux setup
IP configuration
Connectivity verification
Snapshot creation

📌 Video: [ADD YOUR VIDEO LINK HERE]

🚀 Next Steps
🪟 Windows Victim Environment
 Deploy Windows 10/11 VM
 Connect Windows to CyberLab
 Configure Windows IP
 Test Kali ↔ Windows connectivity
🔎 Network Testing
 Network discovery
 Host identification
 Service enumeration
 Controlled penetration-testing exercises
📱 Additional Environment
 Prepare Android testing environment
 Connect Android to the lab
 Document configuration
💾 Recovery
 Create Windows baseline snapshot
 Maintain recovery points before major experiments
👨‍💻 Author
<div align="center">
[YOUR NAME]

🎓 Batch: B082

🔐 Cybersecurity • Ethical Hacking • Networking • Linux

</div>
⚠️ Disclaimer

🔐 Educational & Authorized Use Only

This repository is created strictly for educational cybersecurity practice.

All security testing must be performed only against systems that I own or have explicit permission to test.

The tools and techniques documented here must not be used for unauthorized access, exploitation, disruption or malicious activity.

<p align="center">
🔐 Learn • Build • Test • Document • Repeat 🚀

<b>Week 1 — Cybersecurity Practical Lab</b>

</p> ```
