# 🦉 OUsbGuard

<p align="center">
  <img src="https://img.shields.io/badge/Platform-Linux-0a0c10?style=flat-square"/>
  <img src="https://img.shields.io/badge/Category-OCore-blue?style=flat-square"/>
  <img src="https://img.shields.io/badge/License-MIT-green?style=flat-square"/>
  <img src="https://img.shields.io/badge/Part%20of-OwlSec%20Toolkit-7b5ea7?style=flat-square"/>
  <img src="https://img.shields.io/badge/Version-1.0.0-cyan?style=flat-square"/>
</p>

> **OUsbGuard** — USBGuard Policy & USB Authorization Auditor

---

> ⚠️ **AUTHORISED USE ONLY** — Use only on systems you own or have explicit written permission to test. Unauthorised use is illegal.

---

## 📌 Overview

USBGuard policy & USB authorization auditor (BadUSB / HID / mass-storage / IPC / kernel)

---

## ✨ Features

- Full USBGuard rule-language parser — targets, device ids with wildcards, hash / parent-hash / serial / name / via-port / with-interface / with-connect-type / if / label, set operators (all-of, one-of, none-of, equals, equals-ordered, match-all) and conditions
- Daemon config audit — ImplicitPolicyTarget, Present- Device/Controller policy, InsertedDevicePolicy, AuthorizedDefault, AuditBackend, RuleFile / RuleFolder
- Rule analysis — broad / wildcard allows, HID without hash (BadUSB, ATT&CK T1200), mass storage, network / vendor-specific interfaces, duplicated & shadowed rules
- IPC — IPCAllowedUsers / Groups, IPCAccessControl.d privilege files (Devices / Policy / Parameters modify)
- Kernel — authorized_default, usbcore cmdline, usb-storage / uas / firewire / thunderbolt modprobe blacklists
- udev / udisks2 / dconf auto-mount & authorization bypass
- File-permission and ownership checks, offline --root
- Hashes & serials masked everywhere; CWE + MITRE ATT&CK
- Weighted 0–100 score with A+…F grade
- Hardened policy templates + rules.conf rewrite advisor
- Export TXT / Markdown / JSON / CSV / SARIF 2.1.0
- Self-test --demo, CI gates --fail-on / --min-severity

---

## ⚙️ Requirements

- **Linux**
- **No Python installation needed** — runs as a standalone executable

---

## 🚀 Usage

```bash
./OUsbGuard
```

---

## 📦 Part of OwlSec Toolkit

This tool is part of the **OwlSec** suite — a collection of 300+ security and privacy tools.

🔗 [owlsec.org](https://owlsec.org)

---

## ©️ License

MIT License — © Khaled S. Haddad

*Tools are distributed as pre-built executables. Source code is proprietary.*
