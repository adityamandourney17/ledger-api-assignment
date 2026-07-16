# Attack Surface Assessment Report

## Target

- Domain: `dodopayments.tech`

---

# Methodology

The reconnaissance was performed using passive enumeration techniques without exploiting or interacting aggressively with the target.

The following steps were performed:

1. Subdomain Enumeration
2. Asset Enumeration
3. Passive DNS Enumeration
4. Live Host Discovery
5. Technology Fingerprinting
6. SSL/TLS Configuration Analysis

---

# Tools Used

| Tool | Purpose |
|------|---------|
| Subfinder | Passive subdomain enumeration |
| Assetfinder | Asset discovery |
| Amass | Passive OSINT enumeration |
| Httpx | Live host detection |
| WhatWeb | Technology fingerprinting |
| testssl.sh | SSL/TLS assessment |

---

# Key Findings

## 1. Subdomain Enumeration

Subdomains were collected using multiple tools and merged into a single deduplicated list.

Results are available in:

- recon/subfinder.txt
- recon/assetfinder.txt
- recon/amass.txt
- recon/all-subdomains.txt

---

## 2. Live Hosts

Live HTTP/HTTPS services were identified using Httpx.

Several publicly accessible services were discovered.

Results:

- recon/live-hosts.txt

---

## 3. Technology Fingerprinting

The target is protected by Cloudflare.

Detected technologies include:

- Cloudflare
- Astro
- HSTS
- Next.js
- React
- Vercel (for some subdomains)
- Plunk
- SonarQube
- Google Analytics

Output:

- recon/whatweb.txt

---

## 4. SSL/TLS Analysis

SSL/TLS testing was performed using testssl.sh.

### Summary

Supported:

- TLS 1.2
- TLS 1.3

Legacy Protocols:

- TLS 1.0 (Enabled)
- TLS 1.1 (Enabled)

Overall Rating:

**Grade B**

Reason:

Legacy TLS versions are still enabled.

Output:

- recon/testssl.txt

---

# Security Observations

Positive Findings

- Modern TLS 1.3 support
- Forward Secrecy enabled
- Strong cipher suites
- Valid certificates
- Cloudflare protection

Potential Improvements

- Disable TLS 1.0
- Disable TLS 1.1
- Improve SSL rating from B to A

---

# Evidence

Execution screenshots for every stage are included in:

```
task4/screenshots/
```

---

# Conclusion

The passive reconnaissance successfully identified the target's exposed attack surface, live services, technologies in use, and SSL/TLS configuration.

All evidence, command outputs, and screenshots have been included as part of this submission.
