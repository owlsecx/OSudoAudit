# 🦉 OSudoAudit

<p align="center">
  <img src="https://img.shields.io/badge/Platform-Linux-0a0c10?style=flat-square"/>
  <img src="https://img.shields.io/badge/Category-OCore-blue?style=flat-square"/>
  <img src="https://img.shields.io/badge/License-Proprietary-orange?style=flat-square"/>
  <img src="https://img.shields.io/badge/Part%20of-OwlSec%20Toolkit-7b5ea7?style=flat-square"/>
  <img src="https://img.shields.io/badge/Version-1.0.0-cyan?style=flat-square"/>
</p>

> **OSudoAudit** — Offline Sudoers Policy Auditor

---

> ⚠️ **AUTHORISED USE ONLY** — Use only on systems you own or have explicit written permission to test. Unauthorised use is illegal.

---

## 📌 Overview


OSudoAudit is an offline, strictly read-only sudoers policy auditor that parses Defaults, aliases, Runas specs, tags, digests and includes with full continuation and quoting support. It runs 60+ checks mapped to CWE and MITRE ATT&CK T1548.003, backed by a GTFOBins-style escape knowledge base of 150+ binaries, and detects duplicate or conflicting rules. It produces a risk grade and exports TXT, Markdown, JSON, CSV or SARIF for CI gating.

---

## ✨ Features


- Tolerant offline sudoers parser (Defaults, aliases, tags, digests, includes, continuations, quotes)
- Collected-tree mode (--root) with absolute path remapping for forensic images
- 60+ checks mapped to CWE and MITRE ATT&CK T1548.003
- GTFOBins-style privilege-escalation knowledge base covering 150+ binaries
- Duplicate / conflict detection with risk grade and CI gate (--fail-on)
- Export to TXT, Markdown, JSON, CSV and SARIF 2.1.0 plus a --demo self-test

---

## ⚙️ Requirements

- **Linux**
- **No Python installation needed** — runs as a standalone executable

---

## 🚀 Usage


```bash
./OSudoAudit --file /etc/sudoers --format sarif -o sudo.sarif
./OSudoAudit --scan --gtfo ALL
./OSudoAudit --root /mnt/image --fail-on high
./OSudoAudit --demo
./OSudoAudit --help
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
sudo strace -f -e trace=network ./OSudoAudit --help   # watch every network call
firejail --net=none ./OSudoAudit --help               # deny the network entirely
```

Release signing, GPL compliance and vulnerability reporting:
[**TRUST.md**](https://github.com/owlsecx/owl-os/blob/main/TRUST.md)
