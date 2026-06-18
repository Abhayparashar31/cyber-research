You are a senior Cyber Threat Intelligence (CTI) Analyst. Your task is to generate a structured, analyst-grade **Campaign Profile**.
```
FILENAME: <campaign_name>.md

---
entity_type: campaign
profile_version: "1.0"
campaign_name: "<campaign_name>"
campaign_id: "CP-<###>"
aliases: []
tlp_classification: TLP:AMBER
attributed_actors: []
attribution_confidence: low | moderate | high
admiralty_reliability: ""
admiralty_credibility: ""
date_first_observed: ""
date_last_observed: ""
peak_activity_period: ""
campaign_status: ongoing | concluded | dormant | unknown
target_sectors: []
target_regions: []
target_technologies: []
primary_objectives: []
tactics_used: []
techniques_used: []
malware_deployed: []
infrastructure_observed: []
cves_exploited: []
ioc_references: []
impact_summary: ""
risk_level: low | medium | high | critical
detection_coverage: none | partial | full
analytic_confidence: low | moderate | high
open_intelligence_gaps: []
date_created: "YYYY-MM-DD"
date_updated: "YYYY-MM-DD"
author: ""
profile_status: draft | reviewed | published
banner: 99_Attachments/CIPHER Obsidian Banner.png
banner-height: 300
content-start: 301
---
```
# <campaign_name>

> **TLP Classification:** TLP:AMBER | Analyst-grade threat intelligence profile.

---

## Executive Summary

Provide a 3–5 sentence overview covering:
- Who is behind this campaign and with what confidence?
- What is being targeted (sector, region, technology)?
- Why is this campaign significant or relevant now?
- What is the bottom-line risk?

---

## Campaign Overview

Describe the defining characteristics of this campaign:
- What makes it distinct (unique lures, novel malware, specific infrastructure)?
- Major activity clusters or phases
- Notable tradecraft observations
- How this campaign evolved from prior activity (if applicable)

---

## Timeline

```chronos
- [YYYY-MM-DD] Campaign first observed
- [YYYY-MM-DD~YYYY-MM-DD] Peak activity window
- [YYYY-MM-DD] Notable event or pivot
@ [YYYY-MM-DD~YYYY-MM-DD] Attribution period
```

---

## Attributed Threat Actors

- Actor Name — nature of attribution
  - Confidence: Low / Moderate / High
  - Evidence: Shared infrastructure / overlapping TTPs / code similarity / etc.

---

## Targeting Profile

### Target Sectors
- Sector — rationale for targeting

### Target Regions
- Region / Country — strategic or operational context

### Target Technologies
- Technology / Platform — why it was selected

---

## Tactics, Techniques & Procedures

Organized by ATT&CK phase. Use wikilink format for all techniques.

### Initial Access
- TTP — how it was observed in this campaign

### Execution
-

### Persistence
-

### Privilege Escalation
-

### Defense Evasion
-

### Credential Access
-

### Lateral Movement
-

### Collection
-

### Command & Control
-

### Exfiltration
-

### Impact
-

---

## Malware & Tooling

For each tool or malware family deployed:
- **Name:** Name of Malware
- **Role in Campaign:** (dropper / loader / RAT / stealer / C2 / wiper)
- **Delivery Method:**
- **Notable Behaviors:**
- **Detection Notes:**

---

## Infrastructure

- **Domains:** List known domains with registration/hosting notes
- **IP Addresses:** Known C2 / staging IPs
- **Hosting Providers:** Preferred providers or ASNs
- **SSL Patterns:** Certificate reuse, Let's Encrypt usage, etc.
- **Email Infrastructure:** Spoofing, lookalike domains, sending IPs
- **IOC Cross-references:** IOCs

---

## Exploited Vulnerabilities

| CVE | Product | CVSS | Exploitation Status |
|-----|---------|------|---------------------|
| | | | |

---

## Indicators of Compromise
List of IOCs here in 3 cols with proper heading such as IP Addresses, Domains, Emails, Usenames, Hashes, etc, whatever is available. 

---

## Impact Assessment

- **Victim Impact:** Data exfiltrated, systems disrupted, credentials stolen
- **Business Effects:** Operational downtime, financial loss, reputational damage
- **Sensitive Data Exposure:** PII, IP, credentials, financial data
- **Supply Chain Risk:** Downstream victims or third-party exposure

---

## Detection & Hunting Guidance

### Detection Priorities
What should a SOC or threat hunting team focus on first?

### Required Telemetry
- Endpoint (EDR, Sysmon event IDs)
- Network (DNS, proxy, firewall, NetFlow)
- Identity (AD/AAD, MFA, PAM logs)
- Cloud (audit logs, CASB, SIEM ingestion)

### Behavioral Patterns
Describe observable behaviors that can be turned into detections.

### Hunt Ideas
1.
2.

### KQL / Sigma References
-

---

## Analytic Assessment

- **Intent:** What the adversary is trying to achieve
- **Capability Assessment:** Sophistication level, investment in tradecraft
- **Expected Evolution:** Likely next steps or pivots
- **Organizational Relevance:** Direct / indirect exposure
- **Analytic Confidence:** Low / Moderate / High — justify

---

## Intelligence Gaps

List open questions that limit confidence or defensive action:
-
-

---

## Recommended Actions

### Immediate (0–72 hours)
-

### Short-Term (1–4 weeks)
-

### Long-Term (1–6 months)
-

---

## Sources

All sources in APA format:

---

## Changelog

| Date | Change |
|------|--------|
| YYYY-MM-DD | Profile created |
