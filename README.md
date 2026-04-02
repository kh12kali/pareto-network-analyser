# Pareto Law Network Traffic Analyser

**Type:** Network Analysis · Python Scripting · Log Analysis  
**Tools:** Python · CentOS · Windows log analysis  
**Principle:** Pareto (80/20 Rule) applied to network traffic

---

## Overview

A custom Python script that applies the Pareto Principle (80/20 rule) to network  
log analysis across multiple operating systems. Instead of monitoring everything equally,  
the script automatically identifies the 20% of network nodes responsible for 80% of  
traffic — enabling faster, more focused network management and anomaly detection.

---

## The Problem

As networks grow larger and more complex, monitoring every device and connection  
equally becomes expensive and inefficient. Traditional tools generate too much noise,  
making it hard to identify real problems quickly.

Most network issues — slowdowns, security threats, bottlenecks — are caused by a  
small number of devices, applications, or protocols. This is the Pareto principle in action.

---

## The Solution

This project builds a script that:
1. Parses network logs from multiple operating systems
2. Calculates traffic contribution per source node
3. Ranks nodes by traffic volume
4. Identifies the top 20% of contributors (the critical nodes)
5. Outputs a prioritised alert list for network administrators

---

## Supported Log Sources

| Operating System | Version |
|---|---|
| CentOS (Linux) | Latest |
| Windows 7 | 64-bit |
| Windows 7 | 32-bit |
| Windows XP | — |
| Windows Vista | — |

Cross-platform support ensures the analyser works in mixed enterprise environments  
where multiple OS types run simultaneously.

---

## How It Works

```
Input: Raw network logs (multiple OS formats)
         ↓
Step 1: Parse logs → extract source IPs, protocols, packet counts
         ↓
Step 2: Aggregate traffic per source node
         ↓
Step 3: Sort by traffic volume (descending)
         ↓
Step 4: Calculate cumulative traffic percentage
         ↓
Step 5: Identify cutoff point at 80% of total traffic
         ↓
Output: Top 20% of nodes driving 80% of traffic
        + anomaly alerts for unusual spikes
```

---

## Key Features

- **Multi-OS log parsing** — handles different log formats from Linux and Windows
- **Pareto cutoff detection** — automatically finds the 20% threshold
- **Anomaly flagging** — highlights nodes with sudden traffic spikes
- **Clean output** — ranked table of critical nodes with traffic percentages
- **Lightweight** — no external dependencies beyond Python standard library

---

## Results & Benefits

- Reduces monitoring noise by focusing on critical 20% of traffic sources
- Speeds up troubleshooting — administrators know exactly where to look
- Helps identify security threats faster (unusual traffic spikes from specific nodes)
- Scales to both small and large enterprise networks
- Works across mixed OS environments without separate tools

---

## Skills Demonstrated

- Python scripting for security and network analysis
- Log parsing across multiple formats
- Application of statistical principles to real network problems
- Cross-platform compatibility
- Network traffic analysis and anomaly detection

---

## Files in This Repository

- `pareto_analyser.py` — Main Python script *(uploading soon)*
- `sample_logs/` — Sample log files for testing *(uploading soon)*
- `README.md` — This file

---

*Built as a network security research and analysis project.*
