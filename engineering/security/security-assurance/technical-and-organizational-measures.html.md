---
layout: handbook-page-toc
title: "Technical and Organisational Security Measures for GitLab.com"
---

## On this page
{:.no_toc .hidden-md .hidden-lg}

- TOC
{:toc .hidden-md .hidden-lg}

## Technical and Organisational Security Measures for GitLab.com

GitLab Cloud Services meet the specific requirements of data protection, including, without limitation, Article 28 of the General Data Protection Regulation and which are listed as SOC 2 Type 1 (Security).

At a minimum, GitLab has implemented for the GitLab Cloud Services the technical and organizational measures and maintains security practices within the production environments as follows:
	
## Confidentiality of processing systems

### Identity and Access Management
- Predefined security groups are utilized to assign role-based access privileges and segregate access to data to the production systems. 
- Administrator access to the production systems is granted based on job roles and responsibilities and limited to authorized personnel. 				

### Audit Assurance: Compliance, Governance and Risk Management
- GitLab performs annual risk assessments of production applications and services. Results from risk assessment activities are reviewed to prioritize treatment of identified risks. 						
- GitLab performs a vendor security review for third-party vendors whose services will store, process or transmit GitLab and/or GitLab customer data. 			
- GitLab performs risk based continuous control monitoring throughout the year by performing control testing using a formal methodology. The testing results are documented and reviewed by management, including remediation plans for identified observations. 

### Human Resources
- GitLab team members complete security awareness training upon hire and on an annual basis, which includes updates about relevant security policies and how to report security events to the authorized response team.  
- GitLab new hires are required to pass a background check as a condition of their employment. 				

## Integrity of processing systems

### Application & Infrastructure Security					
- A configuration management tool is utilized to ensure security hardening and baseline configuration standards have been established on production servers. 									
- Network traffic to and from untrusted networks passes through a policy enforcement point; firewall rules are established in accordance to identified security requirements and business justifications. 				
- An issue tracking system is in place to centrally maintain, manage, and monitor application and infrastructure changes from development through implementation. 

### Threat and Vulnerability Management
- GitLab conducts vulnerability scans against the production environment to identify threats and assess their potential impact to system security on a weekly basis. Results are evaluated and remediated according to risk rating. 
- GitLab executes a 3rd party application penetration test on an annual basis, a process which includes additional 3rd party remediation testing if any high or moderate risk vulnerabilities are identified. 	
- Monitoring tools are used to continuously monitor security events, latency, network performance, and virtual server performance.	
- Incident response procedures are in place that outline the response procedures to security events and includes lessons learned to evaluate the effectiveness of the procedures. 		

## Availability of processing systems

### Resilience 
- A business continuity plan is in place to guide personnel in procedures to protect against disruptions caused by an unexpected event. 
- Enterprise monitoring applications are configured to monitor in-scope systems capacity levels and alert operations personnel when predefined thresholds have been met. 			

## Additional Considerations
- Google is responsible for implementing controls to manage physical and logical access to the servers and supporting infrastructure, underlying network and virtualization management software for its cloud hosting services where GitLab processing systems reside.
- Customers may elect to implement technical and organisational measures in relation to Customer Data.

## Resources
For additional details and supporting artifacts please see GitLab's [Customer Assurance Package](https://about.gitlab.com/handbook/engineering/security/security-assurance/field-security/customer-assurance-package.html#gitlabs-customer-assurance-package)
