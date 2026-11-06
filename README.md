# Kim (WardCraftSec)

Started Oct 2026 with zero tech background. 5 weeks later: live PWA with 4 API endpoints, working Python scripts, a Sigma detection rule, and a documented log review pipeline. Built entirely on a Pixel 7 running GrapheneOS in Termux.

**Seeking: Junior SOC / TI roles, UK. Fully remote.**

Skills: Sigma, SIEM (Wazuh), Python, threat intelligence, log analysis, MITRE ATT&CK, DNS, IOC enrichment.

---

## Projects

| Project | What | Status |
|---------|------|--------|
| [Save Me](https://wardcraftsec.github.io/Save-Me/) | Free PWA: guided NextDNS setup + IOC triage. 4 API endpoints, 5 tabs, 200+ lines vanilla JS, Cloudflare Worker backend. Built on Pixel 7 / Termux. | ✅ Live |
| [WardCraft](https://github.com/WardCraftSec/wardcraft) | Blue team scripts, Sigma rules, codex entries, shift-handover docs, documented log reviews | 🔄 Active |

---

## Sample Detection Rule

```yaml
title: SSH Brute Force
status: stable
logsource:
  product: windows
  service: security
detection:
  selection:
    EventID: 4625
    Status: '0xC000006D'
  condition: selection
  timeframe: 5m
  above: 10
level: high
tags:
  - attack.credential_access
  - attack.t1110.001
Full rules: [`sigmas/`](https://github.com/WardCraftSec/wardcraft/tree/main/sigmas)

---

## Stack

| Area | Tools / Tech |
|------|-------------|
| OS | GrapheneOS (Pixel 7), Termux |
| Languages | Python 3.11+ |
| Detection | Sigma, AbuseIPDB, VirusTotal, ipinfo |
| DNS | NextDNS (DoT), Cloudflare DoH |
| Infra | Cloudflare Workers, GitHub Pages, GoatCounter |
| Learning | TryHackMe, Professor Messer (Security+) |

---

## Currently

- NextDNS 30-day log review → codex entry
- Professor Messer — Security+ (SY0-701), target Q1 2027
- Wazuh home lab (planned Dec 2026)

## Next

- BTL1 (Blue Team Level 1)
- 2–3 additional Sigma rules
- Threat actor write-up (MITRE mapped)
- SOC Tier 1 applications — Q2 2027   
