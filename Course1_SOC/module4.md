# SOC Roles

The following figure presents a high-level view of the potential job  roles that are necessary for a SOC. For example, an entry-level analyst  would most likely perform initial triage for alerts that are generated  from a security information and event management tool (SIEM) or an IT  service management (ITSM) ticketing system. After determining that an  alert requires further investigation (based on the SOC’s policies and  workflow procedures), an analyst might escalate the alert to the  investigation team to analyze. The investigation team might collect data  from available tools and perform event correlation on the data to  identify any patterns or relationships. If they determine that more  analysis is necessary, they escalate the alert to a senior member of the  team.  

![image](https://github.com/user-attachments/assets/069dc0b5-2201-4782-90f0-d78b74218874)

The SOC job roles that are identified in the figure are not specifically  defined. Research indicates that SOC-related job roles and  responsibilities within organizations can vary widely. Each organization  might have responsibilities that overlap with other defined roles in a  different organization. Standards have been ineffective at solving this  issue. For example, the NIST NICE workforce framework (Publication—NIST  800-181 Rev.1) identifies the knowledge, skills, and abilities (KSAs) in  the categories of Investigate, Collect and Operate, and Analyze.  However, overlaps might occur in KSAs between the Investigate, and the  Collect and Operate categories across various organizations.  

## SOC Tasks and Responsibilities Overview

A SOC team member helps an organization identify the primary effects of cyberattacks. In short, a SOC analyst works to figure out exactly when, how, and even why an attack was successful. To this end, a SOC analyst reviews evidence of attacks. Such evidence is called an indicator of attack. If an attack is successful, a SOC analyst will then study indicators of compromise to help the organization respond appropriately, as well as make changes so that similar attacks don't happen in the future. All SOC analysts will have a foundation of skills, including device configuration, traffic capture, performance monitoring, and device monitoring. Note that the Tier 1 analyst will play the most heavily in these functions.

### SOC Tier 1 Analyst: Triage Specialist

As the triage specialist, the SOC Tier 1 analyst takes these actions:

![image](https://github.com/user-attachments/assets/04a94c63-2f7f-4109-b2bc-65108be0c412)

#### Note
The SOC Tier 1 analyst role is the entry-level position within the SOC.  The SOC Tier 1 analyst has sysadmin and scripting skills, with one or  more relevant cybersecurity-related certifications (Cisco CyberOPS  Associate, Cisco CCNA, CISSP, CompTIA).  

### SOC Tier 2 Analyst: Incident Handler

The SOC Tier 2 analyst is the incident responder. They will take the following actions: 

- Perform in-depth assessment of incidents escalated by triage specialist.
- Provide attack context through the inclusion of telemetry data not collected by the triage specialist. This may result in discovered actionable threat intelligence to aid in a detection feedback loop through Indicators of Compromise and better rule sets.
- Determine the scope of the attack, the nature of the attack, and the systems affected.
- Decide on a strategy for containment, remediation, and recovery and execute this strategy.
- Decide on a strategy for containment, remediation, and recovery and execute this strategy.
- Escalate to Tier 3 if there are issues encountered.

#### Note

The SOC Tier 2 analyst has a broader and deeper set of skills than the Tier 1  analyst. The Tier 2 analyst analyzes the collected data received from  the triage specialist. 

### SOC Tier 3 Analyst: Incident Responder and Threat Hunter

The SOC Tier 3 analyst is the threat hunter and sometimes also as the subject matter expert. They are the most experienced in the SOC workforce. The threat hunter takes the following actions:

- Proactively identifies threats, security gaps, and unknown vulnerabilities.
- Researches new attack techniques and models threats relevant to the organization. Recommends optimizations and configurations for use in security monitoring tools and assets.
- Aids the other SOC analysts on major incidents. The threat hunter brings key insights, experience, and expertise to incidence response operations.

#### Note

The SOC Tier 3 analyst role is a senior-level position requiring a  considerable breadth of network security knowledge and skills. The Tier 3  analyst has considerable expertise in data analytics and the latest  attack techniques, and will assist Tier 2 incident handlers in their  activities when necessary.  

### SOC Manager

The SOC manager is responsible for the following:

- Managing the security team, including hiring, training, and evaluating team members.
- Assessing incident reports.
- Developing and implementing crisis communication procedures:
- Oversees the financial aspects.
- Supports security audits.

The SOC manager reports to the Chief Information Security Officer (CISO).

## SOC Tools
The SOC team uses various tools for different activities. Some of the tools that make up their toolkit include the following:

### IT Service Management (ITSM)  
system is a set of workflow tools that collects and manages incident  data from security tools and devices into a structured automated  workflow that assists the SOC with prioritizing threats. An example of a  popular ITSM is ServiceNow.

### Security and Information Event Management System (SIEM)
Provides  real-time monitoring, analysis, and logging of events. Provides User  and Entity Behavior Analytics (UEBA) via artificial intelligence (AI)  and machine learning technologies. Splunk is an example of a popular  SIEM.

### Intrusion Detection System (IDS) / Intrusion Prevention System (IPS)
Monitors  networks for malicious activity or policy violations. An IDS will  provide an alert to the SOC analyst on a potential incident. An IPS will  provide an alert to the analyst and will take additional remediation  actions to block the intrusion to minimize damage. An IDS is usually  classified as either Network Intrusion Detection Systems (NIDS) or Host  Intrusion Detection Systems (HIDS). A NIDS will monitor network traffic  for harmful or abnormal behavior. An HIDS will monitor a single device  or host for harmful or abnormal behavior. Cisco Firepower 4100 Series is  an example of an appliance with NIDS/IPS functionality and Cisco Secure  Endpoint is an example of an HIDS/IPS.

### Vulnerability scanner  
Application designed to assess computers, networks, or  applications for known weaknesses. They identify vulnerabilities  resulting from device misconfigurations, software flaws, and missing  software patches that may be present in devices such as firewalls,  routers, and servers, and endpoint devices. Nessus is an example of a  popular vulnerability scan application.

### Threat Intelligence service
Threat Intelligence service collects, processes, analyzes, and disseminates threat information and  responds to activities that pose a threat to applications and systems.  Threat Intelligence collects vulnerability and exploit information in  real time, compiles into a single database, and disseminates it to  consumers of the service. Cisco Talos is one of the largest providers of  security threat intelligence.

## Before, During, and After Incidents

During the day, the SOC analyst typically  focuses on monitoring. When an incident occurs, the SOC analyst’s  attention turns to incident response and to some of the available tools.  The SOC must coordinate with the stakeholders during the incident.  Working with the network operations center (NOC), system owners, and  data owners can improve the outcome.

The  SOC Tier 1 triage specialist focuses on the ITSM ticketing system to  monitor alerts. The threat hunter focuses on the Cisco Talos threat  intelligence feeds.

Note: The SOC coordinates with various stakeholders during the incident, including the NOC, human resources, and the legal department.

![image](https://github.com/user-attachments/assets/b904eb92-37e8-4b7c-9151-370908181b98)

After an incident is resolved, the SOC begins its recovery phase. They work closely with the legal department to make sure all procedures are documented and will hold up in court proceedings. Reports are created that detail findings and lessons learned. The SOC analysts take the following steps in the post-incident phase:

- Use  forensics applications, such as Encase, Velociraptor, or Redline, to  collect, analyze, and create reports. Also, take steps to help ensure  legal compliance for potential court procedures.
- Consider using a SOC 2 audit report to show organizational and legal compliance.
- Generate multiple reports that will serve as lessons learned for future SOC incident response activities.

## Wrap Up

You now know the roles and responsibilities of the prominent SOC team members. And you know the interactions between these members based on an incident response activity that you analyzed. Each soc analyst member has multiple roles and responsibilities and interacts with the other team members in multiple ways based on the responsibility they're carrying out. 
A good example of this, is incidents response procedures. We encourage you to consider your online work activities and determine how you can help the soc improve your company's security posture. And now that you are better versed in the roles and responsibilities of each soc member, you now may have a clear view of what soc role may be appropriate for you now and in the future.
