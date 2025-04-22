# SOC Deployment Models & Types

- SOC types
- Staffing considerations
- Deployment models and their consumers
- Describe various SOC types and staffing considerations
- Describe SOC deployment models and their corresponding consumer profiles 

## SOC Types and Staffing Considerations

### Threat-centric SOC

A threat-centric SOC proactively hunts for malicious threats on networks. New threats can be discovered through recently identified vulnerabilities, threat intelligence gathering services, and reported observations detailing malicious anomalies across targeted industry segments.

Detecting attacks and incidents is a challenging task, even for highly trained security personnel. To deal with today's greatest security challenges, organizations need a simpler, scalable, threat-centric approach that addresses security across the entire attack continuum—before, during, and after an attack. 

Before an attack, comprehensive contextual awareness and in-depth analysis of the network traffic are needed to implement policies and controls that properly defend the environment.
During an attack, it is critical to have the ability to continuously detect the presence of malware and block identified threats.
After an attack, the following actions should be taken:

- Marginalize the impact of an attack by identifying the point of entry
- Determine the scope of the attack
- Contain the threat and remediate the infected host
- Minimize the risk of reinfection

### Compliance-Based SOC

A compliance-based SOC is focused on comparing the compliance posture of network systems to reference configuration templates and standard system builds. This type of monitoring detects unauthorized changes and existing configuration problems that may lead to a security breach. Typically, such issues cannot be identified by common security tools, such as vulnerability scanners, unless the configuration problem is actively exploited. The best time to identify potential security issues within the network is certainly not during an exploit.

Linking the risk management and incident response practices of an organization to an automated system compliance process is key to a successful compliance-based SOC. There could be circumstances in which an industry requirement mandates standards-based security practices, such as continuously evaluating against benchmarks established by the Center of Internet Security (CIS) or meeting PCI DSS 2.0 compliance.

### Operational-Based SOC

An operational-based SOC is an internally focused organization that is tasked with monitoring the security posture of an organization’s internal network. Tiers 2 and 3 analysts that work in these SOCs research, develop, and operationalize complex detection techniques that are tailored for an organization's specific network environment. Tier 2 analysts may develop highly customized regular expression (REGEX)-based search strings. Tier 1 SOC analysts are commonly tasked with deploying these customized REGEX-based expressions into the organization’s security information and event management (SIEM) analytic solution. An operational-based SOC is focused on maintaining the operational integrity of the identity management and access policies, intrusion detection system rules, and the administration of firewall access control list (ACL) rules. The Computer Security Incident Response Team (CSIRT) is the most technically accurate term that describes an operational-based SOC.

## SOC Models and Their Consumers

- ## Internal SOC

On-site, fully administered by organization

### Pros

- Best visibility
- Exclusive data management
- Most customizable
- Dedicated in-house staff

### Cons

- Most expensive
- Most difficult to recruit and retain talent
- Slowest implementation
- Cost $$$

- ## Virtual SOC

Contracted service

### Pros

- Least expensive
- Quickest implementation
- Most flexible and saleable

### Cons

- Least visibility
- Third-party data management
- Least customizable
- Cost $

- ## Hybrid SOC

Combination of internal and virtual

### Pros

- Quickest detection and response
- Most secure (extra pair of eyes)
- Knowledge share between internal SOC and third party

### Cons

- Costly in long term
- Additional hardware required
- Third-party data management
- Cost $$
