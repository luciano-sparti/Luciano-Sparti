# 👋 Hi, I'm Luciano

![Profile views](https://komarev.com/ghpvc/?username=Luciano-Sparti&label=Profile%20views&color=0e75b6&style=flat)

🚀 **DevSecOps Engineer** · Cybersecurity · Cloud Automation

I work at the intersection of automation, security, and reliability — building secure pipelines, custom security tooling, and infrastructure that runs itself. Currently deep-diving into **DevSecOps**, policy-as-code, and Rust-powered utilities.

### 🧰 Tech I work with
![Rust](https://img.shields.io/badge/Rust-000000?logo=rust&logoColor=white)
![Python](https://img.shields.io/badge/Python-3776AB?logo=python&logoColor=white)
![AWS](https://img.shields.io/badge/AWS-232F3E?logo=amazonaws&logoColor=white)
![Docker](https://img.shields.io/badge/Docker-2496ED?logo=docker&logoColor=white)
![Kubernetes](https://img.shields.io/badge/Kubernetes-326CE5?logo=kubernetes&logoColor=white)
![Terraform](https://img.shields.io/badge/Terraform-7B42BC?logo=terraform&logoColor=white)
![CI/CD](https://img.shields.io/badge/CI%2FCD-2088FF?logo=githubactions&logoColor=white)
![Linux](https://img.shields.io/badge/Linux-FCC624?logo=linux&logoColor=black)

---

## 📂 Projects

A running log of what I build — from shipped tools to things still on the loom.

### 👁️ Panopticon — Terminal Real-Time Network Traffic Analyzer & Lightweight NIDS
[![CI](https://github.com/Luciano-Sparti/panopticon/actions/workflows/ci.yml/badge.svg)](https://github.com/Luciano-Sparti/panopticon/actions/workflows/ci.yml)
[![Python: 3.9+](https://img.shields.io/badge/Python-3.9%2B-blue.svg?logo=python&logoColor=white)](https://www.python.org/)
[![Built with Rich](https://img.shields.io/badge/TUI-Rich-magenta.svg)](https://rich.readthedocs.io/)
**Python · Scapy · Rich TUI · CyberSecurity / NIDS · Open Source**

> *All traffic observed. Anomalies highlighted. Threats contained.* Real-time terminal packet inspection, sliding-window threat heuristics, deep host forensics, and streaming PCAP export.

Panopticon gives system administrators and security engineers an immediate, zero-overhead vantage point over network traffic directly from the terminal without the overhead of desktop GUIs:

```bash
# Install with isolated dependencies & launcher
curl -sSL https://raw.githubusercontent.com/luciano-sparti/panopticon/main/install.sh | bash

# Sniff interface with live dashboard & NIDS heuristics
sudo panopticon -i eth0 --resolve-hosts
```

- 📊 **Interactive 4-Pane TUI** — Live packet stream, ranked top-talkers with EWMA bandwidth velocity, active security alerts, and full-screen panel zoom (`1`–`4`).
- 🛡️ **Heuristic NIDS Engine** — Catches TCP SYN-scans, stealth probes (FIN/NULL/Xmas), beaconing C2 heartbeats, cleartext credential exposure, and bandwidth abuse.
- 🔍 **Deep Host Inspector** — Drill into any talker (`Enter`) to inspect open sessions, contacted ports, TLS SNI / DHCP hostnames, and process attribution (`/proc`).
- 🗄️ **Multi-Format Streaming Exporters** — Streams capture into wire-fidelity PCAP, per-packet flow CSV, and SIEM-ready alert JSONL simultaneously off-thread.

🔗 **[github.com/Luciano-Sparti/panopticon](https://github.com/Luciano-Sparti/panopticon)** · ⭐ star it if you monitor network traffic from the terminal

### 🪟 Cardea — Desktop-Ergonomic Terminal File Manager
[![CI](https://github.com/Luciano-Sparti/cardea/actions/workflows/ci.yml/badge.svg)](https://github.com/Luciano-Sparti/cardea/actions/workflows/ci.yml)
[![crates.io](https://img.shields.io/crates/v/cardea)](https://crates.io/crates/cardea)
**Rust · TUI · Ratatui · Open Source**

> *Desktop ergonomics, terminal speed.* Bridging the gap between terminal efficiency and modern desktop file managers with first-class mouse support, collapsible trees, and multimodal previews.

Cardea brings the familiar visual language of modern desktop explorers (KDE Dolphin, Windows File Explorer) into the terminal, built on an asynchronous zero-lag rendering core:

```bash
cargo install cardea # or install via one-line curl script
cardea               # launch in current directory
```

- 🖱️ **Hybrid Navigation** — Full first-class mouse ergonomics (drag & drop, context menus, column resizing) + Vim keybindings (`hjkl`) & multi-selection.
- 🗂️ **Desktop-Class Shell** — Collapsible sidebar tree, virtualized 60 FPS table (100k+ files), interactive breadcrumbs (`Ctrl+L`), tabs (`Ctrl+T`), and dual-pane Commander view (`F3`).
- 👁️ **Multimodal Previews** — Syntax highlighting via `syntect`, high-res terminal graphics (Kitty/Sixel/iTerm2), archive inspection (`.zip`, `.tar`, `.7z`), and hex dumps.
- 🛡️ **Safety & Polish** — Non-blocking async I/O workers, Freedesktop Trash (`trash-rs`) protection, and live dynamic theme hot-reloading.

🔗 **[github.com/Luciano-Sparti/cardea](https://github.com/Luciano-Sparti/cardea)** · ⭐ star it if you want desktop file manager power in your terminal

### ⚡ FATES — Declarative Process Orchestrator
[![CI](https://github.com/Luciano-Sparti/FATES/actions/workflows/ci.yml/badge.svg)](https://github.com/Luciano-Sparti/FATES/actions/workflows/ci.yml)
[![crates.io](https://img.shields.io/crates/v/fates-cli)](https://crates.io/crates/fates-cli)
**Rust · CLI · Open Source**

> *Thread management, orchestrated.* Spin to register, draw to run, cut to end — process management as the three Fates would have it.

FATES is a lightweight, declarative process orchestrator for the command line. Define your stack in one `fates.yaml`, then manage its full lifecycle with three verbs:

```bash
fates draw --all     # bring the whole stack up (dependency-ordered)
fates loom           # live dashboard of every process
fates cut --all      # tear it all down safely
```

```text
NAME        STATUS     PID      CPU%     MEMORY     LIFETIME
-------------------------------------------------------------------
postgres    RUNNING    84201    0.2%     22.4 MB    3m 12s
api         RUNNING    84350    1.4%     88.1 MB    2m 58s
frontend    RUNNING    84489    0.0%     140.2 MB   2m 47s
```

🔗 **[github.com/Luciano-Sparti/FATES](https://github.com/Luciano-Sparti/FATES)** · ⭐ star it if process juggling annoys you too


### 🔜 Upcoming
- *🗳️ Blockchain Voting System* — a tamper-evident voting platform built on blockchain, exploring verifiable, transparent elections without sacrificing voter anonymity.
- *🛡️ Compliance-as-Code Scanner* — a scanner that turns policy requirements into executable checks, so compliance becomes a CI gate instead of a yearly fire drill.
- *🔒 Encrypted Secrets Vault CLI* — a local-first, TPM-backed encrypted secrets vault for developers and DevOps workflows, storing secrets encrypted on disk with shell/env injection, rotation, and audit logging.
- *🚨 Incident Runbook Automator* — a CLI that ingests alerts, gathers related configs/logs, and drafts a timestamped incident brief with timeline, blast radius, and suggested next steps to cut MTTR.

### 🎓 Academic
- **Violence Recognition System** via Convolutional Neural Networks (TensorFlow, Python)
- **Face Recognition System** with Computer Vision (OpenCV, Laravel)

---

## 🔐 Current Focus
- Maintaining **Panopticon**, **Cardea** & **FATES**, and building security & DevSecOps tooling
- Building **Encrypted Secrets Vault CLI** and **Incident Runbook Automator**
- Automating **secure CI/CD pipelines** with policy enforcement
- Practicing **Infrastructure as Code (IaC)** and studying cloud security & OSINT

---

## 📈 GitHub Stats
![GitHub stats](https://github-readme-stats.vercel.app/api?username=Luciano-Sparti&show_icons=true&theme=radical)
![Top Langs](https://github-readme-stats.vercel.app/api/top-langs/?username=Luciano-Sparti&layout=compact&theme=radical)

### 🟢 Contribution Activity
[![Luciano's GitHub contributions over the last year](https://ghchart.rshah.org/Luciano-Sparti)](https://github.com/Luciano-Sparti?tab=activity)

---

## 🌍 Connect with Me
[![LinkedIn](https://img.shields.io/badge/LinkedIn-blue?logo=linkedin&logoColor=white)](https://www.linkedin.com/in/Luciano-Sparti/)
[![Ko-fi](https://img.shields.io/badge/Ko--fi-F16061?logo=ko-fi&logoColor=white)](https://ko-fi.com/lucianosp)
📩 Email: [luciano.sparti@proton.me](mailto:luciano.sparti@proton.me)

---

### ☕ Support my work
If a tool I built saved you time, you can [buy me a coffee on Ko-fi](https://ko-fi.com/lucianosp) — it helps me keep shipping open source. 🙏
