# networkwalks-B082-week1-CyberSecurity-lab-setup
lab setup( for cybersecurity and ethical hacking practice )
<div align="center">

# 🛡️ Cybersecurity Lab

### Week 01 — Virtual Penetration Testing Environment

<p>
  <img src="https://img.shields.io/badge/Kali%20Linux-2026.2-557C94?style=for-the-badge&logo=kalilinux&logoColor=white">
  <img src="https://img.shields.io/badge/VirtualBox-7.x-183A61?style=for-the-badge&logo=virtualbox&logoColor=white">
  <img src="https://img.shields.io/badge/Network-10.0.0.0%2F24-00A67E?style=for-the-badge">
  <img src="https://img.shields.io/badge/Status-Completed-2EA44F?style=for-the-badge">
</p>

<p>
  A controlled virtual environment built for hands-on<br>
  cybersecurity, network security and penetration-testing practice.
</p>

</div>

---

## 🧭 Week 01

This week focused on building the base environment required for the
remaining cybersecurity exercises.

Instead of testing against real systems, the lab uses isolated virtual
machines so that experiments can be performed safely and reset whenever
required.

### Lab Setup

```text
                         HOST MACHINE
                              │
                              ▼
                    ┌──────────────────┐
                    │    VirtualBox    │
                    └────────┬─────────┘
                             │
                     ┌───────▼───────┐
                     │  NAT NETWORK  │
                     │  10.0.0.0/24  │
                     └───────┬───────┘
                             │
                ┌────────────┴────────────┐
                │                         │
         ┌──────▼──────┐           ┌──────▼──────┐
         │ KALI LINUX  │           │   WINDOWS   │
         │   ATTACKER  │           │    VICTIM   │
         │ 10.0.0.10   │           │ 10.0.0.20   │
         └─────────────┘           └─────────────┘
                │                         │
                └───────────┬─────────────┘
                            │
                     Controlled Traffic
```

---

## ⚙️ Environment

| Component | Configuration |
|:--|:--|
| Hypervisor | Oracle VirtualBox |
| Attacker | Kali Linux |
| Victim | Windows 10/11 |
| Network | VirtualBox NAT Network |
| Subnet | `10.0.0.0/24` |
| Kali | `10.0.0.10` |
| Windows | `10.0.0.20` |
| Gateway | `10.0.0.1` |

---

## 🔧 What Was Set Up

```text
01  ──  VirtualBox
02  ──  Kali Linux VM
03  ──  Windows Victim VM
04  ──  Isolated NAT Network
05  ──  Static IP Configuration
06  ──  Kali ↔ Windows Connectivity
07  ──  VM Snapshots
```

Everything required for the Week 01 environment has been configured and
verified.

---

## 🌐 Network

The lab uses a dedicated private subnet:

```text
Network      : 10.0.0.0/24
Gateway      : 10.0.0.1

Kali Linux   : 10.0.0.10
Windows      : 10.0.0.20
```

Connectivity between the attacker and victim environments was verified
before moving forward.

```bash
# From Kali

ping 10.0.0.20
```

Expected result:

```text
64 bytes from 10.0.0.20: icmp_seq=1 ttl=128 time=...
64 bytes from 10.0.0.20: icmp_seq=2 ttl=128 time=...
64 bytes from 10.0.0.20: icmp_seq=3 ttl=128 time=...
```

---

## 📸 Lab Evidence

The Week 01 setup includes evidence for:

- VirtualBox configuration
- Kali Linux installation/import
- Windows victim configuration
- NAT Network configuration
- IP addressing
- Kali → Windows connectivity
- VM snapshots

> Screenshots and command outputs are maintained alongside the project
> documentation.

---

## 🔐 Isolation

The environment is intentionally separated from the host system.

```text
              INTERNET
                  │
                  │
                  X
                  │
        ┌─────────▼─────────┐
        │   VIRTUAL LAB     │
        │                   │
        │  10.0.0.0/24      │
        │                   │
        │  Kali ↔ Windows   │
        └───────────────────┘
```

All security testing is performed only against machines created for this
lab.

---

## 📦 Recovery

Snapshots were created after completing the base configuration.

This allows the environment to be restored to a known-good state before
performing destructive or experimental security tests.

```text
Clean State
     │
     ▼
 Snapshot
     │
     ▼
Security Testing
     │
     ├── Successful → Continue
     │
     └── Broken Environment
              │
              ▼
          Restore Snapshot
```

---

## ✅ Week 01 Checklist

<div align="center">

| Setup | Status |
|:--|:--:|
| VirtualBox | ✅ |
| Kali Linux VM | ✅ |
| Windows Victim VM | ✅ |
| NAT Network | ✅ |
| `10.0.0.0/24` Subnet | ✅ |
| IP Configuration | ✅ |
| Kali ↔ Windows Connectivity | ✅ |
| VM Snapshots | ✅ |
| Isolated Lab | ✅ |

### **WEEK 01 — COMPLETE**

</div>

---

## 🛠️ Tools

<p>
  <img src="https://img.shields.io/badge/Kali%20Linux-557C94?style=flat-square&logo=kalilinux&logoColor=white">
  <img src="https://img.shields.io/badge/Oracle%20VirtualBox-183A61?style=flat-square&logo=virtualbox&logoColor=white">
  <img src="https://img.shields.io/badge/Windows-0078D4?style=flat-square&logo=windows&logoColor=white">
  <img src="https://img.shields.io/badge/Networking-0A66C2?style=flat-square&logo=cisco&logoColor=white">
</p>

---

<div align="center">

### 🛡️ Cybersecurity Lab

`Learn → Configure → Test → Document → Reset`

**Week 01 completed successfully.**

</div>
