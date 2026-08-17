# SOC Home Lab Architecture

## Objective

Build a small SOC environment where I can collect Windows security logs,
detect suspicious activity, investigate alerts, and document incidents.

## Planned Components

### 1. Windows Endpoint
Purpose:
- Act as the monitored workstation
- Generate Windows security logs
- Run Sysmon for additional telemetry

Planned software:
- Windows 10/11
- Sysmon
- Wazuh Agent

### 2. Wazuh SIEM Server
Purpose:
- Receive logs from the Windows endpoint
- Monitor security events
- Generate alerts
- Allow investigation through the Wazuh dashboard

### 3. Attack / Testing Machine
Purpose:
- Generate controlled suspicious activity
- Test whether the SIEM detects attacks

Possible OS:
- Kali Linux

## Data Flow

Windows Endpoint
      |
      | Security Logs + Sysmon Events
      v
Wazuh Agent
      |
      v
Wazuh SIEM Server
      |
      v
Alerts / Detection
      |
      v
SOC Investigation

## Planned Detection Scenarios

- Multiple failed login attempts
- Suspicious PowerShell activity
- User account changes
- Suspicious process execution
- Network scanning

## Current Status

Architecture planning.
