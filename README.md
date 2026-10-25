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


OUsbGuard is an offline, read-only USBGuard configuration auditor that parses rules.conf and usbguard-daemon.conf to evaluate USB device-authorization policy. It checks the default rule-set posture, implicit-policy target, present-device and insertion policies, allow-all rules and IPC access control. Findings are mapped to CWE and MITRE ATT&CK, scored and graded, and exported as TXT, Markdown, JSON, CSV or SARIF.

---

## ✨ Features


- Parsers for usbguard rules.conf and usbguard-daemon.conf (RuleFile, policy and IPC directives)
- Rule-set analysis: allow-all rules, broad allow by class/vendor, ordering and implicit-deny gaps
- ImplicitPolicyTarget, PresentDevicePolicy and InsertedDevicePolicy posture checks
- IPC access control (IPCAllowedUsers/Groups), AuthorizedDefault and device-manager hardening
- File-permission and ownership checks on rule and daemon configuration
- CWE+ATT&CK mapping, score/grade and TXT/MD/JSON/CSV/SARIF export with --fail-on gating

---

## ⚙️ Requirements

- **Linux**
- **No Python installation needed** — runs as a standalone executable

---

## 🚀 Usage


```bash
./OUsbGuard --scan -f sarif -o usbguard.sarif
./OUsbGuard --rules /etc/usbguard/rules.conf --daemon /etc/usbguard/usbguard-daemon.conf
./OUsbGuard -r /mnt/image --fail-on high --json
./OUsbGuard --demo
./OUsbGuard --help
```

---

## 📦 Part of OwlSec Toolkit

This tool is part of the **OwlSec** suite — a collection of 300+ security and privacy tools.

🔗 [owlsec.org](https://owlsec.org)

---

## ©️ License

MIT License — © Khaled S. Haddad

*Tools are distributed as pre-built executables. Source code is proprietary.*
