# OpenVAS – Open Vulnerability Assessment System

## Overview

This project presentation provides an in-depth introduction to **OpenVAS**, a powerful open-source vulnerability scanning and management platform maintained by **Greenbone Networks**. It is widely used for identifying security vulnerabilities in systems and networks.

**Contributors (Group 5):**  
- Drew Dickenson  
- Hassan Evans  
- Mentu Snoh  
- Camron Neal  

---

## Table of Contents

- [What is OpenVAS?](#what-is-openvas)
- [Project History & Evolution](#project-history--evolution)
- [Latest Release & Roadmap](#latest-release--roadmap)
- [Core Components](#core-components)
- [Architecture Overview](#architecture-overview)
- [Installation Options](#installation-options)
- [Initial Setup & Feed Updates](#initial-setup--feed-updates)
- [Scan Configurations](#scan-configurations)
- [Authenticated vs Unauthenticated Scans](#authenticated-vs-unauthenticated-scans)
- [Vulnerability Tests & Feed](#vulnerability-tests--feed)
- [Scan Workflow & Results](#scan-workflow--results)
- [Reporting](#reporting)
- [Performance Tuning](#performance-tuning)
- [Ecosystem Integration & Best Practices](#ecosystem-integration--best-practices)
- [Troubleshooting & Support](#troubleshooting--support)
- [Further Resources](#further-resources)

---

## What is OpenVAS?

OpenVAS (now part of the **Greenbone Vulnerability Management** suite) is an open-source vulnerability scanner used to perform network security assessments and vulnerability tests on target systems.

---

## Project History & Evolution

- Originated from a fork of Nessus when it went proprietary.
- Continues to evolve as part of the Greenbone Security Manager framework.
- Offers both **community** and **enterprise** versions.

---

## Latest Release & Roadmap

- Regular updates and security feeds.
- Roadmap focuses on improving scalability, performance, and enterprise integration.

---

## Core Components

- `gvmd`: Greenbone Vulnerability Manager daemon.
- `openvas-scanner`: Core scanning engine.
- `gsad`: Greenbone Security Assistant web interface.

---

## Architecture Overview

OpenVAS uses a modular architecture:
- Central manager (`gvmd`) orchestrates scans and handles reports.
- One or more scanner nodes perform tests.
- Web UI for managing configurations and reviewing results.

---

## Installation Options

- Native packages (Ubuntu, Kali, Fedora).
- Docker containers.
- Virtual appliance (Greenbone OS).
- Manual build from source.

---

## Initial Setup & Feed Updates

- Feed updates are critical for current vulnerabilities.
- Use `greenbone-nvt-sync` or `gvm-feed-update` to download the latest Network Vulnerability Tests (NVTs).

---

## Scan Configurations

- Multiple scan types: full/fast scans, custom configurations.
- Fine-tune to target specific ports, OS types, or compliance policies.

---

## Authenticated vs Unauthenticated Scans

- **Authenticated Scans:** Use credentials to log in and detect local vulnerabilities.
- **Unauthenticated Scans:** Simulate external attacker perspective; limited depth.

---

## Vulnerability Tests & Feed

- OpenVAS uses thousands of NVTs updated regularly.
- Tests cover a wide array of CVEs, OS, applications, and protocols.

---

## Scan Workflow & Results

1. Configure target and scan settings.
2. Launch scan via web UI or CLI.
3. Review scan results with severity scores (CVSS).
4. Export reports.

---

## Reporting

Built-in export formats:
- PDF, HTML, CSV, XML, TXT

Custom reports:
- XSLT for custom formatting  
- Email delivery or API integration available

---

## Performance Tuning

- Adjust `max_hosts` and `max_checks` for resource balancing.
- Use distributed scanning with multiple engines.
- Recommended: ≥4 CPU cores, 8 GB RAM for production.

---

## Ecosystem Integration & Best Practices

- REST API for automation.
- Integrate with SIEMs and ticketing systems.
- Always run regular feed updates and secure scanner credentials.

---

## Troubleshooting & Support

- **Common Issues:**
  - Feed sync failures
  - Scanner not initialized
  - Timeout errors

- **Support Channels:**
  - [Greenbone Community Forum](https://community.greenbone.net)
  - GitHub Issues
  - Matrix Chat

- **Commercial Support:**  
  Available via Greenbone Enterprise Subscriptions.

---

## Further Resources

- [Official Documentation](https://docs.greenbone.net/)
- [Greenbone GitHub](https://github.com/greenbone)
- [OpenVAS Scanner on Kali Linux](https://www.kali.org/tools/openvas/)

---

## License

This project is presented for educational purposes only.
