# Security Events Data & SOC ANalyst Tools

- Understand the data collection and data analytics activities performed in a SOC
- Identify tools for performing data collection and analysis activities and how they complement each other
- Describe SOC relevant data and security event data
- Describe SOC tools and their features

## Module Objectives

- Describe SOC relevant data and security event data
- Describe SOC tools and their features

## SOC Relevant Data and Security Event Data Introduction

When responding to an incident, the SOC analyst must perform an analysis  based on event data types. For instance, the event data type that is  used to display only the source and destination elements of a session  differs from the event data type that represents a full account of all  the data exchanged between two devices on the network.  

The SOC analyst must understand the  attack kill chain process to determine which data they need to examine  during the security incident. 

![image](https://github.com/user-attachments/assets/f27c18bb-d38f-4c2d-97c5-de3dd74867c6)

## Network Security Monitoring Data Types

Because  no single data type offers a complete solution, the SOC analyst must  conduct the investigation by analyzing several types of event data:

- Session data
- Full packet capture
- Transaction data
- Extracted data
- Statistical data
- Alert data
- External data

## Session Data

Session data, or flow data,  communication represents a summarized conversation between two endpoint  devices on the network. In the physical world, a detective might analyze  a phone bill in an investigative process. The phone bill does not  capture any information that was exchanged during a phone call. However,  knowing who called whom at what time and for how long can be useful  during an investigation. 

Session data  is the cyber equivalent of a phone bill in the physical world. Session  data documents all the individual network sessions, based on the  session's 5-tuple (transport protocol, source IP address, source port,  destination IP address, and destination port). Session data includes  time stamps, indicating when the session started and when it ended, and  the amount of data. Depending on the source of session data, other  information can be included with the data. NetFlow-v5, NetFlow-v9, and  IPFIX are commonly implemented data session standards.

## Full Packet Capture
While session data can be considered  analogous to a phone bill, a full packet capture can be considered  analogous to a wiretap. A full packet capture consists of the header and  the entire payload of a packet. The full packet capture represents a  full account of all the data exchanged between two devices on the  network. 

The header contains metadata,  such as the packet’s source and destination IP address. The payload  contains all the data exchanged. The actual content of a conversation  can be extracted from full packet captures. From that perspective, a  full packet capture might seem superior to session data.

However,  a full packet capture has downsides. Compared to session data, it has  tremendous storage requirements. It can also be tedious to analyze.  Usually, an analysis that is performed with higher-level data types is  required for effectively guiding the analyst to relevant portions of  full packet capture data. 

There are  various file formats for storing full packet capture data. The most  commonly used file format is the packet capture (PCAP) file extension.

## Transaction Data

Transaction data highlights operations  that occur as a result of network sessions and system activities. For  example, an HTTP daemon software program running on a web server might  produce log files that document all the client requests that it  receives, along with its own responses to those requests. An SMTP daemon  might produce log files to document connections from other SMTP  systems. The log files might also document the forwarding of email  messages to other SMTP systems and the storage of email messages in  local mailboxes. A Linux system might produce a log file that documents  all operating system login and logout activities.

Each  log file contains transaction data. Note that there is not a one-to-one  relationship between session data and transaction data. An individual  network session might not produce any transactions or might be  associated with several transactions. Transactions can also document  local activities on a system that do not involve network communications.

## Extracted Content

Artifacts that are mined from network  traffic are considered extracted content. Such content includes, for  example, files that are transmitted as email attachments or files that  are downloaded from a website. Some security monitoring systems pull  extracted content from live network streams. With other security  monitoring systems, you can mine the extracted content from full packet  capture (PCAP) files. The artifacts may also be smaller pieces of data,  such as particular strings defined by an analyst query.

Artifacts that may be extracted include the following: 

- Sessions: Session  data about all network connections, including the standard IP 5-tuple,  time stamp of the session start, and frame number within the PCAP where  the session starts.
- DNS: Transaction data documenting all DNS requests and replies.
- Hosts: All  IP addresses that are seen in the PCAP along with other relevant  information that can be gleaned from the PCAP. Potential information  includes DNS hostnames, open TCP ports, operating system, sessions that  are associated with the host, and total packet and byte counts that are  associated with the host.

## Statistical Data

Statistical data aggregates other  security monitoring data types. This action aids in describing network  activities at a higher level. Statistical data is used to baseline  network traffic activity. 

NetFlow  session data documents each individual connection to a web server. A  graph can be produced using NetFlow session data that shows the average  number of connections per minute to the web server over a period of a  month, The graph is considered statistical data that can be used to  formulate a monthly report identifying baseline network traffic activity  to and from the web server. Baseline data queries document the  aggregate normal network traffic patterns and their trends. Comparing  actual traffic patterns to the baseline patterns can reveal anomalous  behavior. Two common statistical data queries are baseline graphs and  top reports.

Top reports can answer questions such as the following:

- Which hosts request the most HTTP data?
- Which hosts serve the most HTTP data?
- Which DNS domains are the most requested?

## Alert Data

Alert data is the most formed of the  data types. Alert data is generally produced by an IDS or IPS system.  These systems use complex mechanisms and data sources to monitor traffic  streams for malicious behavior. Alert data is generated when network  traffic or some other type of data matches a set of rules that are  configured in a tool. The greatest benefit of alert data is that it is  created after the tool analyzes large sets of data that otherwise must  be analyzed manually by a SOC analyst.

Despite  being the most formed data type, alert data is not necessarily the most  accurate or most relevant data type. The alert is a judgment call that  is produced by a tool. False positives and false negatives are potential  issues with alert data. The advantage of alert data is that the tool  can process tremendous amounts of network traffic in real time. It is  faster than a human analyst could ever be. However, the production of an  alert is often only the start of the analysis. SOC analysts are the  primary recipients of this type of data and must analyze it to judge its  disposition. The SOC analyst determines whether the alert is a false or  true positive.

## External Data

External data consists of information from outside the organization.  External data is knowledge and information about existing or emerging  threats that an organization can use to proactively respond to those  threats. This knowledge is based on the analysis of input data that is  collected from various internal and external sources. For an  organization to be aware of the latest threats, it must subscribe to  threat intelligence feeds. Threat actors are constantly making  improvements to their malware to avoid detection. Therefore, the SOC  must make constant improvements to the threat detection systems,  including creating and refining rules and signatures or adding new  detection capabilities. Intelligence feeds help the organization to  proactively defend against attacks. SOC analysts incorporate actionable  data from the feeds into indicators of compromise (IoCs) and artifacts  that improve the fidelity of the alerts and provide greater context. 

## SOC Tools and Their Features

A SOC relies on a supporting infrastructure of tools and systems that provide the following services:

- Network mapping
- Network monitoring
- Vulnerability detection
- Penetration testing
- Data collection
- Threat and anomaly detection
- Data aggregation and correlation

One tool that is used by analysts in a SOC is Security Onion.

Security Onion is intended to support SOC analysts with a suite of tools for network security monitoring, including intrusion detection, network security monitoring, and log management. The Security Onion distribution is based on the Ubuntu Linux operating system and contains several useful security tools that are designed to provide four core network security-monitoring functions as follows:

- Full packet capture
- Network-based and host-based intrusion detection sensors
- Security analysis tools
- Log management

The Enterprise Log Search and Archive (ELSA) version of Security Onion is composed of the following tools: 

- ### ELSA: 

ELSA is a centralized syslog framework that is built on Syslog-NG, MySQL, and Sphinx full-text search. It provides a fully asynchronous web-based query interface that normalizes logs and makes searching billions of them for arbitrary strings as easy as searching the web. It also includes tools for assigning permissions for viewing the logs, email-based alerts, scheduled queries, and graphing.

- ### Snort: 

An open source, rules-driven network intrusion detection system (NIDS) and network intrusion prevention system (NIPS) developed by Cisco (Sourcefire). It performs real-time threat detection and generates alerts when threats are detected. The NIPS inline mode is not supported within Security Onion.

- ### Suricata:
A script-driven NIDS and NIPS threat detection engine for analyzing traffic and generating alerts. NIPS inline mode is not supported within Security Onion.

- ### Zeek (Bro): 

A packet recorder and protocol parsing engine that is commonly used to analyze network traffic to detect behavioral anomalies.

- ### Traffic logging: 

Traffic captured by means of SPAN, a TAP port, or a packet broker. Traffic logging generates comprehensive, protocol-specific traffic logs for more than 35 network protocols and application layer analyzers, including HTTP, DNS FTP, and SMTP.

- ### Automated analysis: 

Traffic analysis that uses Bro scripts.

- ### File extraction: 

Extracts and reassembles various file types directly off the wire.

- ### Wazuh (OSSEC): 

Host-based intrusion detection system (HIDS) that replaced OSSEC and is used to monitor and defend Security Onion. Wazuh offers a lightweight monitoring agent that can be installed on network host devices and is supported on Windows, Linux, Mac OS X, HP-UX, AIX, and Solaris platforms.

- ### Netsniff-ng: 

Captures network traffic via SPAN, a TAP port, or packet broker in the form of PCAP files.

- ### Sysmon: 

Windows system service to monitor event log and system activity.

- ### Syslog-ng: 

An enhanced BSD log daemon that can receive logs and collect inputs from a wide range of sources.

## Network analyst tools: 

Provide packet capture and network traffic IP flow analytics capabilities that can be used to find anomalous network activity. The following popular network analyst tools are included within Security Onion:

- ### Wireshark: 
Network protocol analyzer

- ### Sguil: 
Sguil (pronounced "sgweel") is built by network security analysts for network security analysts. Sguil's main component is an intuitive GUI that provides access to real-time events, session data, and raw packet captures. Sguil facilitates the practice of Network Security Monitoring and event driven analysis.

- ### Squert: 
Squert is a web application that is used to query and view event data that is stored in a Sguil database (typically IDS alert data). Squert is a visual tool that attempts to provide additional context to events by using metadata, time series representations and weighted and logically grouped result sets.

- ### NetworkMiner: 
Performs network traffic analysis for parsing PCAP files and extracting artifacts

- ### CyberChef: 
Web-based application for data manipulation

- ### CapME: 
Helps with analyzing PCAP transcripts and downloading captured PCAP files

The preceding tools are included in Security Onion to aid the SOC analyst in viewing network telemetry data and analyzing that data to determine if a network intrusion has occurred. For example, IDS alerts are generated from Snort or Suricata. A SOC analyst could use ELSA to query log data from other sources to validate alert messages that are from Snort. Sguil is a real-time event- and session-monitoring tool that displays data for a SOC analyst to interpret. These types of tools are used by security analysts to perform their jobs.

A newer release of Security Onion is called the Elastic Stack (ELK) version. It includes the following tools:

- ### Elasticsearch: 
Ingest and index logs, large scalable search engine based on Apache Lucene

- ### Logstash: 
Data ingestion engine, parsing, and format logs

- ### Kibana: 
Web dashboard that offers visualizations of ingested log data and data exploration. (Kibana and Squert can pivot to CapMe to retrieve full packet captures.)

- ### TheHIVE: 
Security incident response platform and case management system integrated with Malware Information Sharing Platform (MISP)

- ### Elastic Beats: 
Lightweight data shipper server agent that sends specific types of operational data to Logstash and Elasticsearch

- ### Curator: 
Manage indices through scheduled maintenance

- ### ElastAlert: 
Query Elasticsearch and alert on user-defined anomalous behavior or other interesting bits of information

- ### FreqServer: 
Detect DGAs and find random filenames, script names, process names, service names, workstation names, TLS certificate and issuer subjects, and so on.

- ### DomainStats: 
Conducts whois lookups and provides info about a domain by providing additional context, such as creation time, age, reputation.
