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

## SOC Metrics

Today, most enterprises spend more than US$100 billion annually on cybersecurity tools, processes, and people, but history has proven that spending does not always mean secured outcomes. An effective threat-centric SOC consists of deep expertise with cutting-edge technology, leading security intelligence data, and advanced analytics to detect and investigate threats with great speed, accuracy, and focus.

- Speed: Faster detection and targeted mitigation reduce the mean time to respond.
- Focus: Higher fidelity reduces false positives and ensures proper containment and actionable recommendations for remediation.
- Accuracy: Continuous monitoring and investigation plus full packet capture illuminate security blind spots.T

### Reasons to use metrics to define and measure SOC effectiveness include the following:

Typically, the job of the CSO is to find the appropriate reporting model for measuring and reporting the effectiveness of the SOC operations and value that fits the organization. The different metrics that are used to measure the SOC should be as specific, measurable, attainable, relevant, and timely as possible. Metrics is a group of measurements that produce a quantitative picture of something over time.  

Over time and as SOC operations mature, the mean time to detect should begin to trend downward, as shown in the figure. A continued decrease in the TTD is a direct correlation of a successful and mature SOC. It may be years before the metric shows success; the SOC does not mature overnight.  

Typical SOC metrics that demonstrate the SOC's value to the business may include:

- The mean TTD of the incident after its occurrence
- The mean time to contain the incident after its detection
- The mean time to mitigate the incident after its containment
- The number of incidents being detected, contained, and mitigated
- The percentage of the discovered incidents found using the plays in the SOC playbook
- The number of new plays added to the SOC playbook
- The number of zero-day attack detections
- The false positive or true positive detection rate
- The operational cost of running the SOC

Regarding the timeline of the incident, the following figure is another linear approach to measuring the incident response process. The example includes the critical metrics that business decision-makers are most concerned with. The time to report the incident is also included in the dwell time.

In conclusion, metrics are imperative to the success of any SOC organization. Metrics allow leadership to make decisions that are based on data and facts, and allow for the removal of emotion and anecdotes from critical decision-making processes. By implementing a SOC that is built around the metrics, the leadership will be able to show the maturation of the organization and processes, pinpoint areas of focus for process improvement, identify gaps in prevention, and detection and operational capabilities. An organization without a metrics program will open up the possibilities to misdirect spending and ultimately, when dealing with APT, these decisions can lead to substantial impact. As the SOC analyst, your work should help the SOC to achieve its desired metrics.  
