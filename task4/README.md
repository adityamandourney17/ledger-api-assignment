# Task 4 – Attack Surface Reconnaissance

## Objective

Perform passive reconnaissance and technology fingerprinting for the target domain.

**Target:** `dodopayments.tech`

The objective was to enumerate subdomains, identify live hosts, fingerprint technologies, and analyze the TLS/SSL configuration using publicly available information only.

---

## Tools Used

- Subfinder
- Assetfinder
- Amass (Passive)
- Httpx
- WhatWeb
- testssl.sh

---

## Directory Structure

```text
task4/
├── recon/
│   ├── subfinder.txt
│   ├── assetfinder.txt
│   ├── amass.txt
│   ├── all-subdomains.txt
│   ├── live-hosts.txt
│   ├── whatweb.txt
│   └── testssl.txt
│
├── screenshots/
│   ├── 01-subfinder(1).png
│   ├── ...
│   └── 06-testssl(9).png
│
├── README.md
└── REPORT.md
