# Microsoft Sentinel – Defender for Endpoint Telemetry Cap Workbook

## Overview

This repository contains a **Microsoft Sentinel Workbook** designed to help security and SOC teams **identify, monitor, and manage Microsoft Defender for Endpoint (MDE) telemetry ingestion caps**.

The workbook provides visibility into Defender for Endpoint event volume, ingestion trends, and potential telemetry throttling scenarios that may impact detection coverage, investigations, or downstream analytics in Microsoft Sentinel.
Microsoft are apparently working on this issue behind the scences, so it maybe worth reaching out to your TAM. Given the importance of ProcessEvents for an XDR platform, it's important to be aware of drops. 

It is intended to support:
- Telemetry health monitoring
- Detection coverage assurance

This is intended to help investigate and should NOT be seen as 100% accurate. There may be gaps in telemetry caused by other issues.

---

## Problem Statement

Microsoft Defender for Endpoint applies **telemetry ingestion limits** based on service constraints.  
When these limits are exceeded, certain event types may be **throttled or dropped**, potentially resulting in:

- Reduced visibility during high-activity periods
- Missed detections or delayed investigations
- Inaccurate threat hunting or analytics
- Unexpected Sentinel ingestion patterns

Native visibility into these limits is limited. This workbook helps close that gap.

---

## Key Features

- 📊 **Telemetry Volume Monitoring**
  - Visualizes Defender for Endpoint event ingestion over time
  - Highlights spikes and sustained high-volume patterns

- 🚨 **Ingestion Cap Indicators**
  - Identifies conditions that may indicate telemetry throttling
  - Surfaces risk periods where ingestion caps may be exceeded

- 🧭 **Coverage & Risk Awareness**
  - Helps SOC teams understand when endpoint telemetry coverage may be degraded
  - Supports investigation confidence and detection tuning

---

## Data Sources

The workbook relies on data ingested into Microsoft Sentinel from:
- **Microsoft Defender for Endpoint**

> ⚠️ The accuracy of insights depends on proper Defender for Endpoint and Sentinel integration.

---

## Deployment

1. Download the workbook JSON file from this repository.
2. In the Azure Portal, navigate to: Microsoft Sentinel → Workbooks → Add workbook → Advanced editor
3. Paste the JSON content.
4. Save the workbook to your Sentinel workspace.
5. Adjust parameters (time range, thresholds) as needed - Defaults should be fitting.

---

## Limitations

- Telemetry caps are not always explicitly logged by Microsoft
- Some insights are **inferred based on ingestion behavior**

--

## Contributions
Claude AI
