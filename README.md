# Project INSIGHT — Unauthorized Access Detection

## Overview
Project INSIGHT is a cybersecurity monitoring and detection project designed to identify and analyze unauthorized access attempts within a network environment. The project focuses on detecting brute-force login attempts, correlating security logs, and monitoring suspicious activities across a segmented network architecture including LAN and DMZ zones.

The implementation leverages security monitoring tools to provide visibility into authentication attempts, abnormal login patterns, and potential intrusion indicators.

---

## Objectives
- Detect unauthorized access attempts targeting critical services.
- Monitor SSH and FTP authentication activities.
- Identify brute-force attacks originating from internal network sources.
- Correlate logs to detect anomalies such as unusual login times and geolocation mismatches.
- Demonstrate network segmentation using a DMZ architecture.
- Provide actionable insights through centralized monitoring.

---

## Project Scenario
An attacker machine located on the LAN (Kali Linux) performed multiple login attempts against an Ubuntu server hosted in the DMZ. The attack targeted SSH and FTP services using the username **admin**, simulating a brute-force attack scenario.

Security monitoring tools detected:
- Repeated failed login attempts.
- Suspicious login patterns.
- Unusual access times.
- Potential geolocation inconsistencies.

---

## Architecture
The environment consists of:

- **Attacker Machine:** Kali Linux (LAN)
- **Target Server:** Ubuntu Server (DMZ)
- **Monitoring System:** Wazuh Manager and Agents
- **Firewall:** Configured to enforce network segmentation
- **Services Monitored:** SSH (Port 22), FTP (Port 21)

---

## Key Components

### 1. Network Segmentation
A DMZ was configured to isolate publicly accessible services from the internal network, reducing risk exposure.

### 2. Log Monitoring
Wazuh agents collected logs from the Ubuntu server, including authentication logs and system events.

### 3. Attack Simulation
Brute-force login attempts were simulated using the attacker machine to test detection capabilities.

### 4. Log Correlation
Security events were correlated to identify abnormal patterns and generate alerts.

---

## Detection Results
- Multiple failed SSH login attempts detected.
- FTP authentication failures logged.
- Alerts triggered for brute-force behavior.
- Identification of suspicious login timing.
- Correlation rules flagged anomalous activity.

---

## Deliverables
- Network diagram with IP addressing scheme.
- Firewall rule documentation.
- Screenshots of monitoring agents running.
- Evidence of detected unauthorized access attempts.
- Analysis report summarizing findings.

---

## Tools and Technologies
- Kali Linux
- Ubuntu Server
- Wazuh SIEM
- OpenSSH
- FTP Service
- UFW Firewall
- Virtualization platform (e.g., VirtualBox or VMware)

---

## How It Works
1. The attacker initiates login attempts against SSH and FTP services.
2. The target server records authentication events.
3. Wazuh agents forward logs to the monitoring server.
4. Correlation rules analyze events and trigger alerts.
5. Security analysts review alerts and investigate.

---

## Security Considerations
- Strong password policies should be enforced.
- SSH key-based authentication is recommended.
- Account lockout policies help mitigate brute-force attacks.
- Firewall rules should restrict unnecessary access.
- Continuous monitoring improves detection capabilities.

---

## Lessons Learned
- Centralized logging significantly improves visibility.
- Network segmentation reduces attack surface.
- Real-time alerting enables faster incident response.
- Attack simulations help validate security controls.

---

## Future Improvements
- Implement multi-factor authentication (MFA).
- Add intrusion prevention capabilities.
- Expand monitoring to additional services.
- Integrate threat intelligence feeds.
- Automate incident response workflows.

---

## Conclusion
Project INSIGHT demonstrates how security monitoring, log correlation, and network segmentation can effectively detect unauthorized access attempts. By simulating real-world attack scenarios, the project highlights the importance of proactive monitoring and layered security controls in defending network infrastructure.

---

## Author
Project Team — Cybersecurity Monitoring Lab

---

## License
This project is intended for educational and research purposes.
