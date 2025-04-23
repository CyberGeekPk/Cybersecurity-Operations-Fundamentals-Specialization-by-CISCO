# Understanding SOC Workflow & Automation

- Use of a workflow management system and automation to improve the effectiveness of the SOC
- Describe SOC WMS concepts.
- Describe how a typical workflow management system is integrated within a SOC
- Describe SOC WMS integration
- Provide an example of SOC workflow automation

##  Learning Objectives

- Describe SOC WMS concepts.
- Describe how a typical workflow management system is integrated within a SOC.
- Describe SOC WMS integration.
- Provide an example of SOC workflow automation. 

## SOC WMS Concepts

A security analyst needs to look at many logs for security and networking tools. Traditionally, analysts must log in many different security and networking devices to review and analyze logs for security incidents. With each log, an analyst needs to review events that are being produced at a rate of a hundred events per hour, or per minute, or possibly per second. It is very difficult for the analyst to effectively analyze all the events without the help of some automation.

Many networking and security logs can be consolidated into a syslog server so that the security analyst can review logs in one place, without having to log in to numerous devices. A syslog server makes it easier for the analyst to manipulate and review logs. However, significant problems still arise when correlating similar events between devices: the logs are not in the same format and do not contain the same types of data; date and times can look different; computer names use different formats; some logs will not have system names or domain names or IP addresses and MAC addresses may or may not be included.

In the last 10 years or so, SIEM security devices have come on the market and greatly changed the way that incidents are identified. When a possible incident is identified, it might take several hours to research by connecting to other security, networking device, and endless endpoints. Analysts would need to be skilled in the use of several of the different devices and have a good understanding of the network, including understanding the path that each type of packet would take through the network and from which device to retrieve logs. With introduction of SIEM, many (if not all) logs from the security and networking devices and endpoints go directly into SIEM. SIEMs are designed to “ingest” logs: The logs are aggregated and normalized.

The role of the security analyst is to follow the established workflow to ensure that incidents are processed efficiently and in the same way. Many repeatable job tasks can be automated to improve the SOC efficiency. 

## Definition of WMS

A WMS is software that tags and identifies an existing security event, tracks the event, and tracks the actions that are taken in dealing with those events, from detection to response to mitigation to ticketing closure.

A WMS is a platform for orchestrating and automating incident response processes. In simple terms, a WMS automates the remediation of a malicious action. It performs containment and eradication. A WMS does not identify incidents, collect evidence, or help with approvals, which are features of SIEM and a ticketing system. As seen in the following figure, the process begins in SIEM and then moves to the security WMS followed by the individual security devices

NOTE: The term WMS can identify this type of system implementation in any environment. In the context of a SOC, the term security operations, analysis, and reporting (SOAR) can be used; however, vendors have not standardized on a specific acronym. For example, Swimlane dubs its WMS as a security operations orchestration and automation platform.

