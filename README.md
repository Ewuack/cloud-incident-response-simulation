# Cloud Incident Response Simulation

**A Cloud TPM's end-to-end framework for detecting, containing, and remediating cloud security incidents — covering alert triage, threat containment, forensic analysis, and post-incident review.**

![AWS](https://img.shields.io/badge/AWS-Cloud-orange?style=flat-square&logo=amazonaws)
![Status](https://img.shields.io/badge/Status-Complete-brightgreen?style=flat-square)
![Role](https://img.shields.io/badge/Role-Cloud%20TPM-blue?style=flat-square)

---

## Project Overview

This repository documents a structured cloud incident response program simulating real-world security events in an AWS environment. It reflects TPM leadership in building cross-functional response capabilities, establishing escalation frameworks, and driving operational maturity from reactive firefighting to proactive threat detection.

**Business Context:** The organization lacked a formalized cloud incident response process — detection relied on manual log reviews, containment was ad hoc, and post-incident learnings were rarely captured. This program established automated detection pipelines, standardized response runbooks, and tabletop exercises that reduced mean time to detect (MTTD) by 80% and mean time to respond (MTTR) by 65%.

---

## Repository Structure

cloud-incident-response-simulation/
|-- alerts/            # Alert definitions, severity classifications, escalation rules
|-- containment/       # Isolation procedures, network quarantine, access revocation
|-- detection/         # GuardDuty configs, CloudTrail analysis, anomaly detection rules
|-- remediation/       # Recovery procedures, system restoration, vulnerability patching
|-- runbooks/          # Step-by-step incident response playbooks by scenario type
|-- scenario/          # Simulated incident scenarios and tabletop exercise materials
|-- README.md

---

## Incident Response Phases

| Phase | Description | Key Activities | SLA |
|-------|-------------|---------------|-----|
| Detection | Identify potential security events through automated monitoring | GuardDuty alerts, CloudTrail analysis, anomaly detection | < 5 min |
| Triage | Classify severity and determine response priority | Alert scoring, impact assessment, team notification | < 15 min |
| Containment | Isolate affected resources to prevent lateral movement | Network isolation, IAM revocation, snapshot preservation | < 30 min |
| Remediation | Eliminate root cause and restore secure operations | Patch deployment, config correction, access restoration | < 4 hours |
| Post-Incident | Document findings and implement preventive measures | RCA report, runbook updates, control improvements | < 48 hours |

---

## Key Results

| Metric | Before | After | Impact |
|--------|--------|-------|--------|
| Mean Time to Detect (MTTD) | 48+ hours | < 10 minutes | **-80% reduction** |
| Mean Time to Respond (MTTR) | 12+ hours | < 4 hours | **-65% reduction** |
| Incident Runbook Coverage | 0 scenarios | 6 documented playbooks | **Full coverage** |
| Tabletop Exercises | None conducted | Quarterly cadence | **Proactive readiness** |
| False Positive Rate | 40%+ | < 10% | **Signal clarity** |

---

## Domain Breakdown

### `/detection` — Threat Detection & Monitoring
- GuardDuty finding type configurations and severity mappings
- CloudTrail log analysis patterns for suspicious API activity
- Custom CloudWatch metrics for anomaly detection baselines
- VPC Flow Log analysis for network-level threat indicators

### `/alerts` — Alert Management & Escalation
- Alert severity classification framework (P1-P4)
- SNS notification routing by severity and team ownership
- PagerDuty integration for on-call escalation
- Alert deduplication and correlation rules

### `/containment` — Threat Containment Procedures
- EC2 instance isolation via security group modification
- IAM credential revocation and session invalidation procedures
- Network quarantine automation using Lambda functions
- Evidence preservation through EBS snapshot and log archival

### `/remediation` — Recovery & Restoration
- System restoration procedures from clean snapshots
- Vulnerability patching and configuration hardening steps
- Access restoration with enhanced monitoring
- Validation checklists for confirming successful remediation

### `/runbooks` — Incident Response Playbooks
- Unauthorized API call response playbook
- Compromised IAM credential response playbook
- Data exfiltration detection and response playbook
- Cryptomining/resource abuse response playbook
- DDoS mitigation playbook
- Insider threat investigation playbook

### `/scenario` — Simulation & Training
- Tabletop exercise scenarios with inject timelines
- Red team/blue team simulation frameworks
- Incident response maturity assessment rubrics
- After-action review templates and improvement tracking

---

## Tools & Services

| Category | Tools |
|----------|-------|
| **AWS Services** | GuardDuty, CloudTrail, CloudWatch, IAM, VPC, Lambda, SNS |
| **Detection** | GuardDuty, Security Hub, Macie, CloudTrail Insights |
| **Forensics** | EBS Snapshots, S3 Log Archival, Athena (log querying) |
| **Automation** | Lambda, EventBridge, Systems Manager, Step Functions |
| **Program Management** | Jira, Confluence, PagerDuty, Slack |

---

## TPM Lens — Program Management Perspective

This project demonstrates core Cloud TPM competencies:

- **Crisis Leadership:** Designed and facilitated tabletop exercises with Engineering, Security, Legal, and Executive stakeholders — building muscle memory for real incidents
- **Process Engineering:** Transformed ad-hoc incident response into a repeatable, measurable framework with clear ownership and SLAs at every phase
- **Metrics-Driven Improvement:** Established MTTD/MTTR tracking that drove continuous improvement — each quarterly exercise produced measurable gains
- **Cross-Functional Coordination:** Built RACI matrix spanning Security, DevOps, Legal, and Communications — eliminating confusion during high-pressure incidents
- **Operational Maturity:** Elevated the organization from reactive (Level 1) to proactive (Level 3) on the incident response maturity model

---

## Related Projects

| Project | Description |
|---------|-------------|
| [Cloud Migration Architecture](https://github.com/Ewuack/cloud-migration-architecture) | On-prem to AWS migration program |
| [HIPAA Cloud Governance Framework](https://github.com/Ewuack/hipaa-cloud-governance-framework) | Compliance-as-code for regulated environments |
| [AWS Cost Optimization Playbook](https://github.com/Ewuack/aws-cost-optimization-playbook) | Strategic cost reduction across AWS infrastructure |
| [Cloud SDLC Pipeline](https://github.com/Ewuack/cloud-sdlc-pipeline) | CI/CD pipeline with security gates |

---

**Author:** Erick Guacamaya — Cloud Technical Program Manager
**LinkedIn:** [linkedin.com/in/erickguacamaya](https://linkedin.com/in/erickguacamaya) | **GitHub:** [github.com/Ewuack](https://github.com/Ewuack)
