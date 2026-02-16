---
layout: default
title: Systematic Agentic Pressure - Research - selfdriven AI
permalink: /research/systematic-agentic-pressure
---

# Systematic Agentic (AI-automated Attack) Pressure

**How automated AI attack agents increase systemic risk for “hub” infrastructure.**

Central cloud services (hyperscalers, major SaaS platforms, identity providers, CI/CD hosts, API gateways, observability stacks) have always been high-value targets. What changes in an “agentic” era is **tempo and scale**: automated AI attack agents compress the full kill chain—recon → initial access → privilege escalation → lateral movement → persistence → monetisation—into continuous, adaptive loops.

This paper describes why AI-enabled attackers disproportionately threaten central cloud, the dominant agent-driven attack vectors, the systemic “blast radius” problem created by multi-tenant hubs, and a practical defense posture that assumes attackers can iterate faster than humans.

## 1. Why central cloud becomes more fragile in an AI-agent era

### 1.1 The attacker advantage is now *iteration speed*

Generative AI already lowers the cost of producing credible phishing, exploit variants, and operational playbooks. More importantly, agentic systems can *chain* these steps and run them continuously with feedback from results.

Recent reporting highlights accelerating attack conditions and AI being used in real campaigns (e.g., AI-generated decoys).

- [Reuters](https://www.reuters.com/world/europe/russian-defense-firms-targeted-by-hackers-using-ai-other-tactics-2025-12-19/m)

### 1.2 Central cloud is a “trust concentrator”  
Cloud concentrates:
- **Identity** (SSO, OAuth, API keys, service accounts)
- **Control planes** (IAM, Kubernetes, serverless, infra APIs)
- **Data gravity** (object stores, warehouses, logs)
- **Software supply chains** (registries, CI/CD, artifact stores)

So compromise isn’t just “one org breached”—it can become a *cross-tenant or ecosystem event* when shared dependencies or identity layers are abused.

### 1.3 The attack surface is expanding faster than teams can govern  
Enterprise AI adoption expands API surfaces, permissions, plugins/tools, and data movement. Security organizations report frequent attacks against AI services and growing API/IAM exposure.

- [IT Pro](https://www.itpro.com/cloud/cloud-security/cloud-security-teams-are-in-turmoil-as-attack-surfaces-expand-at-an-alarming-rate)

## 2. Threat model: the automated attack-agent loop

An AI attack agent (or swarm) is best modeled as:

**Goal → Plan → Execute → Observe → Adapt → Repeat**

Key properties:
- **Autonomy**: chooses next actions without human prompting
- **Parallelism**: runs thousands of experiments concurrently
- **Adaptation**: mutates payloads/paths to evade controls
- **Tool use**: natively integrates scanners, cloud CLIs, exploit kits, credential checkers, and OSINT

This shifts the defender’s problem from “stop a campaign” to “withstand continuous probing.”

Regulators and government guidance increasingly emphasize that autonomy and speed change operational risk assumptions.

- [Reuters](https://www.reuters.com/markets/funds/agentic-ai-race-by-british-banks-raises-new-risks-regulator-2025-12-17/)

## 3. The most dangerous AI-amplified vectors against cloud hubs

### 3.1 Identity compromise at scale (the control-plane key)  
**Why it worsens with agents**: AI boosts phishing quality and can dynamically tailor lures, pretexts, and timing using OSINT; agents can also automate MFA fatigue attempts, token theft workflows, and OAuth consent traps.

Impact:
- Stolen SSO session → access to cloud consoles
- OAuth token abuse → persistence without passwords
- Service account key exposure → machine-speed exploitation

### 3.2 API abuse and “permission-shaped” attacks  
Modern cloud is an API. Attack agents can:
- Enumerate endpoints and permissions
- Discover weak auth or overly-broad scopes
- Chain misconfigurations into privilege escalation

Cloud/API attack growth is frequently called out as a leading risk area.

- [IT Pro](https://www.itpro.com/cloud/cloud-security/cloud-security-teams-are-in-turmoil-as-attack-surfaces-expand-at-an-alarming-rate)

### 3.3 Misconfiguration exploitation as a continuous harvest

Attack agents are excellent at:
- Scanning for exposed buckets, dashboards, admin ports
- Testing common IaC patterns for privilege mistakes
- Re-checking targets repeatedly (because configs drift)

The key change is persistence: agents don’t “finish”—they keep watching for a momentary opening.

### 3.4 Supply-chain automation (CI/CD, dependencies, artifacts)

Centralized build systems and registries create leverage:
- Dependency confusion/typosquatting
- Poisoned container images
- Compromised CI runners
- Secrets exfiltration from pipelines

An agent can generate convincing PRs, craft malicious packages, and iterate until it finds a project with weaker review gates.

### 3.5 Data exfiltration with camouflage

Agents can:
- Select high-value datasets automatically (contracts, credentials, PII, key material)
- Exfiltrate slowly using “normal-looking” API patterns
- Use living-off-the-land cloud actions (snapshot/copy/export) to blend in

### 3.6 “Economic denial of service” (cost attacks)

Instead of knocking you offline, agents can:
- Trigger serverless invocations, GPU jobs, or egress-heavy workflows
- Inflate bills or exhaust quotas
- Create internal pressure to disable protections “to restore service”

This is uniquely cloud-shaped: the meter is part of the attack surface.

## 4. Systemic risk: multi-tenant blast radius and correlated failure

Central cloud concentrates not just compute, but shared assumptions:
- Common identity providers
- Shared third-party libraries and registries
- Standard reference architectures (same mistakes repeated)
- Centralized monitoring pipelines (if logs are impaired, everyone is blind)

That creates correlated failure modes:
- One exploited zero-day affects thousands of tenants
- One compromised upstream dependency fans out widely
- One identity layer incident locks out critical services

Government threat reporting shows rising volumes of proactive notifications and confirmed incidents—evidence that defenders are being pushed into higher tempo operations.

- [Cyber Security Australia](https://www.cyber.gov.au/about-us/view-all-content/reports-and-statistics/annual-cyber-threat-report-2024-2025m)

## 5. What “good” defense looks like when attackers are agentic

This is not about one silver bullet. It’s about changing the shape of the system so automation can’t chain small wins into total compromise.

### 5.1 Assume breach of identity; design for containment

- Mandatory phishing-resistant MFA / passkeys for admins
- Short-lived tokens, scoped credentials, no long-lived access keys
- Separate “human admin” and “workload” identities
- Tiered admin (break-glass accounts stored offline, audited use)

### 5.2 Make permissions *boring* (least privilege, by default)

- Deny by default; explicit allow
- Permission boundaries / policy guardrails
- “No wildcard” policies in production
- Continuous IAM linting and drift detection

### 5.3 Rate-limit, shape traffic, and detect abnormal tool use

Because agents rely on repeated probing:
- Strict API throttling per identity, per project, per IP/ASN
- Behavior-based anomaly detection (new regions, new user agents, unusual sequences)
- Step-up auth for sensitive API calls (key export, role changes, policy edits)

### 5.4 Secure the software supply chain like it’s production infrastructure

- Signed artifacts, provenance (SLSA-style), SBOMs
- Private registries with strict publishing controls
- CI/CD secrets isolation (OIDC federation over static keys where possible)
- Mandatory review + policy checks for pipeline changes

### 5.5 Observability that survives compromise

- Immutable logging (write-once / separate account)
- Cross-account log replication
- Alerts on log disruption (delete, disable, retention edits)

### 5.6 “Agentic defense” with human gating

Attackers will use AI; defenders should too—but safely:
- Automated triage + correlation, not autonomous “delete everything”
- Red-team simulation with AI agents (validated in test environments)
- Continuous control verification (policy-as-code + runtime checks)

Industry and government guidance is increasingly converging on AI-specific security controls and profiles that map AI risks into standard cybersecurity programs.

- [nvlpubs.nist.gov](https://nvlpubs.nist.gov/nistpubs/ir/2025/NIST.IR.8596.iprd.pdfm)

## 6. Practical roadmap for cloud providers and cloud customers

### Providers (CSP / major SaaS)

1. **Harden the control plane**: extra protections for IAM, org policies, key material.
2. **Default secure**: secure-by-default templates; “insecure configuration” as an explicit opt-out.
3. **Attack-surface contracts**: publish and enforce rate limits and abnormal-usage triggers.
4. **Cross-tenant isolation discipline**: minimize shared components that can cross boundaries.
5. **Transparent incident primitives**: rapid, customer-actionable guidance when systemic issues occur.

### Customers (enterprises / communities / startups)

1. Treat **identity and CI/CD** as Tier-0 assets.
2. Implement **continuous posture management** (configs, IAM drift, exposed services).
3. Replace static keys with **short-lived federated identity** wherever possible.
4. Practice **blast-radius drills**: “what if an admin token is stolen?”
5. Budget for **cost-attack controls**: quotas, egress limits, anomaly alerts.

## 7. Conclusion

AI-enabled attack agents don’t create entirely new categories of cloud risk; they weaponise the gaps already present—over-permissive IAM, sprawling APIs, supply-chain trust, configuration drift—by applying relentless, adaptive iteration.

Central cloud services are uniquely exposed because they are *hubs of trust and control*. The correct response is not to abandon cloud, but to rebuild cloud security assumptions around:
- containment over prevention,
- immutable evidence over “best effort logging,”
- least privilege over convenience,
- and defensive automation that is verified and human-governed.

### References (selected)
- ASD ACSC Annual Cyber Threat Report 2024–25  [oai_citation:6‡Cyber Security Australia](https://www.cyber.gov.au/about-us/view-all-content/reports-and-statistics/annual-cyber-threat-report-2024-2025m)  
- NIST Cybersecurity Framework Profile for AI (draft)  [oai_citation:7‡nvlpubs.nist.gov](https://nvlpubs.nist.gov/nistpubs/ir/2025/NIST.IR.8596.iprd.pdfm)  
- NIST Adversarial Machine Learning taxonomy/terminology  [oai_citation:8‡nvlpubs.nist.gov](https://nvlpubs.nist.gov/nistpubs/ai/NIST.AI.100-2e2025.pdfm)  
- CISA + partners joint guidance on secure AI integration (AI agents)  [oai_citation:9‡cisa.gov](https://www.cisa.gov/news-events/alerts/2025/12/03/cisa-australia-and-partners-author-joint-guidance-securely-integrating-artificial-intelligencem)  
- ENISA Threat Landscape 2025  [oai_citation:10‡enisa.europa.eu](https://www.enisa.europa.eu/sites/default/files/2025-10/ENISA%20Threat%20Landscape%202025_0.pdfm)  
- Reporting on cloud attack-surface expansion and AI-service attacks  [oai_citation:11‡IT Pro](https://www.itpro.com/cloud/cloud-security/cloud-security-teams-are-in-turmoil-as-attack-surfaces-expand-at-an-alarming-ratem)  

---

## Related
- [Governance Risks due to Systematic Agentic Pressure](/research/systematic-agentic-pressure/governance)