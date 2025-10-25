# Security-Log-Analysis-and-Monitoring-Project-on-Mac-OS

**Tools:** Splunk, Universal Forwarder, Mac Log Files 

**Project goal:** Security Log Analysis, Endpoint Monitoring

**Project Goal & Scope**
_Primary Objective_: Establish robust, consistent, and validated ingestion of endpoint security logs (Unified Log System and Audit Logs) into a Splunk instance.

_Analytical Goal_: Develop specific Splunk Search Processing Language (SPL) queries to isolate and identify patterns indicative of unauthorized access attempts and security misconfigurations.

_Target Skills_: Demonstrating proficiency in SIEM fundamentals, configuration management, analytical problem-solving, and contributing to the initial phases of Incident Management.

**Technologies Utilized**
- _SIEM Platform_ | Splunk Enterprise (Free/Dev License) | Log aggregation, parsing, indexing, and visualization.
- _Operating System_ | macOS (Endpoint) & Ubuntu VM (Splunk Host) | Source endpoint for log data; target host for the SIEM platform.
- _Query Language_ | Splunk SPL |  Executing targeted Threat Detection analysis.

**Implementation and Configuration Highlights**
The success of this project hinged on identifying the precise log locations and creating specific parsing rules to ensure the raw data was usable for analytical security monitoring.

A. _Log Source Identification and Data Ingestion_
The initial phase involved manually identifying the specific file paths for critical macOS security data (Audit Logs and the Unified Log Stream) and examining their raw structure to define the ingestion strategy.

**Action**: Configured Splunk's built-in File Monitoring Input to point to the precise locations of these logs, demonstrating the ability to manually map log sources into the SIEM environment for endpoint security monitoring.

B. _Data Normalization and Parsing for SIEM Readiness_
To make the raw, unstructured logs actionable for SIEM analysis, a crucial normalization step was performed. This process familiarized me with enterprise SIEM log schemas and the need for data structure.

Action: Created custom parsing rules in props.conf and transforms.conf to properly assign source types and perform field extractions. This guaranteed that important fields (e.g., user, action, outcome) were reliably indexed, which is crucial for security analysis.

C. _Analytical Dashboarding and Proactive Alert Creation_
The final stage involved operationalizing the ingested data into a usable security monitoring environment for continuous Threat Detection.

_Dashboard Creation_: Successfully designed and launched a Splunk Dashboard to provide clear visualization of key security metrics (e.g., login trends and critical user activity) for easy, high-level oversight.

_Alert Implementation_: Developed a basic real-time alert based on analytical findings (e.g., triggering on a high threshold of failed login attempts). This simulates a proactive incident management workflow and notifies administrators of potential threats.

**Key Analytical Findings (Threat Detection)** 
Using the configured Splunk pipeline, I performed targeted analysis for Threat Detection. While some security events were isolated, a core challenge demonstrated the importance of understanding endpoint security hardening:

Brute-Force Attack Attempt: 
su invaliduser | this prompts for a password, and I enter a random password. 

**Adaptation and Discovery**:
Running the command above, I was unable to observe any effect from this brute-force attack even after waiting a few hours for it to appear. This failure led me to research macOS security architecture, confirming the existence of built-in account lockout mechanisms that countered the simple attack method. I am now exploring alternative, more complex attack simulation techniques to generate the necessary log data for analysis.

**Conclusion: Skill Validation**:
_Analytical Problem-Solving_: Demonstrated the ability to debug analytical failures (e.g., failed brute-force detection), research the underlying cause (macOS hardening), and find alternative solutions.

_SIEM Proficiency_: Hands-on experience with the entire log lifecycle (log sourcing, parsing, indexing, and visualization).

_Threat Detection & Incident Response_: Ability to develop and execute targeted queries to identify security events and formulate initial incident management actions.

_Configuration Management_: Practical knowledge of configuring Splunk inputs and parsing rules for consistent data collection and readiness.

_Log Parsing & Normalization_: Deep familiarity with transforming raw logs into actionable security data.

How to Run/View
- Clone this repository.
- Review the ReadMe
- Full Project Report: Detailed Case Study

