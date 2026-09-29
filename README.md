# NIST-Incident-Report-
Incident report analysis of a simulated phishing attack, mapped to the NIST Cybersecurity Framework (Identify, Protect, Detect, Respond, Recover).

# Objective 
Analysis of a simulated phishing incident, structured around the NIST Cybersecurity Framework (CSF): Identify, Protect, Detect, Respond and Recover, with reflections that reference the Govern function introduced in CSF 2.0.

# Scenario
An employee reported unusually slow network performance at about 10:00 AM. Network logs confirmed an unusually high volume of traffic. She also reported that at about 9:00 AM she had received an email asking her to log in to an external website with her internal credentials. The attacker used an intern's stolen credentials to access the customer database, where records were altered or deleted.

# Timeline
Time                          	      Event
~9:00 AM	                            Phishing email received
~10:00 AM	                            Anomaly reported; high traffic confirmed in logs
After detection	Containment:          account disabled, other credentials reset
Within 24 hours	                      Management informed;  customers and authorities notified
Recovery	                            Database restore planned from the previous night's backup

# Analysis by NIST CSF function
Function	                            Focus of the analysis
Identify	                            Affected assets (intern account, email, internal network, customer database), vulnerabilities (no MFA, excessive privileges,                                       no segmentation, no email filtering) and risks to data confidentiality and integrity
Protect	                              MFA, least privilege, network segmentation, firewall filtering, email security, awareness training with phishing simulations
Detect	                              SIEM log correlation, IDS/IPS on inbound and outbound traffic, alerts on anomalous logins, audit logging and integrity                                             monitoring on the database
Respond	                              Account disabling and credential resets, evidence preservation for forensics, management escalation, customer and regulatory                                       notification (LGPD, GDPR, Swiss nLPD)
Recover	                              Ordered recovery: confirm containment, validate backup, restore (with point-in-time recovery where available), verify                                              integrity, resume services, post-incident review

# Key findings
The phishing email was the entry point, but the impact was amplified by technical gaps: no MFA, excessive privileges on a limited-scope account, no network segmentation and no automated detection.
Least privilege would have limited what a single compromised account could reach.
Traffic-volume blocking alone does not address an attacker using valid credentials. Detection must focus on account behavior, outbound traffic and database activity.
Restoring a backup before confirming containment and validating the backup risks reintroducing the problem.
Real-time alerting reduces dwell time more effectively than relying on employee reports.

# Skills demonstrated
Incident analysis and documentation
Mapping controls to NIST CSF functions
Risk and vulnerability identification
Security control recommendations (MFA, least privilege, segmentation, SIEM, IDS/IPS)
Recovery planning and post-incident review
Regulatory awareness (LGPD, GDPR, Swiss nLPD)

# References
NIST Cybersecurity Framework 2.0
Google Cybersecurity Certificate (Coursera)
