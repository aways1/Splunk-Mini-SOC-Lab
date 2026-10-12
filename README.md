Splunk Mini SOC Lab — Authentication Log Analysis

Overview

This project is a beginner cybersecurity lab created to practise Security Operations Centre (SOC) analyst skills using Splunk Enterprise and a synthetic authentication-log dataset.

The goal was to explore login activity, identify patterns in failed authentication attempts, and present the findings in a simple monitoring dashboard.

Tools Used

- Splunk Enterprise
- Search Processing Language (SPL)
- CSV authentication-log dataset
- Splunk Dashboard Studio

What I Did

1. Imported a synthetic authentication dataset into the `soc_lab` index in Splunk.
2. Searched and analysed login events using SPL.
3. Counted failed login events.
4. Grouped failed attempts by username and source IP address.
5. Built a dashboard with three panels to visualise the results.
6. Reviewed a suspicious sequence of failed logins followed by a successful login.
7. Documented the findings and identified further investigation steps.

Key Findings

- Analysed 19 simulated authentication events.
- Identified 14 failed-login events and 5 successful-login events.
- Found 6 failed attempts associated with `admin`, 5 with `ahmed`, and 3 with `sara`.
- Found 11 failed attempts from `192.0.2.50` and 3 from `192.0.2.70`.
- Observed five failed login attempts for `ahmed`, followed by a successful login from the same source IP one minute later.

Investigation and Limitations

The sequence of failed attempts followed by a successful login was considered suspicious and worthy of further investigation. However, the synthetic dataset does not establish that an account was compromised or that the activity was malicious.

In a real investigation, I would review additional authentication and endpoint logs and check whether the activity was recognised by the account owner.

Project Contents

- `dataset/` — synthetic authentication logs
- `queries/` — SPL searches used in the investigation
- `screenshots/` — dashboard and search-result screenshots
- `incident-report.md` — investigation notes and recommendations

What I Learned

- How to search and analyse authentication events in Splunk.
- How to use SPL to count and group events.
- How to investigate patterns by username and source IP.
- How to present findings in a dashboard.
- Why suspicious activity should be investigated without automatically assuming a compromise.

Disclaimer

This is an educational portfolio project using synthetic data. It is not a real company investigation, and the results do not represent a confirmed security incident.