# Hi there, I'm Idris Lawan Mustapha 👋

<div align="center">

  ### 🛡️ SOC Analyst | Threat Detection Engineer | Cloud SIEM & Blue Team Operations

  [![B.Sc. Cybersecurity](https://img.shields.io/badge/Degree-B.Sc._Cybersecurity-0052CC?style=for-the-badge&logo=academic-cap&logoColor=white)](https://buk.edu.ng)
  [![Google Cybersecurity Certified](https://img.shields.io/badge/Certification-Google_Cybersecurity_Professional-4285F4?style=for-the-badge&logo=google&logoColor=white)](https://coursera.org)
  [![Splunk Cloud](https://img.shields.io/badge/SIEM-Splunk_Cloud_Platform-000000?style=for-the-badge&logo=splunk&logoColor=white)](https://splunk.com)
  [![Wazuh SIEM / XDR](https://img.shields.io/badge/SIEM-Wazuh_SIEM%2FXDR-007ACC?style=for-the-badge&logo=wazuh&logoColor=white)](https://wazuh.com)
  [![MITRE ATT&CK](https://img.shields.io/badge/Framework-MITRE_ATT%26CK-FF6F00?style=for-the-badge&logo=matrix&logoColor=white)](https://attack.mitre.org)
  [![LinkedIn](https://img.shields.io/badge/LinkedIn-Connect-0A66C2?style=for-the-badge&logo=linkedin&logoColor=white)](https://linkedin.com/in/idris-mustapha-l)
  [![Email](https://img.shields.io/badge/Email-Contact_Me-EA4335?style=for-the-badge&logo=gmail&logoColor=white)](mailto:idreesmustpher@gmail.com)

</div>

---

## 👨‍💻 Professional Summary

Security Operations Center (**SOC**) Analyst and Threat Detection Engineer with hands-on experience in **security monitoring, detection engineering, incident investigation, and 24/7 NOC network operations** across enterprise lab and production environments.

Holds a **B.Sc. in Cybersecurity** (Bayero University Kano) and the **Google Cybersecurity Professional Certificate**, with verified expertise across enterprise SIEM platforms—including **Splunk Cloud Platform** and **Wazuh SIEM/XDR**. Experienced in ingesting kernel-level **Sysmon telemetry** via mTLS, conducting **detection gap analyses**, engineering custom **SPL and XML detection rules** for ransomware staging (MITRE T1490), building production **SOC operations dashboards**, authoring formal incident response reports, and maintaining high availability for VoIP and ISP infrastructure under strict enterprise SLAs.

- 🎯 **Target Roles**: SOC Analyst (Tier 1 / Tier 2) | Detection Engineer | Blue Team Specialist | Cloud Security Analyst
- 📍 **Location**: Kano, Nigeria (Open to Remote Globally & Relocation)
- 🎓 **Education**: B.Sc. Cybersecurity — Bayero University Kano
- 📜 **Certifications**: Google Cybersecurity Professional, Cisco Ethical Hacker, Cisco Networking Basics, Cisco Intro to Cybersecurity
- 📂 **Main Portfolio Repository**: [github.com/fikira001/cybersecurity-portfolio](https://github.com/fikira001/cybersecurity-portfolio)

---

## 🚀 Technical Skills & Frameworks

| Category | Technologies, Tools & Frameworks |
| :--- | :--- |
| **SIEM & Analytics Platforms** | **Splunk Cloud Platform** (SPL, Alert Manager, Classic XML Dashboards), **Wazuh SIEM/XDR** (OSSEC XML Rules, Wazuh Indexer & Dashboard), Elastic Stack (ELK) |
| **Endpoint Telemetry & Ingestion** | **Microsoft Sysmon v15** (SwiftOnSecurity Schema), **Splunk Universal Forwarder v10.4.3** (mTLS Ingestion), Windows Event Logs (`Security.evtx`, `System.evtx`, `Sysmon/Operational`) |
| **Detection Engineering** | Search Processing Language (**SPL**), **PCRE2 Regular Expressions**, **XML Detection Rules**, Detection Gap Analysis, False Positive Tuning |
| **Security Operations & Blue Team** | Threat Hunting, Incident Response Triage, IOC Extraction & Analysis, Forensic Timeline Reconstruction, Incident Reporting |
| **Adversary Simulation** | **Kali Linux**, **Parrot OS**, **Metasploit Framework**, Msfvenom, Nmap, PowerShell Empire |
| **Networking & Protocols** | TCP/IP, DNS, DHCP, HTTP/HTTPS, FTTH, GPON, **VoIP, SIP**, Routing & Switching, Wireshark, Packet Analysis |
| **Programming & Scripting** | **Python**, **SQL**, **Bash**, **PowerShell**, Linux CLI |
| **Security Frameworks** | **MITRE ATT&CK Framework**, NIST Cybersecurity Framework (CSF), NIST SP 800-61, Cyber Kill Chain, CIA Triad |

---

## 🛡️ Featured Enterprise Security Projects

### ☁️ 1. [Enterprise Splunk Cloud SOC & Detection Engineering Lab](https://github.com/fikira001/cybersecurity-portfolio/tree/main/splunk-cloud-soc-lab)
> **Stack:** Splunk Cloud Platform • Splunk Universal Forwarder v10.4.3 • Sysmon v15 • Parrot OS • Windows 10 • MITRE ATT&CK

* **Cloud Telemetry Pipeline:** Configured Splunk Universal Forwarder on Windows 10 with tenant private CA certificates (`splunkclouduf.spl`) streaming encrypted Sysmon XML logs over mTLS to an enterprise Splunk Cloud tenant (`prd-p-o1pgk.splunkcloud.com`).
* **Full Attack Lifecycle Simulation:** Executed an end-to-end adversary simulation from Parrot OS covering Nmap port sweeping (`T1046`), dropped payload execution from `C:\Users\Public` (`T1204.002`), Meterpreter reverse TCP C2 (`T1571`), PowerShell defense evasion (`T1059.001`, `T1562.001`), SYSTEM privilege escalation (`T1134`), SAM credential harvesting (`T1003`), and Volume Shadow Copy deletion (`T1490`).
* **Detection Engineering (SPL):** Engineered **6 production SPL detection rules** utilizing PCRE regex extraction on `_raw` XML telemetry with false positive analysis and tuning.
* **Alert Automation:** Deployed **5 scheduled alerts** in Splunk Cloud Alert Manager with automated trigger actions, validating live alert firings for ransomware pre-staging and payload execution.
* **SOC Operations Dashboard & Reporting:** Built a centralized 6-panel dark-mode Splunk Classic XML dashboard and authored formal executive documentation: [IR-SPLUNK-2026-001.pdf](https://github.com/fikira001/cybersecurity-portfolio/blob/main/splunk-cloud-soc-lab/docs/INCIDENT_REPORT.pdf).

---

### 🔬 2. [Enterprise SOC Detection Lab: Wazuh SIEM/XDR Ransomware Simulation](https://github.com/fikira001/cybersecurity-portfolio/tree/main/wazuh-detection-lab)
> **Stack:** Wazuh SIEM/XDR v4.14.5 • Sysmon v15 • Windows 10 Enterprise • Kali Linux • VMware Workstation

* **Endpoint Telemetry & Ingestion:** Ingested enriched Sysmon Event ID 1 process creation logs into Wazuh Manager on an isolated VMware virtual network.
* **Detection Gap Analysis:** Demonstrated that default Wazuh rules dropped administrative utilities below alerting thresholds, creating a critical visibility gap for ransomware preparation steps.
* **Custom XML Detection Rules:** Authored **3 custom XML detection rules** (Rules `100001`–`100003`) escalating `vssadmin`, `bcdedit`, and `wbadmin` recovery inhibition commands to **Level 12 Critical** alerts mapped directly to MITRE ATT&CK `T1490`.
* **Forensic Documentation:** Correlated IOCs and authored formal executive Incident Report: [INCIDENT_REPORT.pdf](https://github.com/fikira001/cybersecurity-portfolio/blob/main/wazuh-detection-lab/docs/INCIDENT_REPORT.pdf).

---

### 🔒 3. [SME-Guard — AI-Powered Cybersecurity Awareness Platform](https://github.com/fikira001/sme-guard)
> **Stack:** React JS • Firebase • Python • Generative AI

* **Secure Authentication & RBAC:** Implemented secure user authentication and Role-Based Access Control (RBAC) via Firebase Authentication.
* **Interactive Threat Training:** Developed modules training users against phishing, ransomware execution, credential hygiene, and social engineering.
* **AI Training Integration:** Integrated Generative AI to deliver adaptive, personalized cybersecurity awareness scenarios for small-to-medium businesses.

---

### 🎓 4. [Google Cybersecurity Professional Portfolio](https://github.com/fikira001/cybersecurity-portfolio/tree/main/google-cybersecurity)
> **Stack:** Linux CLI • Python • SQL • Wireshark • NIST CSF

* Practical implementations of security audits against NIST CSF, incident response playbooks, Linux file permission administration, and SQL filtering for security investigations.

---

## 💼 Professional Security & Network Experience

### 📞 Network Operations Center (NOC) Support Engineer
**Ratel Plus Nigeria Ltd.** | *Kano, Nigeria* | *2026 – Present*
- Monitor and support enterprise Voice over IP (VoIP) and SIP infrastructure to ensure high service availability under strict SLAs.
- Investigate VoIP degradation, call quality anomalies, SIP registration drops, and network connectivity faults.
- Perform first-level incident investigation, triage, and escalation following operational runbooks.
- Proactively track network device health and operational alerts to prevent infrastructure downtime.
- Author Root Cause Analysis (RCA) and incident post-mortems for continuous service improvement.

### 🛰️ Network Operations Center (NOC) Intern
**BrowsePoint Telecommunications & ISP** | *Kano, Nigeria* | *Nov 2024 – May 2025*
- Monitored FTTH (Fiber-to-the-Home) and wireless radio network infrastructure in a 24/7 ISP Network Operations Center.
- Investigated fiber cuts, link degradation, GPON backhaul faults, and customer connectivity issues using network monitoring suites.
- Executed first-level triage and escalated high-priority outages to senior network engineers per SLA policies.

### 💻 IT & Systems Assistant
**Startbench Limited** | *Kano, Nigeria* | *2023 – 2024*
- Managed endpoint configuration, software deployment, Windows system administration, and technical issue resolution.

### ⚙️ IT Support Assistant
**Sab Ventures Computer Services** | *Kano, Nigeria* | *2017 – 2021*
- Installed, configured, and maintained Windows workstations, network peripherals, and endpoint security applications.

---

## 🎓 Education & Industry Certifications

### 📜 Industry Certifications & Credentials
- 🏅 **Google Cybersecurity Professional Certificate** — Coursera / Google
- 🛡️ **Ethical Hacker Course** — Cisco Networking Academy
- 🌐 **Networking Basics** — Cisco Networking Academy
- 🔒 **Introduction to Cybersecurity** — Cisco Networking Academy

### 🏛️ Academic Education
- 🎓 **B.Sc. in Cybersecurity** — Bayero University Kano (*2021 – 2026*)
- 💻 **Computer Science Program** — Citadel Center for Learning Computer (*2018 – 2019*)

---

## 📊 GitHub & Core Focus

<div align="center">

  [![GitHub Profile](https://img.shields.io/badge/GitHub-fikira001-181717?style=for-the-badge&logo=github&logoColor=white)](https://github.com/fikira001)
  [![Security Operations](https://img.shields.io/badge/Focus-SOC_Operations-0052CC?style=for-the-badge&logo=shield&logoColor=white)](https://github.com/fikira001/cybersecurity-portfolio)
  [![Detection Engineering](https://img.shields.io/badge/Domain-Detection_Engineering-FF6F00?style=for-the-badge&logo=matrix&logoColor=white)](https://github.com/fikira001/cybersecurity-portfolio)
  [![Splunk Cloud](https://img.shields.io/badge/SIEM-Splunk_Cloud-000000?style=for-the-badge&logo=splunk&logoColor=white)](https://github.com/fikira001/cybersecurity-portfolio/tree/main/splunk-cloud-soc-lab)
  [![Wazuh XDR](https://img.shields.io/badge/SIEM-Wazuh_XDR-007ACC?style=for-the-badge&logo=wazuh&logoColor=white)](https://github.com/fikira001/cybersecurity-portfolio/tree/main/wazuh-detection-lab)

  <br/>

  [![Python](https://img.shields.io/badge/Python-Automation_&_Scripting-3776AB?style=for-the-badge&logo=python&logoColor=white)](https://python.org)
  [![SPL](https://img.shields.io/badge/Query_Language-SPL-black?style=for-the-badge&logo=splunk&logoColor=white)](https://splunk.com)
  [![Linux](https://img.shields.io/badge/Linux-Ubuntu_%26_Kali-FCC624?style=for-the-badge&logo=linux&logoColor=black)](https://linux.org)
  [![Networking](https://img.shields.io/badge/Networking-NOC_%26_VoIP%2FSIP-1BA0D7?style=for-the-badge&logo=cisco&logoColor=white)](https://netacad.com)

</div>

---

## 📫 Let's Connect!

- 📧 **Email**: [idreesmustpher@gmail.com](mailto:idreesmustpher@gmail.com)
- 💼 **LinkedIn**: [linkedin.com/in/idris-mustapha-l](https://linkedin.com/in/idris-mustapha-l)
- 🌐 **GitHub**: [github.com/fikira001](https://github.com/fikira001)
- 📂 **Portfolio**: [github.com/fikira001/cybersecurity-portfolio](https://github.com/fikira001/cybersecurity-portfolio)

<div align="center">
  <sub><i>"Security is not a product, but a process." — Bruce Schneier</i></sub>
</div>
