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

Sequential: A sequential workflow is typically flow chart-based. It progresses from one stage to the next and does not step backward.

State machine: A state machine workflow progresses from state to state. It is more complex and can return to a previous point if required.

Rules-driven: Implementation of a rules-driven workflow is based on a sequential workflow. The rules dictate the progress of the workflow.

A workflow can be described simply as the ordered execution of tasks through a well-defined and structured process. Workflows can be a sequential progression of work activities or a complex set of processes each taking place concurrently and eventually affecting each other according to a set of rules and roles. The WMS defines and controls the various tasks and activities that are associated with a process. In addition, many management systems can also measure and analyze the execution of the process so that continuous improvements can be made. The SOC management team develops the workflow model that implements the standardized operating procedures for the incident handling process. The workflow model guides the SOC analysts through the triage and response procedures. 
