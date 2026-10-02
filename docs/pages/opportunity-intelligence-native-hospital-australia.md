---
layout: selfdriven
title: Intelligence-Native Hospital Australia Opportunity - selfdriven Health
permalink: /opportunity/intelligence-native-hospital/australia
---

# Intelligence-Native Hospital (Australia)

## Capability Maturity Ladder + Regulatory/Governance Model

This document covers:

- A capability maturity ladder for hospitals transitioning from *manual → assisted → autonomous* operation.
-  A practical Australian regulatory + governance model aligned to **NSQHS**, **TGA SaMD**, **Privacy Act/APPs**, and **clinical safety**.

## 1) Capability maturity ladder (Manual → Assisted → Autonomous)

This ladder is intended to be applied across the hospital, and per capability (triage, imaging, surgery, pharmacy, discharge, robotics, etc.)

Principle: **autonomy increases only when governance + evidence quality increases.**

|Level|Description|
|:---:|:----------|
|0|Manual / Legacy|
|1|Digitised|
|2|Assisted (Non-clinical automation)|
|3|Assisted Clinical Decision Support (CDS)|
|4|Semi-autonomous execution (bounded autonomy)|
|5|High autonomy clinical ops (“autonomous hospital in normal mode”)|
|6|Network-autonomous healthcare (system-of-systems)|

### Level 0 — Manual / Legacy
**Description**
- Human-led care + human coordination
- Digital systems exist but are fragmented
- EHR is a recording tool, not an operational system

**Typical traits**
- Triage by nurse/doctor only
- Imaging read by radiologist only
- Discharge plan created manually
- Paper-like consent forms
- Robots = none

**Safety**
- Safety relies on training and vigilance
- Incident investigation is manual

**Outputs**
- Mostly unstructured notes

### Level 1 — Digitised

**Description**
- Core systems digitised (EHR/PACS/LIS/pharmacy)
- Still low interoperability; workflows remain manual

**Capabilities**
- Standardised order sets
- Electronic medication management
- Central monitoring dashboards
- Basic telehealth

**AI**
- None or trivial automation (templating, macros)

### Level 2 — Assisted (Non-clinical automation)

**Description**
- Automation improves **flow and admin** without impacting clinical decisions

**Capabilities**
- AI transcription & summarisation into clinical notes
- Bed-flow forecasting
- Automated rostering assistance
- Supply chain optimisation
- **Robotics for logistics**
  - linen / waste / supplies
  - sample transport

**Governance**
- AI treated like “IT with oversight”
- Not treated as clinical device (in most cases)

**Expected KPI improvement**
- nursing/admin burden reduced
- ED length-of-stay improves

### Level 3 — Assisted Clinical Decision Support (CDS)
**Description**
- AI becomes a clinical co-pilot — but **always human-confirmed**

**Capabilities**
- AI triage suggestions (risk band + likely pathway)
- Early warning alerts (sepsis, falls, hypoxia)
- Imaging prioritisation + “second reader” support
- Medication contraindication guidance
- Auto-drafting discharge plans + follow-ups

**Controls**
- “Suggest-only mode”
- Mandatory clinician sign-off
- Confidence scores + rationale required
- Overrides logged

**Regulatory note**
Many CDS systems become **Software as a Medical Device (SaMD)** if they influence diagnosis/treatment.

### Level 4 — Semi-autonomous execution (bounded autonomy)

**Description**
- AI can trigger actions **within constraints**
- Humans supervise outcomes and exceptions

**Capabilities**
- Auto-ordering bundles based on pathway *(with clinician pre-approval)*
- Auto-escalation rules:
  - call rapid response
  - request STAT labs
- Robots execute clinical tasks:
  - autonomous medication delivery (chain-of-custody)
  - autonomous cleaning / UV cycles
  - autonomous sterile supply handling
- Closed-loop monitoring: alert → action → verify

**Required**
- Formal model governance
- Clinical safety case
- Continuous monitoring + drift detection
- Real-time auditability

### Level 5 — High autonomy clinical ops (“autonomous hospital in normal mode”)

**Description**
- Most operations are autonomous under policy
- Humans are supervisors, decision authorities, and consent holders
- Exceptions, novelty, and ethical judgement escalate to humans

**Capabilities**
- Autonomous ambulance routing + pre-triage
- Automated bed assignment + discharge orchestration
- Autonomous intra-hospital logistics spine (fully robotic)
- Autonomous pharmacy packing + delivery
- Autonomous ward insight synthesis (not autonomous decisions)
- Surgical robotics remains supervised (current likely ceiling)

**Safety bar**
- Operate like aviation:
  - redundancy
  - simulation
  - incident replay
  - safety case for each autonomous system

### Level 6 — Network-autonomous healthcare (system-of-systems)

**Description**
- Hospital is a node in a regional autonomous care network

**Capabilities**
- Federated learning across hospitals
- Shared surge prediction + outbreak detection
- Continuous post-discharge monitoring at home
- Seamless patient digital twin across providers

**Sovereignty requirement**
- strong Australian data residency + security posture
- cross-border disclosure controls

### Recommended scoring model (per capability)
Score each hospital capability across:

- **Clinical risk** (low → high)
- **Autonomy level** (0–6)
- **Evidence maturity** (data completeness + bias + drift)
- **Governance maturity** (safety case + audits)

