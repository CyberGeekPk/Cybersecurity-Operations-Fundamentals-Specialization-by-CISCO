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

