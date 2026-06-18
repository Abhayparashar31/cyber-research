<<<<<<< HEAD
# CTI REPORT GENERATION RULES

Before generating the report, interpret all values from `REPORT_CONFIGURATION` and apply the following rules.

---

# GENERAL RULES

* Treat `REPORT_CONFIGURATION` as the authoritative source of truth.
* All enabled sections must be generated.
* Omit sections that are disabled.
* Do not mention omitted sections.
* Adapt depth, style, and wording based on the selected configuration.
* Generate only content supported by available reporting.
* Clearly separate facts, assessments, and assumptions.
* Avoid unnecessary repetition between sections.

---

# ORGANIZATION PROFILE

## Company Mode

If:

```yaml
company_mode: specific
```

Then:

* Refer to the organization using:

```text
{{company_name}}
```

* Assess risk relative to:

  * Sector
  * Geography
  * Employee size
  * Technology stack

---

If:

```yaml
company_mode: generic
```

Then:

* Never mention a specific organization.
* Replace organization references with:

```text
organizations operating in the {{sector}} sector
```

---

If:

```yaml
sector: Generic
```

Then:

* Produce sector-agnostic analysis.
* Use:

```text
most enterprises
```

instead of sector-specific wording.

---

# REPORT TYPE

## CTI Bulletin

Focus on:

* Threat relevance
* Business impact
* Exposure assessment
* Operational recommendations

---

## Flash Report

Focus on:

* Speed
* Facts
* Immediate actions

Avoid lengthy contextual analysis.

---

## Executive Brief

Focus on:

* Strategic implications
* Business impact
* Risk
* Decision support

Minimize technical detail.

---

## Weekly Intelligence Report

Include:

* Threat trends
* Multiple campaigns
* Emerging patterns

---

## Vulnerability Advisory

Focus on:

* Vulnerability details
* Exploitability
* Exposure
* Mitigations

---

# TONE

## Executive

* Use plain language.
* Prioritize business impact.
* Avoid excessive technical jargon.
* Emphasize disruption, financial impact, and strategic consequences.

---

## Professional

Maintain balanced technical depth.

Suitable for mixed audiences.

---

## Technical

Assume analyst readership.

Include:

* Malware families
* Infrastructure
* ATT&CK mappings
* TTPs
* Detection opportunities

Technical terminology is acceptable.

---

# VERBOSITY

## Short

Use concise writing.

Keep:

* Executive Overview short
* Bullet lists preferred
* CTI Assessment limited

Avoid historical context.

---

## Medium

Provide standard depth.

---

## Detailed

Include:

* Threat landscape context
* Infrastructure analysis
* Victimology
* Actor profiling
* Campaign analysis

---

# REPORT MATURITY

## Strategic

Emphasize:

* Business impact
* Trends
* Long-term implications

Avoid excessive operational detail.

---

## Operational

Focus on:

* Campaign behavior
* Threat exposure
* Detection opportunities
* Mitigation actions

---

## Tactical

Prioritize:

* Indicators
* Detection logic
* Technical details
* Hunting guidance

---

# TIMELINE

If:

```yaml
include_timeline: false
```

Do not generate timeline sections.

---

If:

```yaml
timeline_format: table
```

Present timelines in tabular form.

---

If:

```yaml
timeline_format: bullets
```

Present timelines as bullet points.

---

# RISK ASSESSMENT

Apply the selected methodology.

---

Likelihood x Impact

Risk score should consider:

* Actor capability
* Exposure
* Potential impact

---

Qualitative

Use:

* High
* Medium
* Low

---

CVSS

Use standard CVSS severity terminology.

---

# INTELLIGENCE DEPTH

Generate only enabled analysis components.

Possible components include:

* Executive Summary
* Threat Landscape Context
* Actor Profiling
* Infrastructure Analysis
* Victimology Analysis
* Malware Analysis
* Campaign Analysis

Do not generate disabled components.

---

# THREAT ACTOR SECTION

Generate actor sections only if:

```yaml
enabled: true
```

Include aliases and motivations only when enabled.

Historical activity should be included only when requested.

---

# MITRE ATT&CK

Generate ATT&CK mappings only if:

```yaml
include_mapping: true
```

Include sub-techniques only if:

```yaml
include_sub_techniques: true
```

Generate ATT&CK attack-chain narratives only if:

```yaml
include_attack_chain: true
```

Never infer unsupported techniques.

Map only confirmed or strongly assessed TTPs.

---

# IOCS

Generate IOC tables only if:

```yaml
include_iocs: true
```

Include only enabled categories.

Possible categories:

