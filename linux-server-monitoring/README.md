# Linux Server & Monitoring Infrastructure

## Overview

Hands-on experience in Linux server administration, service deployment, container management, and network monitoring infrastructure for ISP operations.

This project highlights practical experience maintaining Linux-based services and supporting reliable monitoring systems in a production ISP environment.

## Technical Skills

- **Operating Systems:** Ubuntu Server, Linux administration
- **Containerization:** Docker, Docker Compose
- **Network Monitoring:** LibreNMS, SNMP, device and interface monitoring
- **Automation:** Bash scripting, scheduled tasks, service automation
- **Alerting:** Telegram notifications and n8n workflow integration
- **Web Services:** Nginx, web-based monitoring interfaces
- **Database Services:** MariaDB, Redis
- **Troubleshooting:** Service failures, logs, resource usage, connectivity, and port conflicts

## Key Responsibilities

### 1. Linux Server Administration
- Manage Linux servers and essential system services.
- Monitor CPU, memory, disk usage, uptime, and system health.
- Troubleshoot service failures and network connectivity issues.
- Review system logs to investigate operational problems.

### 2. Docker Infrastructure
- Deploy and maintain containerized applications.
- Manage Docker Compose services, container logs, and restart policies.
- Troubleshoot container networking, port mappings, and service dependencies.
- Perform controlled updates while minimizing service disruption.

### 3. Monitoring Infrastructure
- Operate LibreNMS for network device and interface monitoring.
- Configure SNMP-based monitoring for supported network equipment.
- Monitor device availability, interface traffic, CPU, memory, and optical sensors where supported.
- Integrate monitoring events with notification workflows.

### 4. Alerting and Automation
- Integrate Telegram notifications for operational alerts.
- Use n8n to build automation workflows where appropriate.
- Investigate alert conditions and validate notifications.
- Automate repetitive administrative tasks using shell commands and scripts.

### 5. Troubleshooting and Reliability
- Analyze Linux service logs and resource utilization.
- Investigate application startup failures and port conflicts.
- Validate service availability after configuration changes.
- Use backups, change control, and rollback procedures to reduce operational risk.

## Example Infrastructure Workflow

```text
Linux Server
    |
    +-- Docker / Docker Compose
    |      |
    |      +-- Monitoring Services
    |      +-- Supporting Applications
    |
    +-- System Logs and Resource Monitoring
    |
    +-- LibreNMS
    |      |
    |      +-- SNMP Monitoring
    |      +-- Network Alerts
    |
    +-- n8n Automation
           |
           +-- Telegram Notifications
```

*This diagram illustrates a logical workflow, not a complete production network diagram.*

## Operational Approach

- Follow least-privilege access principles.
- Keep credentials, tokens, and private configuration out of public repositories.
- Validate changes before applying them to production.
- Monitor services after upgrades and configuration changes.
- Maintain documented troubleshooting and recovery procedures.

## Professional Focus

Linux Server Administration | Docker | LibreNMS | SNMP | Network Monitoring | Bash Scripting | Automation | ISP Infrastructure

## Disclaimer

This repository documents technical skills and representative infrastructure workflows. Sensitive production configurations, credentials, customer information, and private network details are intentionally excluded.
