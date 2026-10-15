# Portunus

[한국어](README.md) · **English**

**A workspace for IT engineers to connect, diagnose and fix — all in one place.**

Portunus is a Windows remote access and operations toolkit for engineers who run servers, networks, databases, security appliances and cloud resources.

**[Download the latest installer](https://github.com/bluewind201/Portunus/releases/latest)**

SSH, SFTP, Telnet, serial, RDP, VNC and RustDesk; Proxmox, IPMI and SNMP; Docker and Kubernetes; database, HTTP and AWS management, plus network diagnostics, in a single app. The interface is available in **English and Korean** (Settings → Display → Language).

## Why Portunus

| Strength | What it changes in daily work |
|---|---|
| **One flow from connecting to fixing** | Register IP discovery results as assets, then continue with terminal, SFTP, Docker and Kubernetes work over the saved SSH connection. AWS RDS endpoints hand off directly to the database explorer. |
| **A terminal that helps you type** | Context-aware suggestions for Linux, Cisco and database subcommands, options and arguments. It also shows next-step hints after the command you just ran and shortcut hints for vim, less, top and nano. You can require confirmation before risky commands run. |
| **Many devices on one screen** | 2–4 pane split views. Drag a tab out to detach it into its own window, and drag it back to dock. Broadcast input to several terminals and save workspace sets for repeated work. |
| **From bare metal to the cloud** | Dedicated screens for IPMI hardware health and power, Proxmox VM consoles, Docker, k8s/k3s, databases, and AWS EC2, RDS and S3. |
| **No dedicated agent required** | IP discovery and bulk DNS, TCP and HTTPS checks do not install anything on the targets. Server management uses the existing SSH, API, SNMP and BMC interfaces. |
| **Safe storage and migration of connection details** | A vault encrypted with AES-256-GCM under an Argon2id master password. Import from CSV or Excel, and export as password-free CSV or an encrypted session backup. |

## What you can do

| Area | Main features |
|---|---|
| Remote access · files | SSH, Telnet, serial, raw TCP, SFTP, external RDP and RustDesk, built-in VNC, jump hosts and SSH tunnels |
| Terminal productivity | Context-aware completion, next-step hints, command snippets, risky-command confirmation, vim/less/top/nano hints, session logs |
| Workspace | Session folders, search, favorites and environment badges; 2–4 pane split, detached windows, broadcast input, workspace sets |
| Network diagnostics | IP range discovery, path analysis, ping, traceroute, port scan, DNS, SNMP, bulk device checks, packet capture and analysis |
| Servers · virtualization | Docker, Kubernetes/k3s/microk8s, Proxmox VE, IPMI/BMC (power, sensors, event log, SOL console, web console auto-login) |
| Databases · APIs | PostgreSQL, MySQL/MariaDB, SQLite; SQL queries, changes and operational checks; HTTP requests and bulk URL checks |
| AWS | IAM keys, existing CLI profiles and SSO; EC2, RDS, S3, VPC, security groups, IAM audit, SSM sessions |
| Operations support | Config diff, Nmap, VPN connection status, built-in SFTP/TFTP/syslog servers |
| Calculators · converters | Subnet, MAC, Wake-on-LAN; JSON, Base64, URL, JWT, Unix time, SHA-256 |
| Storage · personalization | Password vault, bulk change of saved passwords, import/export, 14 themes, optional PC info bar, signed updates, English/Korean UI |

## Videos

- **[Full feature overview (MP4, 1 min 38 s)](https://github.com/bluewind201/Portunus/releases/download/v1.4.0/portunus-features-v1.4.mp4)**: feature cards and example screens covering remote access, terminal assistance, network diagnostics, servers, databases, AWS, storage and settings.
- **[24-second demo (MP4)](https://github.com/bluewind201/Portunus/releases/download/v1.4.0/portunus-intro-v1.4.mp4)**: the workspace, IP range discovery, config diff and theme settings, in that order.

The videos and screenshots show the Korean UI with silent Korean captions. They were recorded in the real app using virtual devices and sample data. They contain no PC names, real accounts, private or public IPs, gateways or saved connection details. `192.0.2.x` is a documentation-only example range, and the IP discovery results are demo data.

## Screenshots

**A workspace that brings connections and operations together.** Organize sessions and favorites, then continue with quick connect and the engineer tools.

![Workspace — virtual sessions and favorites](media/01-workspace.png)

**Discover only the IP ranges you need.** Specify a CIDR or a start/end address, review the replies and open ports, then register them as assets or save them as CSV.

![IP range discovery — sample data](media/02-ip-discovery.png)

**Compare configuration changes line by line.** Additions and deletions in device and service configs are color-coded, and you can show only the changed lines.

![Config diff — a fictional service config](media/03-config-diff.png)

**Make it yours.** Choose from 14 themes, an accent color, spacing and fonts, and manage terminal, vault and update settings by section.

![Display settings and themes](media/04-settings.png)

## Install and update

- Requires Windows 11 x64. The installer installs for the current user and includes the WebView2 installer.
- On first launch the language follows your Windows display language. Change it any time in Settings → Display → Language.
- Check for new versions in Settings → Updates. Since 1.4 the app checks automatically at startup and every 6 hours, and asks before closing connections and restarting to install.
- Users on 1.3 or earlier need to install 1.4 or later manually once.
- Update files are verified with a public key built into the app. The user DB is backed up before installing, and existing sessions, the password vault and settings are kept.
- Compare installer hashes with `SHA256SUMS.txt`. The `.sig` and `latest.json` files are used by the in-app updater.
- Trust in the Windows code-signing certificate and SmartScreen reputation are separate from the update signature. Check the publisher, the hash and where you downloaded the file from.

## What's new in 1.5

- **English UI.** Choose Korean or English in Settings → Display → Language. Menus, dialogs, notifications, errors, terminal suggestions and command guides are all translated. The IP range discovery screen is still Korean only.

This repository is for **distribution only** and does not contain the application source code. The Source code ZIP/TAR that GitHub provides contains only this repository's documents and images. To install, download the installer from Releases.

License, copyright and source information for bundled third-party tools is in `tools/THIRD-PARTY-NOTICES.txt` and the license folder in the install directory. This repository does not grant any rights to the Portunus source code.