* Domains
* URLs
* IP addresses
* File hashes
* Email addresses
* Mutexes
* Registry keys

Do not create empty IOC tables.

---

# ACTIONABILITY

Generate recommendations only when enabled.

Possible recommendation groups:

* Executive
* CTI
* SOC
* Incident Response

Generate:

* Detection opportunities
* Hunting guidance

only when enabled.

Generate:

* Sigma rules
* YARA rules
* KQL queries
* Splunk queries

only when explicitly requested.

---

# EXPOSURE ASSESSMENT

Assess exposure using enabled factors:

* Sector
* Geography
* Technology stack
* Third-party dependencies

Do not assume exposure without evidence.

Clearly distinguish:

* Direct exposure
* Indirect exposure
* Potential exposure

---

# ATTACK LIFECYCLE

Generate attack lifecycle discussions only when enabled.

Generate Cyber Kill Chain mappings only if requested.

---

# VISUALS

Visual placeholders should only appear when enabled.

Possible visuals:

* Campaign flow diagrams
* Attack-chain diagrams
* Infrastructure diagrams
* Geographic maps

Every visual must:

* Have a caption.
* Be referenced in the report body.

---

# APPENDIX

Generate appendices only when enabled.

Possible appendices:

* IOC Appendix
* Visual Appendix
* Source Appendix

---

# SOURCE HANDLING

Use citations when enabled.

Source titles should be hyperlinked when enabled.

Always preserve attribution.

---

# LANGUAGE

Generate content in the selected language.

Adapt complexity to the selected reading level.

---

# CONFIDENCE MODEL

Use estimative language when enabled.

Examples:

* We assess with high confidence...
* We assess with moderate confidence...
* Limited reporting suggests...

Avoid presenting assumptions as established facts.

---

# CUSTOM SECTIONS

Generate only enabled custom sections.

Possible sections:

* Key Intelligence Gaps
* Lessons Learned
* Watchlist
* Related Campaigns

---

# QUALITY REQUIREMENTS

The report must:

* Use active voice.
* Be concise.
* Avoid unnecessary jargon.
* Avoid repetition.
* Distinguish facts from assessments.
* Maintain section consistency.
* Avoid unsupported conclusions.
* Prioritize relevance over completeness.
* Provide decision-support value rather than news-style summaries.

The report is an intelligence product, not a news digest.

```
```
=======
# CTI REPORT GENERATION RULES

Before generating the report, interpret all values from `REPORT_CONFIGURATION` and apply the following rules.

---

# GENERAL RULES

* Treat `REPORT_CONFIGURATION` as the authoritative source of truth.
* All enabled sections must be generated.
* Omit sections that are disabled.
* Do not mention omitted sections.
* Adapt depth, style, and wording based on the selected configuration.
* Generate only content supported by available reporting.
* Clearly separate facts, assessments, and assumptions.
* Avoid unnecessary repetition between sections.

---

# ORGANIZATION PROFILE

## Company Mode

If:

```yaml
company_mode: specific
```

Then:

* Refer to the organization using:

```text
{{company_name}}
```

* Assess risk relative to:

  * Sector
  * Geography
  * Employee size
  * Technology stack

---

If:

```yaml
company_mode: generic
```

Then:

* Never mention a specific organization.
* Replace organization references with:

```text
organizations operating in the {{sector}} sector
```

---

If:

```yaml
sector: Generic
```

Then:

* Produce sector-agnostic analysis.
* Use:

```text
most enterprises
```

instead of sector-specific wording.

---

# REPORT TYPE

## CTI Bulletin

Focus on:

* Threat relevance
* Business impact
* Exposure assessment
* Operational recommendations

---

## Flash Report

Focus on:

* Speed
* Facts
* Immediate actions

Avoid lengthy contextual analysis.

---

## Executive Brief

Focus on:

* Strategic implications
* Business impact
* Risk
* Decision support

Minimize technical detail.

---

## Weekly Intelligence Report

Include:

* Threat trends
* Multiple campaigns
* Emerging patterns

---

## Vulnerability Advisory

Focus on:

* Vulnerability details
* Exploitability
* Exposure
* Mitigations

---

# TONE

## Executive

* Use plain language.
* Prioritize business impact.
* Avoid excessive technical jargon.
* Emphasize disruption, financial impact, and strategic consequences.

---

## Professional

Maintain balanced technical depth.

Suitable for mixed audiences.

---

## Technical

Assume analyst readership.

Include:

* Malware families
* Infrastructure
* ATT&CK mappings
* TTPs
* Detection opportunities

Technical terminology is acceptable.

---

# VERBOSITY

## Short

Use concise writing.

Keep:

* Executive Overview short
* Bullet lists preferred
* CTI Assessment limited

Avoid historical context.

---

## Medium

Provide standard depth.

---

## Detailed

Include:

* Threat landscape context
* Infrastructure analysis
* Victimology
* Actor profiling
* Campaign analysis

---

# REPORT MATURITY

## Strategic

Emphasize:

* Business impact
* Trends
* Long-term implications

Avoid excessive operational detail.

---

## Operational

Focus on:

* Campaign behavior
* Threat exposure
* Detection opportunities
* Mitigation actions

---

## Tactical

Prioritize:

* Indicators
* Detection logic
* Technical details
* Hunting guidance

---

# TIMELINE

If:

```yaml
include_timeline: false
```

Do not generate timeline sections.

---

If:

```yaml
timeline_format: table
```

Present timelines in tabular form.

---

If:

```yaml
timeline_format: bullets
```

Present timelines as bullet points.

---

# RISK ASSESSMENT

Apply the selected methodology.

---

Likelihood x Impact

Risk score should consider:

* Actor capability
* Exposure
* Potential impact

---

Qualitative

Use:

* High
* Medium
* Low

---

CVSS

Use standard CVSS severity terminology.

---

# INTELLIGENCE DEPTH

Generate only enabled analysis components.

Possible components include:

* Executive Summary
* Threat Landscape Context
* Actor Profiling
* Infrastructure Analysis
* Victimology Analysis
* Malware Analysis
* Campaign Analysis

Do not generate disabled components.

---

# THREAT ACTOR SECTION

Generate actor sections only if:

```yaml
enabled: true
```

Include aliases and motivations only when enabled.

Historical activity should be included only when requested.

---

# MITRE ATT&CK

Generate ATT&CK mappings only if:

```yaml
include_mapping: true
```

Include sub-techniques only if:

```yaml
include_sub_techniques: true
```

Generate ATT&CK attack-chain narratives only if:

```yaml
include_attack_chain: true
```

Never infer unsupported techniques.

Map only confirmed or strongly assessed TTPs.

---

# IOCS

Generate IOC tables only if:

```yaml
include_iocs: true
```

Include only enabled categories.

Possible categories:

* Domains
* URLs
* IP addresses
* File hashes
* Email addresses
* Mutexes
* Registry keys

Do not create empty IOC tables.

---

# ACTIONABILITY

Generate recommendations only when enabled.

Possible recommendation groups:

* Executive
* CTI
* SOC
* Incident Response

Generate:

* Detection opportunities
* Hunting guidance

only when enabled.

Generate:

* Sigma rules
* YARA rules
* KQL queries
* Splunk queries

only when explicitly requested.

---

# EXPOSURE ASSESSMENT

Assess exposure using enabled factors:

* Sector
* Geography
* Technology stack
* Third-party dependencies

Do not assume exposure without evidence.

Clearly distinguish:

* Direct exposure
* Indirect exposure
* Potential exposure

---

# ATTACK LIFECYCLE

Generate attack lifecycle discussions only when enabled.

Generate Cyber Kill Chain mappings only if requested.

---

# VISUALS

Visual placeholders should only appear when enabled.

Possible visuals:

* Campaign flow diagrams
* Attack-chain diagrams
* Infrastructure diagrams
* Geographic maps

Every visual must:

* Have a caption.
* Be referenced in the report body.

---

# APPENDIX

Generate appendices only when enabled.

Possible appendices:

* IOC Appendix
* Visual Appendix
* Source Appendix

---

# SOURCE HANDLING

Use citations when enabled.

Source titles should be hyperlinked when enabled.

Always preserve attribution.

---

# LANGUAGE

Generate content in the selected language.

Adapt complexity to the selected reading level.

---

# CONFIDENCE MODEL

Use estimative language when enabled.

Examples:

* We assess with high confidence...
* We assess with moderate confidence...
* Limited reporting suggests...

Avoid presenting assumptions as established facts.

---

# CUSTOM SECTIONS

Generate only enabled custom sections.

Possible sections:

* Key Intelligence Gaps
* Lessons Learned
* Watchlist
* Related Campaigns

---

# QUALITY REQUIREMENTS

The report must:

* Use active voice.
* Be concise.
* Avoid unnecessary jargon.
* Avoid repetition.
* Distinguish facts from assessments.
* Maintain section consistency.
* Avoid unsupported conclusions.
* Prioritize relevance over completeness.
* Provide decision-support value rather than news-style summaries.

The report is an intelligence product, not a news digest.

```
```
>>>>>>> 969d4c9e3e080b2bb6eb8aee7efbd103063a5e8c
