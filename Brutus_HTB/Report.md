## 🛡️ Brutus (Hack The Box Sherlock) – Introduction

 This Sherlock focuses on defensive investigations and log analysis.
 The scenario simulates an investigation of a Linux server (Confluence)
 that was brute-forced via SSH. The primary artifacts for analysis are:
 - /var/log/auth.log
 - wtmp (login records)

### Objective:
 - Perform an investigation from an incident responder / DFIR perspective.
 - Identify the brute-force activity, timeline, and attacker actions.
 - Find evidence of any privilege escalation, persistence, or command execution.
 - Document findings and recommended remediation.

### Rules / Notes:
 - Approach this exercise like a real-world investigation (chain of custody, timeline).
 - Manual analysis is encouraged; use tools where they add clear value.
 - Deliverables: short executive summary, timeline of events, key evidence screenshots,
   indicators of compromise (IOCs), remediation suggestions.

# Screenshot (lab start page): screenshots/brutus_start_page.png