![image](https://github.com/user-attachments/assets/97f8f4e7-1cb2-402c-ad16-0096b7125b1f)

After a ticket has been created or SIEM has identified an incident, the Tier 1 analyst has collected supporting evidence, and a higher-level tier analyst has confirmed that it is an incident, the security WMS gets involved.

## Workflow Types

A SOC uses workflows to coordinate tasks between people and synchronize data between different systems, with the ultimate goal of improving SOC efficiency and responsiveness.

There are three types of workflows:

- Sequential: A sequential workflow is typically flow chart-based. It progresses from one stage to the next and does not step backward.
- State machine: A state machine workflow progresses from state to state. It is more complex and can return to a previous point if required.
- Rules-driven: Implementation of a rules-driven workflow is based on a sequential workflow. The rules dictate the progress of the workflow.

A workflow can be described simply as the ordered execution of tasks through a well-defined and structured process. Workflows can be a sequential progression of work activities or a complex set of processes each taking place concurrently and eventually affecting each other according to a set of rules and roles. The WMS defines and controls the various tasks and activities that are associated with a process. In addition, many management systems can also measure and analyze the execution of the process so that continuous improvements can be made. The SOC management team develops the workflow model that implements the standardized operating procedures for the incident handling process. The workflow model guides the SOC analysts through the triage and response procedures. 

## Incident Response Workflow

Maintaining consistency within an incident response process is very important. A defined incident response process articulates how a particular incident is to be handled based on its severity. The key to a sound and robust incident response process is to ensure that all incident severity levels have a defined response process. Also, as an incident is handled, the severity of that incident may change over time. The severity of an incident may be lowered, particularly when an incident is being monitored after remediation. The incident response process should have appropriate procedures in place to identify how an incident should be handled when the severity of the incident is changed from one level to another. 

During an incident response, it is also important to ensure consistent and timely reporting. Each incident severity type would have defined times for notification, constant reporting until an incident is remediated, and monitoring and reporting on the incident after remediation. At times, incident investigators are responsible for the consistent and timely reporting of an incident. As staff work shifts end, these activities are usually handed off to the person on the next shift. Because of the manual nature of this involvement, there are opportunities for investigators to miss reporting targets.

A SOC WMS can automate these types of activities, reducing manual intervention within the incident response process and in ensuring consistent and timely reporting. A SOC WMS can also generate alerts when a certain reporting period is passed, to inform the investigators or confirm if the report for that time period has been acted on.

## Incident Response Workflow Roles

Within a SOC, there are varying degrees of specialized individuals who are highly trained in the functions that they perform. The figure presents a conceptual overview of the SOC workflow that is focused on the different roles. Organizations will customize their workflow, which is based on their particular situation.

![image](https://github.com/user-attachments/assets/30e17e84-c28b-456a-b775-8dae8d25cdd2)

Depending on how the particular SOC is organized, various tiers of security analysts and teams may be involved in the workflow. For example, security analysts may be more involved in the detect and triage stages, while the CSIRT team members may be more involved in the respond stage. Each organization may embed a different variation of a SOC. The following roles would often be found within a SOC:

- ### Tier 1 analyst

Continuously monitors the alert queue; triages security alerts; monitors health of security sensors and endpoints; collects data and context necessary to initiate Tier 2 work

- ### Tier 2 analyst

Performs deep-dive incident analysis by correlating data from various sources; determines if a critical system or data set has been affected; advises on remediation; provides support for new analytic methods for detecting threats

- ### Incident response handler

Manages the incident; executes containment strategies and ensures that the incident response process is followed throughout; at times, may also communicate with the business to provide periodic updates

- ### Forensics specialists

Focused on gathering, retaining, and analyzing computer-related data for investigative purposes, in a manner that maintains the integrity of the data

- ### Malware reverse engineering specialists

Analyze the malware behaviors in depth to determine the relevant tactics, techniques, and procedures, and the indicators of compromise. May also write signatures to detect, hunt, and prevent the malware

- ### SOC management

Manages resources to include personnel, budget, shift scheduling, and technology strategy to meet SLAs; communicates with management; serves as the organizational point person for business-critical incidents

- ### Executive

Provides overall direction of the SOC; ensures that the SOC is achieving and maintaining the objectives that have been defined

## SOC WMS Integration Overeview

The traditional, manual processes that SOCs  currently use to perform remediation have left security teams  struggling to keep up with an ever-increasing volume of work. The WMS is  the latest technology in the SOC environment, specifically concerning  remediation. The primary mission of the WMS is to remediate an incident  autonomously, so the WMS needs to receive security events and alerts  information from SIEM and then push information or commands to security  devices. The security device then executes a procedure or configuration  to either remediate or contain some malicious action.

Processes and workflows under the SOC responsibilities may include the following:

- Cybersecurity incident management
- Vulnerability management
- Threat intelligence and hunting
- Network security monitoring and detection
- Governance and compliance management
- Physical security and physical threat management

## SOC WMS Integration

To improve efficiency of SOC operations, the WMS is also typically integrated with SIEM, IT operations ticketing management system, and other security controls.

Most WMSs also integrate with other systems that are used by the organization. Integration provides structure to a process that employs several otherwise independent systems. For example, an optimum WMS for the SOC may take events from SIEM, correlate those events, and create a ticket for the SOC analyst to process. That process would be executed in a workflow that can be defined for the particular event. Some tasks may also be automated to improve efficiency and consistency. 

## WMS Integration Approaches

Many methods are available to integrate WMS within a SOC. The most common method is by using APIs. APIs are a system of tools and resources in an operating system, enabling developers to create software applications. WMSs can also use frameworks such as TAXII for integration.

- ### RESTful API:
A RESTful API uses HTTP requests to get, put, post, and delete data. REST, which is used by browsers, can be thought of as the language of the Internet. WMS can use RESTful APIs to retrieve and send information across the upstream and downstream tools that they integrate with. For example, a WMS may use RESTful API to update a corporate enterprise ticket management system. Similarly, the WMS may use this API to update its own workflow, based on the information that is passed back from the enterprise ticket management system.

- ### Command-line API:
Command-line APIs are similar to RESTful APIs. The primary difference is that command-line APIs are run directly from the command line. WMS can use command-line APIs to execute one-time or ad hoc commands and retrieve a specific set of information. For example, a WMS may use command-line APIs to query a SIEM tool with the SOC in order to check on the status of a particular use case, and confirm if the use case is still considered live or if it has been taken back for rebuild or test.

- ### TAXII:
A free and open transport mechanism, TAXII standardizes the automated exchange of cyber threat information. Based on the discrete use of the WMS, where a WMS is required to make decisions that are based on specific threat intelligence or conditions, a WMS can apply the industry recognized framework, TAXII, to retrieve and exchange information that relates to a particular threat or group of threats.

## SOC Workflow Automation Example

SOC today is changing, and the need for automation is becoming mission-critical. As organizations grow or mature their security capabilities, the need for a more automated SOC operation becomes ever more evident. The diverse set of operational security functions, processes, and departments justify the need of a centralized and coordinated SOC. Managing security defenses and incident response through a program of orchestration and automation allows businesses to optimize the effectiveness and operating speed of the SOC. Today, many companies require specialized, automated tools to meet regulatory obligations in case of a serious information security incident.

Automation is the process of making the tools and machines execute repeatable actions without human intervention. Orchestration is the utilization of automating these tasks to complete the workflow. Reducing the time that is needed to perform redundant tasks, such as logging in to multiple device consoles and other manual tasks, gives security analysts more time to focus on what matters: collaborating and making informed decisions to contain, remediate, and recover from a security incident.

By incorporating sophisticated and progressive technology for security automation, businesses can realize critical advantages, such as:

- More effectively manage the security incidents with faster response times while being consistent in the response capabilities, and reducing the risk of human error.
- Allow the SOC to evolve the playbook to deal with recurring and unique events.
- Allow the SOC analysts to focus on the issues that truly require human critical-thinking skills.
- Eliminate manual efforts, resulting in time savings and reduced labor costs.
- Reduce the time to detection, containment, and remediation.

More complex analysis may not lend itself well to automation—for example, when the investigation process involves disparate data sources or data across incompatible tools. For most plays in the playbook, eventually, an analyst may need to review the resulting data output from the play, which is no different than any other security monitoring approach. SIEM, log management, or other security solutions may still require some human analysis and critical thinking.

## SOC Workflow for an Alert

The following shows a sample workflow for an alert that was initially received by a SOC Tier 1 analyst. Each level of the SOC workflow can be divided into several subtasks. For example, the following tasks are assigned to the SOC Tier 1 analyst after a SIEM alert is received:

- Open a case in ticketing system.
- Look up user details in user directory to obtain name, location, email, and manager.
- Look up the user hostname and IP address.
- Look up the IP address in the threat intel platform to get context (threat intel source, related threats, and reputation score).
- Collect the user proxy traffic report and assigns to case.
- Collect user packet captures for analysis and assigns to case.
- Review user traffic history with threat intel to understand the context and to determine the potential threat impact.
- Assign severity and priority.
- Escalate the event to Tier 2 for investigation.

Note: While many of the tasks within the workflow can be automated, some tasks may need to be performed manually. For example, reviewing user traffic history with threat intel to understand the context and determining the potential threat impact may be manual tasks that are performed by the Tier 1 SOC analyst.

The following tasks are performed by a Tier 2 SOC analyst after escalation from a SOC Tier 1 analyst:

- Review threat intelligence.
- Review packet captures to determine if an exploit was deployed.
- Query endpoint for indicators of compromise.
- Execute endpoint log collection and memory dump.
- Determine whether to contain an infected host.
- Execute containment.
- Add artifacts of evidence collection to case and updates case details.
- Notify SOC Tier 3 and management.

The SOC Tier 3 forensics and incident handler performs these tasks:

- Send technical support to remediate machine (reimage and extract malicious content).
- Extract new indicators and sends to threat intel platform.
- Provide context and threat summary for update in threat intel platform.
- Update case details and closes case.

Management does the following:

- Collect summary and statistics on the case (time to detect, time to contain, time to resolve, and time to close).

## WMS Products

Many SOC WMS (or SOAR) products and vendors focus on providing specific functionalities around automating workflows for the SOC. SOC WMS (or SOAR) vendors include the following:

- Cisco SecureX
- Cisco CloudCenter Action Orchestrator (simplifies workflow creation using a drag and drop workflow designer)
- CyberSponse
- IBM Resilient Systems
- Proofpoint Threat Response
- Swimlane

Orchestration and automation can help a SOC analyst to operate more efficiently. 
