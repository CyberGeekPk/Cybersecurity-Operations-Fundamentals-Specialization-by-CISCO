# Understanding SOC Metrics

- Explain security data aggregation
- Explain Time to Detection (TTD) in context to network security
- Describe security controls detection effectiveness
- Describe SOC metrics

## Learning Objectives

- Explain security data aggregation
- Explain Time to Detection (TTD) in context to network security
- Describe security controls detection effectiveness
- Describe SOC metrics

## Security Data Aggregation

A SIEM is used by most enterprises to provide real-time reporting and analysis of security events. The SIEM collects, sorts, processes, prioritizes, stores, and reports the alarms to the security analyst. One of the main goals of using a SIEM is to reduce the time that is needed to detect, and to contain the threats.

The main SIEM functions include:

- Log collection of event records from sources throughout the organization
- Log normalization to map log messages from different systems to a common data model
- Events and logs correlation to speed the detection of and reaction to security threats
- Consolidating duplicate event records to reduce the volume of event data to be analyzed
- Reporting tools to address regulation compliance reporting requirements

The SIEM is intended to be the glue for various security tools. Many Open Source and closed-source SIEMs are available in the market. Vendor-specific SIEMs, such as Splunk, may also contain some Open Source components. All the Splunk Open Source projects are hosted on GitHub.

## Time to Detection

As stated in a Cisco Annual Security Report, the current industry estimate for time to detection (TTD) is 100 to 200 days, which is clearly an unacceptable time frame given how rapidly malware authors are able to innovate. The time that it takes for businesses to detect a data breach once it occurs gives the threat actors plenty of time to conduct surveillance and steal the sensitive data of a company. Defenders must adopt strategies and implement solutions that provide end-to-end network activities visibility and reduce the TTD. For example, the Cisco CSIRT, using a combination of people, processes (such as the incident response process), and technologies (such as Cisco Advanced Malware Protection [AMP]), reduced the TTD from days to hours.

According to another cybersecurity report conducted by the Ponemon Institute, once a data breach occurs, it takes an average of 98 days for financial services companies to detect intrusion on their networks, and 197 days in retail. Despite the long time to detection, also known as dwell time, 58 percent of people who work in finance and 71 percent of people who work in retail said that they are not optimistic about the ability of their firm to improve these results in the coming year.

While there are varying views on TTD, Cisco defines TTD as the window of time between the first observation of a malicious event having bypassed all security technologies and make it to an endpoint, and the detection of a threat that is associated with that malicious event.

As part of the incident response process, after the detection phase, should come the containment and mitigation phases. Similar to the TTD, other important metrics for measuring the effectiveness of the SOC include the time to containment, and the time to mitigation.

## Security Controls Detection Effectiveness

Effective security controls that work  across the attack continuum can help reduce the TTD. An effective  security control should produce true positive events, few false positive  events, and most importantly, minimal false negative events.

All decisions of security controls can be classified as one of the following:

- ### False negative:
The  security control did not detect actual malicious activity. Minimizing  false negatives should be given a very high priority, sometimes at the  expense of higher occurrences of false positives.

- ### False positive:
The  security control acted as a consequence of benign (nonmalicious)  activity. Many false positives can significantly drain the SOC  resources.

- ### True negative: 
The security control has not acted, because there was no malicious activity, which represents normal and optimal operation.

- ### True positive: 
The security control acted as a consequence of malicious activity, which represents normal and optimal operation.
