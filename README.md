# AutoClearance 

<div align="center">

![Python](https://img.shields.io/badge/Python-3.10%2B-blue?style=for-the-badge&logo=python)
![CrewAI](https://img.shields.io/badge/CrewAI-Powered-orange?style=for-the-badge)
![License](https://img.shields.io/badge/License-MIT-green?style=for-the-badge)

**Automating Cross-Border Logistics Compliance with Multi-Agent AI**

[Features](#-key-features) • [Architecture](#-system-architecture) • [Getting Started](#-getting-started) • [The Story](#-the-story)

</div>

---

##  The Problem

In the cross-border logistics industry (specifically the **China-US Dedicated Line**), highly skilled professionals are trapped in low-value work.

Based on my analysis of real-world operations, **70% of a customs broker's time** is occupied by repetitive data processing:

* Manual Entry:** Typing data from messy PDF/Image invoices into ERP systems.
* Human Error:** Typos in HS Codes or weight discrepancies (Gross Weight < Net Weight).
* Inefficiency:** Valuable human capital is wasted on "Copy-Paste" tasks instead of strategic compliance.

##  The Solution: AutoClearance

**AutoClearance** is a **Multi-Agent System** engineered to replace the manual data entry pipeline. It acts as a virtual "Compliance Department" that works 24/7.

| Feature | Traditional Workflow | AutoClearance AI |
| :--- | :--- | :--- |
| **Data Ingestion** | Manual Typing (Avg. 20 mins/doc) | **OCR + LLM Extraction (< 30 secs)** |
| **Logic Check** | Manual Calculator | **Statistical Audit (Auto-Flagging)** |
| **Output** | Copy-Paste to Excel | **Standardized JSON/CSV API** |

---

## System Architecture

I designed this system using **CrewAI** to orchestrate three specialized agents.

```mermaid
graph LR
    A[Raw Invoice <br> PDF/Image] --> B(Ingest Agent <br>  Cleaner)
    B --> C{Auditor Agent <br>  Logic Check}
    C -- Pass --> D[Delivery Agent <br> Formatter]
    C -- Fail --> E[Error Report <br>  Alerts]
    D --> F[ERP System <br> JSON/XML]
