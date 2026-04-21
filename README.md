# Active Directory Security Monitoring Lab with Splunk

## Overview
This project demonstrates how I built a small Active Directory lab and used Splunk to monitor, investigate, and visualize Windows authentication activity in a controlled environment.

The primary goal of this lab was to improve visibility into failed logon behavior, identify where suspicious authentication attempts originated, and better understand how Windows security events appear inside a SIEM.

## What This Project Demonstrates
- Active Directory lab setup and log visibility
- Windows authentication event analysis in Splunk
- Detection of repeated failed logon activity
- Correlation of source host and IP address
- Investigation of Windows Event ID 4625
- Hands-on SOC-style troubleshooting and validation

## Lab Goal
Generate authentication failures in a controlled lab environment and verify that:
1. The events are captured correctly
2. Splunk can surface meaningful patterns
3. The source of the activity can be identified quickly
4. Failed logon telemetry can support security investigation workflows

## Environment
- VirtualBox
- Kali Linux
- Windows 10
- Windows Server 2022
- Ubuntu Server 22.04
- Splunk

## Tools Used
- Splunk
- Active Directory
- Windows Event Logs
- Kali Linux
- Crowbar (used in an isolated lab to generate failed authentication activity for detection testing)

## Network Diagram
<p align="center">
  <img src="https://imgur.com/pEdUmkX.png" width="80%" alt="Active Directory and Splunk lab network diagram" />
</p>

## Project Walkthrough

### 1) Build the Lab
I created a small virtualized environment that included:
- A Windows Server domain environment
- A Windows 10 endpoint
- A Kali Linux system to generate test activity
- Splunk for log collection, searching, and visualization

### 2) Generate Failed Authentication Activity
To test visibility, I generated repeated failed logon attempts in the lab. This allowed me to validate whether Splunk was receiving the correct Windows security events and whether the activity could be investigated effectively.

### 3) Investigate in Splunk
Once the events were indexed, I searched for failed authentication activity and analyzed the relevant Windows security logs.

Key focus areas:
- Event ID 4625 (failed logon)
- Number of failed attempts
- Target user account
- Source workstation and IP address
- Event details useful for triage

### 4) Confirm Findings
Through Splunk, I was able to observe:
- A high volume of failed logon events
- Repeated failures associated with a user account
- Source attribution back to the originating system
- Useful event detail for investigation and incident context

## Key Screenshots

### Failed Authentication Activity from Lab System
<p align="center">
  <img src="https://imgur.com/bJR5F1T.png" width="80%" alt="Lab-generated failed authentication activity" />
</p>

### Event ID 4625 Count in Splunk
<p align="center">
  <img src="https://imgur.com/KHPcF6r.png" width="80%" alt="Splunk search showing Event ID 4625 counts" />
</p>

### Repeated Failed Logons for the Account
<p align="center">
  <img src="https://imgur.com/8kX9qj7.png" width="80%" alt="Splunk results showing repeated failed account logons" />
</p>

### Source Host and IP Visibility
<p align="center">
  <img src="https://imgur.com/BKljCZr.png" width="80%" alt="Splunk showing source machine and IP address" />
</p>

### Windows Event 4625 Details
<p align="center">
  <img src="https://imgur.com/YpvjbUe.png" width="80%" alt="Windows Event ID 4625 detail view" />
</p>

## Skills Demonstrated
- SIEM monitoring and investigation
- Log analysis and event correlation
- Windows security event interpretation
- Authentication failure analysis
- Blue-team lab development
- Cybersecurity troubleshooting in virtualized environments

## Key Takeaways
This project helped me strengthen my understanding of:
- How authentication failures appear in Windows logs
- How Splunk can be used to investigate suspicious login behavior
- How repeated failed logons can be identified and contextualized
- Why centralized visibility is important for blue-team operations

## Ethical Use Note
This project was conducted in an isolated home lab for defensive learning, monitoring validation, and security analysis. No activity was performed against unauthorized systems.

## Future Improvements
- Add custom Splunk dashboards for failed logon trends
- Create alerts for repeated authentication failures
- Expand to include successful logons and privilege-related events
- Map detections to security use cases and triage workflows
