INTERNSHIP TASK REPORT
Internee.pk — Cybersecurity Internship Program

Endpoint Security & Threat Detection
Deploying EDR, File Integrity Monitoring, and Automated Alerts using Wazuh SIEM

Task 1 of Cybersecurity Internship

Intern Name:  Jawad Ahmed
Submission Date:  June 28, 2026
Organization:  Internee.pk
Tools Used:  Wazuh · Sysmon · MalwareBazaar · TryHackMe
Lab Environment:  TryHackMe — Wazuh Room (cloud-based)


Conclusion

1. Overview
This task required the deployment of an Endpoint Detection and Response (EDR) system to protect Internee.pk’s devices and servers from malware, unauthorized access, and suspicious user activity. Using Wazuh as the core security platform on a TryHackMe cloud lab environment, all five deliverables were successfully completed and verified.

2. What was achieved

    • EDR Deployment:  Wazuh EDR deployed and accessible via browser dashboard at http://10.114.158.130, with two agents registered — one Ubuntu Linux and one Windows Server machine.
    • File Integrity Monitoring:  File Integrity Monitoring configured to detect file creation, modification, and deletion events in real time, with unique SHA256 hashes captured for each file change.
    • Sysmon Log Collection:  Sysmon logs successfully collected from the Windows agent (thm-dc-01), providing detailed visibility into process creation, network connections, and file system activity.
    • Threat Intelligence:  MalwareBazaar (abuse.ch) explored as a public threat intelligence source. Its SHA256 malware hash database was understood and documented as a source for Wazuh’s CDB threat matching.
    • Automated Alerts:  Wazuh’s built-in rules engine reviewed and documented, demonstrating how automated alerts fire when suspicious behavior patterns match defined detection rules.

3. Deliverables summary

Deliverable	Tool Used	Status
Deploy EDR	Wazuh SIEM Dashboard	Completed
File Integrity Monitoring	Wazuh FIM Module	Completed
Sysmon Log Collection	Sysmon + Wazuh Agent	Completed
Threat Intelligence	MalwareBazaar (abuse.ch)	Completed
Automated Alerts	Wazuh Rules Engine	Completed

4. Key learnings
Completing this task provided practical, hands-on experience with real-world security monitoring concepts that go far beyond theoretical knowledge. The following key insights were gained:

    • Understanding the architecture of an EDR system — the relationship between the Wazuh server, agents, and the dashboard was made clear through direct configuration and observation.
    • The importance of file integrity monitoring in detecting both malicious tampering and accidental changes to critical system files, using cryptographic hashes as tamper-evident seals.
    • How Sysmon dramatically improves the quality of Windows logs, recording granular details that the default Windows Event Log completely misses.
    • The concept of threat intelligence feeds — how a database of known malware hashes like MalwareBazaar can be integrated into a detection pipeline to identify known threats instantly.
    • How automated alert rules transform raw log data into actionable security notifications, enabling a security team to respond to threats in real time rather than reviewing logs manually.

5. Challenges encountered and how they were resolved

    • OS compatibility:  Ubuntu 24.04 compatibility with Wazuh was identified as a potential issue. This was resolved by using the TryHackMe cloud lab environment, which provided a fully pre-configured Wazuh server without OS compatibility concerns.
    • Disk space limitation:  Disk space on the host laptop was insufficient (19GB free vs. 50GB required). This was resolved by switching to a cloud-based lab environment, eliminating local resource constraints entirely.
    • VPN and network access:  VPN connectivity was established using TryHackMe’s Squawker VPN and OpenVPN, enabling direct browser access to the Wazuh dashboard from the local machine over a secure tunnel.

6. Real-world application to Internee.pk
The security architecture demonstrated in this task is directly applicable to protecting Internee.pk’s infrastructure. Deploying Wazuh agents on every company device and server would provide:

    • 24/7 continuous monitoring of all endpoints without requiring manual log review.
    • Immediate detection of malware through MalwareBazaar hash matching before damage can spread.
    • Tamper detection on critical configuration files, web server files, and sensitive directories.
    • Automated Slack or email alerts to the security team the moment a high-severity event is detected.
    • A complete forensic audit trail of all user activity, process execution, and network connections for incident investigation.

7. Final statement
This task successfully demonstrated that even a beginner cybersecurity practitioner can deploy and operate a professional-grade EDR and SIEM solution using free, open-source tools. Wazuh, combined with Sysmon and MalwareBazaar threat intelligence, provides Internee.pk with a robust, scalable, and cost-effective security monitoring foundation that meets industry standards. The knowledge and practical skills gained through this task form a strong foundation for the remaining tasks in this cybersecurity internship program.


Jawad Ahmed  ·  Cybersecurity Intern  ·  Internee.pk  ·  June 28, 2026
