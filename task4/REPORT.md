# Attack Surface Assessment Report

## Target

**Domain:** `dodopayments.tech`

---

## Objective

Perform passive reconnaissance to identify publicly exposed assets, discover live services, fingerprint technologies, and review SSL/TLS configuration.

---

## Methodology

The assessment was performed using passive reconnaissance techniques without exploiting or interacting aggressively with the target.

The following activities were completed:

1. Subdomain Enumeration
2. Asset Discovery
3. Passive DNS Enumeration
4. Live Host Discovery
5. Technology Fingerprinting
6. SSL/TLS Configuration Analysis

---

## Tools Used

| Tool | Purpose |
|------|---------|
| Subfinder | Passive subdomain enumeration |
| Assetfinder | Asset discovery |
| Amass | Passive OSINT enumeration |
| Httpx | Live host detection |
| WhatWeb | Technology fingerprinting |
| testssl.sh | SSL/TLS assessment |

---

# Findings

## 1. Subdomain Enumeration

Subdomains were collected using multiple passive enumeration tools and merged into a single deduplicated list.

Outputs:

- recon/subfinder.txt
- recon/assetfinder.txt
- recon/amass.txt
- recon/all-subdomains.txt

---

## 2. Live Hosts

Live HTTP/HTTPS services were identified using Httpx.

Outputs:

- recon/live-hosts.txt

---

## 3. Technology Fingerprinting

Detected technologies include:

- Cloudflare
- Astro
- Next.js
- React
- HSTS
- Vercel
- Google Analytics
- Plunk
- SonarQube

Output:

- recon/whatweb.txt

---

## 4. SSL/TLS Assessment

SSL/TLS configuration was evaluated using testssl.sh.

### Supported Protocols

- TLS 1.2
- TLS 1.3

### Legacy Protocols

- TLS 1.0 (Enabled)
- TLS 1.1 (Enabled)

### Overall Rating

**Grade: B**

The rating is limited because legacy TLS 1.0 and TLS 1.1 are still enabled.

Output:

- recon/testssl.txt

---

# Security Observations

## Positive Findings

- TLS 1.3 supported
- Forward Secrecy enabled
- Strong cipher suites
- Valid SSL certificates
- Cloudflare protection detected

## Recommendations

- Disable TLS 1.0
- Disable TLS 1.1
- Restrict weak cipher suites where applicable
- Improve SSL configuration to achieve an **A** rating

---

# Evidence

Evidence for each stage of the assessment is available under:

```
task4/screenshots/
```

---

# Conclusion

The passive reconnaissance successfully identified publicly exposed assets, active services, web technologies, and the SSL/TLS posture of the target domain.

All command outputs, screenshots, and supporting evidence have been included as part of this submission.