Realistic state: a hospital can run multiple autonomy levels at once  
(e.g., logistics at Level 5, triage at Level 3, surgery at Level 4).

## 2) Australian regulatory + governance model (TGA, NSQHS, Privacy, clinical safety)

This section defines an operating model for an AI/robotics-native hospital compliant with:

- **NSQHS Standards** (clinical governance baseline)
- **TGA** (Software as a Medical Device, including many AI functions)
- **Privacy Act 1988 / APPs** (health information = sensitive data)
- practical clinical safety expectations for autonomous systems

### 2.1 Regulatory perimeter (what you must comply with)

#### A) NSQHS Standards (Australian Commission on Safety and Quality in Health Care)
NSQHS is the hospital’s **quality & safety operating baseline**.

Most critical anchor:
- **Clinical Governance Standard**: leadership, culture, safety systems, performance, care environment

AI/robotics must be governed within NSQHS clinical governance, not treated as a separate digital project.

#### B) TGA — Software as a Medical Device (SaMD), including AI

If software **influences diagnosis or treatment**, it may be regulated as a medical device.

Key implications:
- Many AI CDS functions become SaMD
- Classification depends on potential harm
- Requires documentation, validation, cybersecurity, post-market monitoring

#### C) Privacy Act 1988 + Australian Privacy Principles (APPs)

Health data is **sensitive information**.

Key themes:
- transparent collection + purpose limitation
- strong access control
- breach response
- patient access/correction
- third-party disclosure constraints
- cross-border disclosure obligations

#### D) National clinical governance for digital health

Use Australia’s digital health clinical governance frameworks as the bridge between:
- clinical safety
- privacy
- cybersecurity
- operational accountability

#### E) Emerging AI governance guidance (Australia)
Adopt national clinical AI usage guidance as internal operational policy (training + acceptable use + safety expectations).

### 2.2 Governance operating model (how the hospital runs safely)

**The “Three-Layer Governance Stack”**

Three intersecting lines of governance are required:

#### 1) Clinical Governance (NSQHS-driven)

**Owned by**
- Medical Director / Chief Nurse / Board Clinical Governance Committee

**Responsible for**
- patient safety systems
- incident response
- clinical policy
- credentialing & training
- “acceptable use” rules for AI

#### 2) Medical Device / SaMD Governance (TGA-driven)
**Owned by**
- Head of Biomedical Engineering + Regulatory Affairs + Clinical Safety Officer

**Responsible for**
- what qualifies as SaMD vs admin tool
- supplier due diligence
- validation, versioning, change control
- post-deployment performance monitoring
- reporting and corrective action

#### 3) Information Governance (Privacy + Security)
**Owned by**
- CIO / CISO / Privacy Officer

**Responsible for**
- APP compliance
- cybersecurity controls
- audit logs
- data minimisation
- model data lineage
- cross-border vendor controls

### 2.3 Committees required (operationally credible setup)

#### 1) Clinical AI Safety Committee
- approves AI use cases
- reviews safety cases
- owns “human override policy”
- approves autonomy escalation (L2→L3→L4…)

#### 2) Model Registry & Change Control Board
No model goes live without:
- evaluation report
- drift plan
- rollback plan
- versioned documentation

#### 3) Robotics Safety Committee
Robotics = physical harm domain. Requires:
- physical safety case
- collision/injury prevention protocols
- infection control protocols
- emergency stop standards
- OR sterile boundary rules

### 2.4 Clinical Safety Case template (mandatory for AI/autonomy)
Every AI capability above Level 2 should have a safety case:

- intended use statement
- clinical context
- hazards & mitigations
- validation evidence (incl. local population + workflow)
- bias analysis (priority groups)
- drift monitoring + triggers
- incident response playbook
- training/credentialing requirements
- accountability map (RACI)

### 2.5 Data + model controls (privacy + safety combined)

#### Minimum viable controls
- **data minimisation**
- **privacy by design**
- immutable audit logging (who/what/when)
- role-based access (clinical vs ops vs vendor)
- segregated environments:
  - dev / test / clinical
- release channels:
  - shadow mode → assisted → bounded autonomy → higher autonomy

#### Continuous monitoring requirements
- performance drift
- calibration drift
- false-negative monitoring (highest safety priority)
- subgroup monitoring (bias)
- novelty detection (“unknown unknowns”)

### 2.6 Practical TGA mapping: what becomes SaMD in your hospital

#### Usually SaMD
- AI suggesting diagnosis likelihood
- AI recommending treatment actions
- imaging interpretation algorithms
- triage severity scoring that influences clinical action

#### Usually not SaMD (but still governed)
- transcription
- summarisation
- workflow automation
- rostering
- supply chain optimisation

Even non-SaMD automation requires governance because admin errors can become clinical harm.

### 2.7 Compliance statement (what you should be able to assert)
An intelligence-native hospital should be able to state:

- All clinical AI is governed under NSQHS clinical governance
- SaMD-relevant AI is assessed and controlled under TGA requirements
- Patient data handling aligns with Privacy Act + APPs + health guidance
- Digital clinical safety and assurance align with national digital health clinical governance
- Clinicians are trained under a national-aligned AI clinical use policy
- All autonomous systems have safety cases, drift monitoring, and rollback procedures

---

- [Intelligence-Native Hospital](/opportunity/intelligence-native-hospital)