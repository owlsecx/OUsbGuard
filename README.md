# 🦉 OUsbGuard

<p align="center">
  <img src="https://img.shields.io/badge/Platform-Linux-0a0c10?style=flat-square"/>
  <img src="https://img.shields.io/badge/Category-OCore-blue?style=flat-square"/>
  <img src="https://img.shields.io/badge/License-Proprietary-orange?style=flat-square"/>
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

This tool is part of the **OwlSec** suite — a collection of 275+ security and privacy tools.

🔗 [owlsec.org](https://owlsec.org)

---

## ©️ License

Proprietary — © 2026 Owlsec LLC. All rights reserved.

*Tools are distributed as pre-built executables. Source code is proprietary.*

---

## 🔍 Verification & Transparency

This tool is closed-source. These files let you see exactly what is inside it,
without the source:

- [`SBOM.cdx.json`](SBOM.cdx.json) — CycloneDX inventory: SHA-256 of this
  binary, bundled CPython version, and every bundled library with its exact
  version and license. Feed it to Grype, Trivy or Dependency-Track to audit
  our dependencies for CVEs yourself.
- [`THIRD-PARTY-NOTICES.md`](THIRD-PARTY-NOTICES.md) — the full license text
  of every third-party component, extracted from this binary.

**No telemetry, no analytics, no licence check-in.** This tool does not phone
home. Verify that claim yourself:

```bash
sudo strace -f -e trace=network ./OUsbGuard --help   # watch every network call
firejail --net=none ./OUsbGuard --help               # deny the network entirely
```

Release signing, GPL compliance and vulnerability reporting:
[**TRUST.md**](https://github.com/owlsecx/owl-os/blob/main/TRUST.md)
