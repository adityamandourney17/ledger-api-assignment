# Task 4 – Attack Surface Reconnaissance

## Objective

Perform passive reconnaissance and technology fingerprinting for the target domain:

- Target: `dodopayments.tech`

The goal was to enumerate subdomains, identify live hosts, fingerprint technologies, and analyze the TLS/SSL configuration using publicly available information only.

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

```
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
│   ├── 01-subfinder(2).png
│   ├── 02-assetfinder(1).png
│   ├── ...
│   └── 06-testssl(9).png
│
└── README.md
```

---

## Reconnaissance Workflow

1. Enumerated subdomains using Subfinder.
2. Enumerated additional assets using Assetfinder.
3. Performed passive enumeration using Amass.
4. Combined and deduplicated all discovered subdomains.
5. Verified live hosts using Httpx.
6. Fingerprinted web technologies using WhatWeb.
7. Performed SSL/TLS assessment using testssl.sh.

---

## Findings Summary

- Multiple subdomains were discovered.
- Live web services were identified.
- Cloudflare was detected as the CDN/WAF.
- Multiple services were hosted behind Cloudflare.
- TLS 1.2 and TLS 1.3 are supported.
- Legacy TLS 1.0 and TLS 1.1 are still enabled.
- SSL/TLS overall rating reported by testssl.sh: **Grade B**.

---

## Output Files

| File | Description |
|------|-------------|
| subfinder.txt | Subdomains discovered using Subfinder |
| assetfinder.txt | Subdomains discovered using Assetfinder |
| amass.txt | Passive Amass enumeration |
| all-subdomains.txt | Combined unique subdomains |
| live-hosts.txt | Live HTTP/HTTPS hosts |
| whatweb.txt | Technology fingerprinting |
| testssl.txt | SSL/TLS assessment |

---

## Screenshots

Execution screenshots for every reconnaissance step are included in the `screenshots/` directory.
