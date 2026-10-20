<div align="center">

# 💊 Drug-Safety Intelligence Platform

### Project Documentation

*From raw FDA adverse-event reports to clean, standardized, analysis-ready drug-safety data.*

**Digital Egypt Pioneers Initiative (DEPI) · Graduation Project**

![Phase](https://img.shields.io/badge/phase-planning%20%26%20requirements-orange?style=flat-square)
![Data](https://img.shields.io/badge/data-FAERS%20%2B%20RxNorm-blue?style=flat-square)
![Timeline](https://img.shields.io/badge/timeline-24%20Oct%20→%201%20Dec%202026-green?style=flat-square)
![Docs](https://img.shields.io/badge/docs-PDF-informational?style=flat-square)

[Contents](#-contents) · [Overview](#-overview) · [Pipeline](#-pipeline) · [Targets](#-key-targets) · [Timeline](#timeline) · [Team](#team)

</div>

> [!IMPORTANT]
> **Disclaimer:** This platform analyzes *reported* adverse events. It does not establish causation, provide medical advice, or replace professional pharmacovigilance.

---

## 📚 Contents

| Document | Description |
|:---------|:------------|
| [**Project Documentation (PDF)**](final_documentation.pdf) | Planning, literature review, requirements, and references in one document |

### What's inside

| # | Section | Covers |
|:-:|:--------|:-------|
| 1 | **Project Planning & Management** | Overview, problem statement, objectives, scope, timeline, milestones, team roles, risks, success metrics |
| 2 | **Literature Review** | FAERS and RxNorm, similar systems (openFDA, OpenVigil, AEOLUS, VigiBase), comparison, research gap |
| 3 | **Requirements Gathering** | Stakeholders, functional and non-functional requirements, data and technical requirements, constraints, acceptance criteria |

---

## 🎯 Overview

The platform ingests adverse-event reports from the **FDA FAERS** system, standardizes drug names using **RxNorm**, removes duplicate reports, and presents reporting patterns through an **interactive dashboard**. An AI component is planned on top of this core.

| | |
|:--|:--|
| **Goal** | An end-to-end data pipeline that turns raw FAERS reports into a clean, standardized dataset with a searchable dashboard |
| **Stack (planned)** | Python · SQL · PostgreSQL · dbt · OHDSI Usagi · Parquet · Docker |
| **AI (planned)** | One team member will explore AI features (e.g. drug-name matching, data exploration). Scope to be defined. |
| **Out of scope** | Diagnosis · medication recommendations · causal inference · clinical risk prediction · drug–drug interaction checking |

---

## 🔄 Pipeline

```mermaid
flowchart LR
    A["📥 Ingest<br/>FAERS + RxNorm"] --> B["🧹 Clean &<br/>validate"]
    B --> C["🔁 Deduplicate"]
    C --> D["💊 Map drugs<br/>to RxNorm"]
    D --> E["🗄️ Analytical<br/>model"]
    E --> F["📊 Signals<br/>PRR / ROR"]
    F --> G["🖥️ Dashboard"]
```

---

## 📈 Key Targets

| Metric | Target |
|:-------|:------:|
| RxNorm mapping rate | **≥ 90%** |
| Duplicate removal | **≥ 95%** |
| Search response time | **< 3 s** |
| Signal detection accuracy | **≥ 80%** |
| Test pass rate | **≥ 90%** |

---

<a id="timeline"></a>

## 🗓️ Timeline

**24 October – 1 December 2026**

```mermaid
gantt
    title Project Timeline (2026)
    dateFormat YYYY-MM-DD
    axisFormat %d %b
    section Foundation
    Planning            :a1, 2026-10-24, 4d
    Literature review   :a2, 2026-10-26, 8d
    Requirements        :a3, 2026-10-30, 7d
    section Build
    Data collection     :b1, 2026-10-31, 13d
    System design       :b2, 2026-11-03, 8d
    Development         :b3, 2026-11-10, 14d
    section Delivery
    Testing             :c1, 2026-11-22, 6d
    Documentation       :c2, 2026-11-24, 8d
```

| Milestone | Date | Deliverable |
|:----------|:----:|:------------|
| **M1** Project kickoff | 27 Oct | Approved scope and plan |
| **M2** Literature review | 2 Nov | Review section and references |
| **M3** Requirements approved | 5 Nov | Requirements specification |
| **M4** Design approved | 10 Nov | Architecture and UI mockups |
| **M5** Clean dataset ready | 12 Nov | FAERS cleaned and mapped to RxNorm |
| **M6** First prototype | 17 Nov | Working prototype (search, signals) |
| **M7** Testing complete | 27 Nov | Test report and fixes |
| **M8** Final documentation | 1 Dec | Final PDF uploaded to GitHub |

---

## Team

**Team Leader:** Youssef Asaad Saad

| Member | GitHub | Role | Documentation Sections |
|:-------|:-------|:-----|:-----------------------|
| **Youssef Saad** | [@Usf132](https://github.com/Usf132) | Team Leader · AI Engineer | 2.1 – 2.3 (Literature review: introduction, data sources, similar systems) |
| **Randa Gomaa** | [@ran-da25](https://github.com/ran-da25) | Team Member | 1.1 – 1.4 (Overview, problem statement, objectives, scope) |
| **Mariam Abdelaziz** | [@MariamAbdelaziz21](https://github.com/MariamAbdelaziz21) | Team Member | 1.5 – 1.9 (Timeline, milestones, team roles, risks, success metrics) |
| **Olivia Hanna** | [@ohanna725](https://github.com/ohanna725) | Team Member | 2.4, 2.5, 3.1 (Comparison, research gap, stakeholders) |
| **Abanoub Ayman** | [@Abanob-Ayman](https://github.com/Abanob-Ayman) | Team Member | 3.2 – 3.7 (Functional, non-functional, data, technical requirements, constraints, acceptance criteria) |

All members also contribute to data engineering and QA. Detailed technical assignments (data engineering, backend, frontend, testing) are still to be agreed and will be added here.

---

<div align="center">
<sub>Public, anonymized data only · Web sources accessed October 2026 · Items marked <i>planned</i> describe intended design, not completed work</sub>
</div>
