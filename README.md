# 🦉 OSudoAudit

<p align="center">
  <img src="https://img.shields.io/badge/Platform-Linux-0a0c10?style=flat-square"/>
  <img src="https://img.shields.io/badge/Category-OCore-blue?style=flat-square"/>
  <img src="https://img.shields.io/badge/License-MIT-green?style=flat-square"/>
  <img src="https://img.shields.io/badge/Part%20of-OwlSec%20Toolkit-7b5ea7?style=flat-square"/>
  <img src="https://img.shields.io/badge/Version-1.0.0-cyan?style=flat-square"/>
</p>

> **OSudoAudit** — Offline Sudoers Policy Auditor

---

> ⚠️ **AUTHORISED USE ONLY** — Use only on systems you own or have explicit written permission to test. Unauthorised use is illegal.

---

## 📌 Overview

Offline sudoers / sudo policy auditor — Defaults, aliases, GTFOBins, CWE/ATT&CK

---

## ✨ Features

- Tolerant offline sudoers parser (Defaults, aliases, tags, digests, includes, continuations, quotes)
- Collected-tree mode (--root) with absolute remap
- 60+ checks → CWE + MITRE ATT&CK T1548.003
- GTFOBins-style escape knowledge base (150+)
- Duplicate/conflict detection, risk grade, CI gate
- Export TXT / Markdown / JSON / CSV / SARIF 2.1.0
- --demo self-test; strictly read-only

---

## ⚙️ Requirements

- **Linux**
- **No Python installation needed** — runs as a standalone executable

---

## 🚀 Usage

```bash
./OSudoAudit
```

---

## 📦 Part of OwlSec Toolkit

This tool is part of the **OwlSec** suite — a collection of 300+ security and privacy tools.

🔗 [owlsec.org](https://owlsec.org)

---

## ©️ License

MIT License — © Khaled S. Haddad

*Tools are distributed as pre-built executables. Source code is proprietary.*
