---
layout: handbook-page-toc
title: "SYS.1.01 - Audit Logging Control Guidance"
---

## On this page
{:.no_toc .hidden-md .hidden-lg}

- TOC
{:toc .hidden-md .hidden-lg}

# SYS.1.01 - Audit Logging

## Control Statement

GitLab logs critical information system activity.

## Context

Logging is the foundation for a variety of other security controls including monitoring, incident response, and configuration management. Without comprehensive and reliable logs, large parts of our security compliance program wouldn't be possible. This control is left vague by design. As we develop our system maps and inventories this control will likely become a bit more targeted. To start we really want all GitLab teams to enable system-level logging on all production systems.

An auditor will look to validate in-scope systems are generating logs, those logs are collected, retained the required amount of time and utilized to monitor for performance, health, and anomalies.  To validate the control is working properly, the auditor should require additional pieces of information to demonstrate audit logging is functioning properly.  Those information items include:

* Review of the audit and accountability policy and procedures
* Confirmation that audit events are reviewed and updated on a recurring basis
* Review what should be collected for auditing and cross-reference against what is collected
* Determine what defines a production system to validate the correct systems are being audited
* Confirm log validation processes are working as intended
* Master asset listing to confirm correct systems are being audited
* Log collection process(es)

## Scope

This control applies to all systems within our production environment. The production environment includes all endpoints and cloud assets used in hosting GitLab.com and its subdomains. This may include third-party systems that support the business of GitLab.com.

## Ownership

Control Owner: 

* Infrastructure

Process Owners:

* Security Compliance
* Infrastructure
* Security Operations

## Guidance

Server configuration standards should have logging information enabled for each type of system. These logs should be retained for one year with 90 days of data immediately available for analysis or in accordance with [Record Retention Policy](/handbook/legal/record-retention-policy/), whichever is longer.


### Audit Logging Matrix

_Audit Logging Matrix is a modified version of_ [NIST 800-92 - Guide to Computer Security Log Management](https://nvlpubs.nist.gov/nistpubs/Legacy/SP/nistspecialpublication800-92.pdf)

<table dir="ltr" border="1" cellspacing="0" cellpadding="0"><colgroup><col width="137" /><col width="252" /><col width="218" /><col width="700" /></colgroup>
<tbody>
	<tr>
		<td data-sheets-value="{&quot;1&quot;:2,&quot;2&quot;:&quot;Type&quot;}">Type</td>
		<td data-sheets-value="{&quot;1&quot;:2,&quot;2&quot;:&quot;Value&quot;}">Value</td>
		<td data-sheets-value="{&quot;1&quot;:2,&quot;2&quot;:&quot;Reason(s)&quot;}">Reason(s)</td>
		<td data-sheets-value="{&quot;1&quot;:2,&quot;2&quot;:&quot;Log Example(s)&quot;}">Log Example(s)</td>
	</tr>
	<tr>
		<td colspan="1" rowspan="6" data-sheets-value="{&quot;1&quot;:2,&quot;2&quot;:&quot;General Information&quot;}">
			<div>General Information</div>
		</td>
		<td data-sheets-value="{&quot;1&quot;:2,&quot;2&quot;:&quot;Timestamp&quot;}">Timestamp</td>
		<td data-sheets-value="{&quot;1&quot;:2,&quot;2&quot;:&quot;When the event occurred&quot;}">When the event occurred</td>
		<td data-sheets-value="{&quot;1&quot;:2,&quot;2&quot;:&quot;2017-07-04*13:23:55\n2019-09-30T19:15:26.309Z\nSep 30, 2019 @ 15:15:26.309&quot;}">2017-07-04*13:23:55<br />2019-09-30T19:15:26.309Z<br />Sep 30, 2019 @ 15:15:26.309</td>
	</tr>
	<tr>
		<td data-sheets-value="{&quot;1&quot;:2,&quot;2&quot;:&quot;Event, Status, and/or error codes&quot;}">Event, Status, and/or error codes</td>
		<td data-sheets-value="{&quot;1&quot;:2,&quot;2&quot;:&quot;The action taken&quot;}">The action taken</td>
		<td data-sheets-value="{&quot;1&quot;:2,&quot;2&quot;:&quot;Sep 11 09:46:33 sys1 crontab[20601]: (root) BEGIN EDIT (root)\nSep 11 09:46:39 sys1 crontab[20601]: (root) REPLACE (root)\nSep 11 09:46:39 sys1 crontab[20601]: (root) END EDIT (root)\nstorage.objects.delete\nv1.compute.instances.delete&quot;}">Sep 11 09:46:33 sys1 crontab[20601]: (root) BEGIN EDIT (root)<br />Sep 11 09:46:39 sys1 crontab[20601]: (root) REPLACE (root)<br />Sep 11 09:46:39 sys1 crontab[20601]: (root) END EDIT (root)<br />storage.objects.delete<br />v1.compute.instances.delete</td>
	</tr>
	<tr>
		<td data-sheets-value="{&quot;1&quot;:2,&quot;2&quot;:&quot;Service/cmd/app name&quot;}">Service/cmd/app name</td>
		<td data-sheets-value="{&quot;1&quot;:2,&quot;2&quot;:&quot;What tool the actor used&quot;}">What tool the actor used</td>
		<td data-sheets-value="{&quot;1&quot;:2,&quot;2&quot;:&quot;service sshd start&quot;}">service sshd start</td>
	</tr>
	<tr>
		<td data-sheets-value="{&quot;1&quot;:2,&quot;2&quot;:&quot;User or system acct associated with an event (username, uuid, global UID, API token name, 3rd party)&quot;}">User or system acct associated with an event (username, uuid, global UID, API token name, 3rd party)</td>
		<td data-sheets-value="{&quot;1&quot;:2,&quot;2&quot;:&quot;Actor&quot;}">Actor</td>
		<td data-sheets-value="{&quot;1&quot;:2,&quot;2&quot;:&quot;\&quot;user_id\&quot;:3003042\n\&quot;username\&quot;:\&quot;jsmith-admin\&quot;\n\&quot;TdGZg20BL6pl1duCU2g7\&quot;&quot;}">"user_id":3003042<br />"username":"jsmith-admin"<br />"TdGZg20BL6pl1duCU2g7"</td>
	</tr>
	<tr>
		<td data-sheets-value="{&quot;1&quot;:2,&quot;2&quot;:&quot;Group&quot;}">Group</td>
		<td data-sheets-value="{&quot;1&quot;:2,&quot;2&quot;:&quot;What access the actor has&quot;}">What access the actor has</td>
		<td data-sheets-value="{&quot;1&quot;:3,&quot;3&quot;:6007778}">6007778</td>
	</tr>
	<tr>
		<td data-sheets-value="{&quot;1&quot;:2,&quot;2&quot;:&quot;Device used (e.g. source and destination IPs, terminal session ID, web browser, device ID, etc.)&quot;}">Device used (e.g. source and destination IPs, terminal session ID, web browser, device ID, etc.)</td>
		<td data-sheets-value="{&quot;1&quot;:2,&quot;2&quot;:&quot;Where the event is originating from or terminates&quot;}">Where the event is originating from or terminates</td>
		<td data-sheets-value="{&quot;1&quot;:2,&quot;2&quot;:&quot;source IP - 192.168.xxx.174:8080\ndestination IP - 192.168.xxx.126:53021\ndevice ID -   89ABxDEF-01234567-89ABxDEF&quot;}">source IP - 192.168.xxx.174:8080<br />destination IP - 192.168.xxx.126:53021<br />device ID - 89ABxDEF-01234567-89ABxDEF</td>
	</tr>
	<tr>
		<td colspan="1" rowspan="4" data-sheets-value="{&quot;1&quot;:2,&quot;2&quot;:&quot;OS Events&quot;}">
			<div>OS Events</div>
		</td>
		<td data-sheets-value="{&quot;1&quot;:2,&quot;2&quot;:&quot;Start-up and shut-down of the system&quot;}">Start-up and shut-down of the system</td>
		<td data-sheets-value="{&quot;1&quot;:2,&quot;2&quot;:&quot;Unintended or modified system activity&quot;}">Unintended or modified system activity</td>
		<td data-sheets-value="{&quot;1&quot;:2,&quot;2&quot;:&quot;Jun  1 22:20:05 secserv kernel: Kernel logging (proc) stopped.\nJun  1 22:20:05 secserv kernel: Kernel log daemon terminating.\nJun  1 22:20:06 secserv exiting on signal 15\nNov 27 08:05:57 galileo kernel: Kernel logging (proc) stopped.\nNov 27 08:05:57 galileo kernel: Kernel log daemon terminating.\nNov 27 08:05:57 galileo exiting on signal 15&quot;}">Jun 1 22:20:05 secserv kernel: Kernel logging (proc) stopped.<br />Jun 1 22:20:05 secserv kernel: Kernel log daemon terminating.<br />Jun 1 22:20:06 secserv exiting on signal 15<br />Nov 27 08:05:57 galileo kernel: Kernel logging (proc) stopped.<br />Nov 27 08:05:57 galileo kernel: Kernel log daemon terminating.<br />Nov 27 08:05:57 galileo exiting on signal 15</td>
	</tr>
	<tr>
		<td data-sheets-value="{&quot;1&quot;:2,&quot;2&quot;:&quot;Start-up and shut-down of a service&quot;}">Start-up and shut-down of a service</td>
		<td data-sheets-value="{&quot;1&quot;:2,&quot;2&quot;:&quot;Unintended or modified service activity&quot;}">Unintended or modified service activity</td>
		<td data-sheets-value="{&quot;1&quot;:2,&quot;2&quot;:&quot;Jan 26 12:22:41 combo xinetd[2013]: bind failed (Address already in use (errno = 98)). service = telnet\nJan 26 12:22:41 combo xinetd[2013]: Service telnet failed to start and is deactivated.\nJan 26 12:22:42 combo spamassassin: spamd startup succeeded\nJan 26 12:22:43 combo privoxy: privoxy startup succeeded\nJan 26 12:55:20 combo sendmail: sm-client shutdown succeeded&quot;}">Jan 26 12:22:41 combo xinetd[2013]: bind failed (Address already in use (errno = 98)). service = telnet<br />Jan 26 12:22:41 combo xinetd[2013]: Service telnet failed to start and is deactivated.<br />Jan 26 12:22:42 combo spamassassin: spamd startup succeeded<br />Jan 26 12:22:43 combo privoxy: privoxy startup succeeded<br />Jan 26 12:55:20 combo sendmail: sm-client shutdown succeeded</td>
	</tr>
	<tr>
		<td data-sheets-value="{&quot;1&quot;:2,&quot;2&quot;:&quot;Network connection changes or failures&quot;}">Network connection changes or failures</td>
		<td data-sheets-value="{&quot;1&quot;:2,&quot;2&quot;:&quot;Unintended or modified network activity&quot;}">Unintended or modified network activity</td>
		<td data-sheets-value="{&quot;1&quot;:2,&quot;2&quot;:&quot;Jan 26 12:22:03 combo network: Setting network parameters:  succeeded&quot;}">Jan 26 12:22:03 combo network: Setting network parameters: succeeded</td>
	</tr>
	<tr>
		<td data-sheets-value="{&quot;1&quot;:2,&quot;2&quot;:&quot;Changes to, or attempts to change, system security settings and controls&quot;}">Changes to, or attempts to change, system security settings and controls</td>
		<td data-sheets-value="{&quot;1&quot;:2,&quot;2&quot;:&quot;Security settings and controls are modified very rarely&quot;}">Security settings and controls are modified very rarely</td>
		<td>TBD&nbsp;</td>
	</tr>
	<tr>
		<td colspan="1" rowspan="6" data-sheets-value="{&quot;1&quot;:2,&quot;2&quot;:&quot;Audit Records&quot;}">
			<div>Audit Records</div>
		</td>
		<td data-sheets-value="{&quot;1&quot;:2,&quot;2&quot;:&quot;Log-on attempts (successful or unsuccessful)&quot;}">Log-on attempts (successful or unsuccessful)</td>
		<td data-sheets-value="{&quot;1&quot;:2,&quot;2&quot;:&quot;Identify brute force, password spraying&quot;}">Identify brute force, password spraying</td>
		<td data-sheets-value="{&quot;1&quot;:2,&quot;2&quot;:&quot;May 21 11:21:03 gitlab.com sshd[11179]: &#96;Accepted password&#96; for tanuki from 202.91.xxx.210 port 58244 ssh2\nDec 12 21:32:40 gitlab.com sshd[43456]: &#96;Failed password&#96; for root from 192.168.xxx.174 port37632 ssh2\nJan 22 05:51:12 combo sshd[24935]: Failed password for illegal user miha from ::ffff:212.24.173.67 port 55263 ss&quot;}">May 21 11:21:03 gitlab.com sshd[11179]: `Accepted password` for tanuki from 202.91.xxx.210 port 58244 ssh2<br />Dec 12 21:32:40 gitlab.com sshd[43456]: `Failed password` for root from 192.168.xxx.174 port37632 ssh2<br />Jan 22 05:51:12 combo sshd[24935]: Failed password for illegal user miha from ::ffff:212.24.173.67 port 55263 ss</td>
	</tr>
	<tr>
		<td data-sheets-value="{&quot;1&quot;:2,&quot;2&quot;:&quot;The function(s) performed after logging on (e.g., reading or updating a critical file, software installation)&quot;}">The function(s) performed after logging on (e.g., reading or updating a critical file, software installation)</td>
		<td data-sheets-value="{&quot;1&quot;:2,&quot;2&quot;:&quot;Track all actions taken by actor&quot;}">Track all actions taken by actor</td>
		<td data-sheets-value="{&quot;1&quot;:2,&quot;2&quot;:&quot;Jan 26 12:22:13 combo kernel: audit(1138278089.855:0): avc:  denied  { read write } for  pid=1 exe=/sbin/init name=initctl dev=hda2 ino=1031635 scontext=system_u:system_r:kernel_t tcontext=system_u:object_r:file_t tclass=fifo_file&quot;}">Jan 26 12:22:13 combo kernel: audit(1138278089.855:0): avc: denied { read write } for pid=1 exe=/sbin/init name=initctl dev=hda2 ino=1031635 scontext=system_u:system_r:kernel_t tcontext=system_u:object_r:file_t tclass=fifo_file</td>
	</tr>
	<tr>
		<td data-sheets-value="{&quot;1&quot;:2,&quot;2&quot;:&quot;File changes( e.g., name, creation and deletion, integrity)&quot;}">File changes( e.g., name, creation and deletion, integrity)</td>
		<td data-sheets-value="{&quot;1&quot;:2,&quot;2&quot;:&quot;Unintended or modified file activity&quot;}">Unintended or modified file activity</td>
		<td data-sheets-value="{&quot;1&quot;:2,&quot;2&quot;:&quot;Sat Feb  3 05:32:20 CST 2007 0 /etc/hosts1308742 fd:00 0100644 0 0 00:00 system_u:object_r:etc_t:s0&quot;}">Sat Feb 3 05:32:20 CST 2007 0 /etc/hosts1308742 fd:00 0100644 0 0 00:00 system_u:object_r:etc_t:s0</td>
	</tr>
	<tr>
		<td data-sheets-value="{&quot;1&quot;:2,&quot;2&quot;:&quot;Data export&quot;}">Data export</td>
		<td data-sheets-value="{&quot;1&quot;:2,&quot;2&quot;:&quot;Track data exportation against defined baselines&quot;}">Track data exportation against defined baselines</td>
		<td data-sheets-value="{&quot;1&quot;:2,&quot;2&quot;:&quot;Mon Jun 19 04:44:43 2017 1 10.4.xxx.22 20 /CSV/test1.csv a _ o r testuser ftp 0 * c\nMon Jun 19 04:51:33 2017 1 10.4.xxx.22 432 /CSV/test4.csv a _ o r testuser ftp 0 * c\nMon Jun 19 04:57:15 2017 1 10.4.xxx.22 110 /CSV/test14.csv a _ o r testuser ftp 0 * c\nMon Jun 19 04:57:19 2017 1 10.4.xxx.22 2505 /CSV/master.csv a _ o r testuser ftp 0 * c&quot;}">Mon Jun 19 04:44:43 2017 1 10.4.xxx.22 20 /CSV/test1.csv a _ o r testuser ftp 0 * c<br />Mon Jun 19 04:51:33 2017 1 10.4.xxx.22 432 /CSV/test4.csv a _ o r testuser ftp 0 * c<br />Mon Jun 19 04:57:15 2017 1 10.4.xxx.22 110 /CSV/test14.csv a _ o r testuser ftp 0 * c<br />Mon Jun 19 04:57:19 2017 1 10.4.xxx.22 2505 /CSV/master.csv a _ o r testuser ftp 0 * c</td>
	</tr>
	<tr>
		<td data-sheets-value="{&quot;1&quot;:2,&quot;2&quot;:&quot;Account changes (e.g., account creation and deletion, account privilege assignment)&quot;}">Account changes (e.g., account creation and deletion, account privilege assignment)</td>
		<td data-sheets-value="{&quot;1&quot;:2,&quot;2&quot;:&quot;Identify privilege escalation or suspicious accounts&quot;}">Identify privilege escalation or suspicious accounts</td>
		<td data-sheets-value="{&quot;1&quot;:2,&quot;2&quot;:&quot;sudo: mike : TTY=pts/2 ; PWD=/home/mike ; USER=root ; COMMAND=/usr/sbin/adduser jim\n sudo: pam_unix(sudo:session): session opened for user root by mike(uid=1000)\n groupadd[1731]: group added to /etc/group: name=jim, GID=1001\n groupadd[1731]: group added to /etc/gshadow: name=jim\n groupadd[1731]: new group: name=jim, GID=1001\n useradd[1735]: new user: name=jim, UID=1001, GID=1001, home=/home/jim, shell=/bin/bash\n passwd[1742]: pam_unix(passwd:chauthtok): password changed for jim\n passwd[1742]: gkr-pam: couldn't update the login keyring password: no old password was entered chfn[1743]: changed user 'jim' information\n sudo: pam_unix(sudo:session): session closed for user root&quot;}">sudo: mike : TTY=pts/2 ; PWD=/home/mike ; USER=root ; COMMAND=/usr/sbin/adduser jim<br />sudo: pam_unix(sudo:session): session opened for user root by mike(uid=1000)<br />groupadd[1731]: group added to /etc/group: name=jim, GID=1001<br />groupadd[1731]: group added to /etc/gshadow: name=jim<br />groupadd[1731]: new group: name=jim, GID=1001<br />useradd[1735]: new user: name=jim, UID=1001, GID=1001, home=/home/jim, shell=/bin/bash<br />passwd[1742]: pam_unix(passwd:chauthtok): password changed for jim<br />passwd[1742]: gkr-pam: couldn't update the login keyring password: no old password was entered chfn[1743]: changed user 'jim' information<br />sudo: pam_unix(sudo:session): session closed for user root</td>
	</tr>
	<tr>
		<td data-sheets-value="{&quot;1&quot;:2,&quot;2&quot;:&quot;Successful/failed use of privileged accounts&quot;}">Successful/failed use of privileged accounts</td>
		<td data-sheets-value="{&quot;1&quot;:2,&quot;2&quot;:&quot;Unintended privileged account activity&quot;}">Unintended privileged account activity</td>
		<td data-sheets-value="{&quot;1&quot;:2,&quot;2&quot;:&quot;Jan 30 11:25:57 combo sshd(pam_unix)[3533]: authentication failure; logname= uid=0 euid=0 tty=NODEVssh ruser= rhost=mail.fullerproperties.com  user=root\nJan 23 05:28:18 combo sshd[28534]: Failed password for root from ::ffff:62.26.66.134 port 57203 ssh2&quot;}">Jan 30 11:25:57 combo sshd(pam_unix)[3533]: authentication failure; logname= uid=0 euid=0 tty=NODEVssh ruser= rhost=mail.fullerproperties.com user=root<br />Jan 23 05:28:18 combo sshd[28534]: Failed password for root from ::ffff:62.26.66.134 port 57203 ssh2</td>
	</tr>
	<tr>
		<td colspan="1" rowspan="2" data-sheets-value="{&quot;1&quot;:2,&quot;2&quot;:&quot;Database Operations&quot;}">
			<div>Database Operations</div>
		</td>
		<td data-sheets-value="{&quot;1&quot;:2,&quot;2&quot;:&quot;Direct data changes&quot;}">Direct data changes</td>
		<td data-sheets-value="{&quot;1&quot;:2,&quot;2&quot;:&quot;Integrity of financial data used in reporting&quot;}">Integrity of financial data used in reporting</td>
		<td>TBD&nbsp;</td>
	</tr>
	<tr>
		<td data-sheets-value="{&quot;1&quot;:2,&quot;2&quot;:&quot;ELT job failures&quot;}">ELT job failures</td>
		<td data-sheets-value="{&quot;1&quot;:2,&quot;2&quot;:&quot;Completeness and accuracy of data being used in financial reporting and operational decision-making&quot;}">Completeness and accuracy of data being used in financial reporting and operational decision-making</td>
		<td data-sheets-value="{&quot;1&quot;:2,&quot;2&quot;:&quot;_Dependent on key financial applications_&quot;}">_Dependent on key financial applications_</td>
	</tr>
	<tr>
		<td colspan="1" rowspan="3" data-sheets-value="{&quot;1&quot;:2,&quot;2&quot;:&quot;Application account information&quot;}">
			<div>Application account information</div>
		</td>
		<td data-sheets-value="{&quot;1&quot;:2,&quot;2&quot;:&quot;Successful and failed application authentication attempts&quot;}">Successful and failed application authentication attempts</td>
		<td data-sheets-value="{&quot;1&quot;:2,&quot;2&quot;:&quot;Identify unintended activity&quot;}">Identify unintended activity</td>
		<td data-sheets-value="{&quot;1&quot;:2,&quot;2&quot;:&quot;Git-99-sb-gprd sshd 3087 error: Received disconnect from 10.218.xxx.36 port 39772:3: com.jcraft.jsch.JSchException: Auth fail [preauth] system.auth gprd git-99-sb-gprd git-99-sb-gprd.c.gitlab-production.internal\n\n2019/10/04 18:06:23 [error] 29881#0: *319208 connect() to unix:/var/opt/gitlab/gitlab-workhorse/socket failed (111: Connection refused) while connecting to upstream, client: 156.160.xxx.190, server: git.kts.io, request: \&quot;POST /api/v4/jobs/request HTTP/1.1\&quot;, upstream: \&quot;hxxp://unix:/var/opt/gitlab/gitlab-workhorse/socket:/api/v4/jobs/request\&quot;, host: \&quot;git.kts.io\&quot;&quot;}">Git-99-sb-gprd sshd 3087 error: Received disconnect from 10.218.xxx.36 port 39772:3: com.jcraft.jsch.JSchException: Auth fail [preauth] system.auth gprd git-99-sb-gprd git-99-sb-gprd.c.gitlab-production.internal<br /><br />2019/10/04 18:06:23 [error] 29881#0: *319208 connect() to unix:/var/opt/gitlab/gitlab-workhorse/socket failed (111: Connection refused) while connecting to upstream, client: 156.160.xxx.190, server: git.kts.io, request: "POST /api/v4/jobs/request HTTP/1.1", upstream: "hxxp://unix:/var/opt/gitlab/gitlab-workhorse/socket:/api/v4/jobs/request", host: "git.kts.io"</td>
	</tr>
	<tr>
		<td data-sheets-value="{&quot;1&quot;:2,&quot;2&quot;:&quot;Application account changes (e.g., account creation and deletion, account privilege assignment)&quot;}">Application account changes (e.g., account creation and deletion, account privilege assignment)</td>
		<td data-sheets-value="{&quot;1&quot;:2,&quot;2&quot;:&quot;Identify privilege escalation or suspicious accounts&quot;}">Identify privilege escalation or suspicious accounts</td>
		<td data-sheets-value="{&quot;1&quot;:2,&quot;2&quot;:&quot;October 06, 2014 11:56: User \&quot;Administrator\&quot; (admin@example.com) was created\nOctober 06, 2014 11:56: Documentcloud created a new project \&quot;Documentcloud / Underscore\&quot;\nOctober 06, 2014 11:56: GitLab Org created a new project \&quot;GitLab Org / GitLab Ce\&quot;\nOctober 07, 2014 11:25: User \&quot;Claudie Santie\&quot; (santie_clause@tanuki.co.uk)  was removed\nOctober 07, 2014 11:25: Project \&quot;project133\&quot; was removed&quot;}">October 06, 2014 11:56: User "Administrator" (admin@example.com) was created<br />October 06, 2014 11:56: Documentcloud created a new project "Documentcloud / Underscore"<br />October 06, 2014 11:56: GitLab Org created a new project "GitLab Org / GitLab Ce"<br />October 07, 2014 11:25: User "Claudie Santie" (santie_clause@tanuki.co.uk) was removed<br />October 07, 2014 11:25: Project "project133" was removed</td>
	</tr>
	<tr>
		<td data-sheets-value="{&quot;1&quot;:2,&quot;2&quot;:&quot;Use of application privileges&quot;}">Use of application privileges</td>
		<td data-sheets-value="{&quot;1&quot;:2,&quot;2&quot;:&quot;Unintended privileged account activity&quot;}">Unintended privileged account activity</td>
		<td>&nbsp;TBD</td>
	</tr>
	<tr>
		<td colspan="1" rowspan="4" data-sheets-value="{&quot;1&quot;:2,&quot;2&quot;:&quot;Application Operations&quot;}">
			<div>Application Operations</div>
		</td>
		<td data-sheets-value="{&quot;1&quot;:2,&quot;2&quot;:&quot;Application startup and shutdown&quot;}">Application startup and shutdown</td>
		<td data-sheets-value="{&quot;1&quot;:2,&quot;2&quot;:&quot;Unintended or modified application activity&quot;}">Unintended or modified application activity</td>
		<td>&nbsp;TBD</td>
	</tr>
	<tr>
		<td data-sheets-value="{&quot;1&quot;:2,&quot;2&quot;:&quot;Application failures&quot;}">Application failures</td>
		<td data-sheets-value="{&quot;1&quot;:2,&quot;2&quot;:&quot;Identify brute force, password spraying&quot;}">Identify brute force, password spraying</td>
		<td>&nbsp;TBD</td>
	</tr>
	<tr>
		<td data-sheets-value="{&quot;1&quot;:2,&quot;2&quot;:&quot;Major application configuration changes&quot;}">Major application configuration changes</td>
		<td data-sheets-value="{&quot;1&quot;:2,&quot;2&quot;:&quot;Unintended or modified application configuration activity&quot;}">Unintended or modified application configuration activity</td>
		<td>&nbsp;TBD</td>
	</tr>
	<tr>
		<td data-sheets-value="{&quot;1&quot;:2,&quot;2&quot;:&quot;Application transactions:\n\n&ndash;  e-mail servers recording the sender, recipients, subject name, and attachment names for each e-mail\n\n&ndash;  Web servers recording each URL requested and the type of response provided by the server\n\n&ndash;  business applications recording which financial records were accessed by each user&quot;}">Application transactions:<br /><br />&ndash; e-mail servers recording the sender, recipients, subject name, and attachment names for each e-mail<br /><br />&ndash; Web servers recording each URL requested and the type of response provided by the server<br /><br />&ndash; business applications recording which financial records were accessed by each user</td>
		<td data-sheets-value="{&quot;1&quot;:2,&quot;2&quot;:&quot;Capture relevant application transaction data to create baselines for identifying unintended actions&quot;}">Capture relevant application transaction data to create baselines for identifying unintended actions</td>
		<td>TBD&nbsp;</td>
	</tr>
</tbody>
</table>
<p>&nbsp;</p>
<p>&nbsp;</p>

## Additional control information and project tracking

Non-public information relating to this security control as well as links to the work associated with various phases of project work can be found in the [Audit Logging control issue](https://gitlab.com/gitlab-com/gl-security/security-assurance/sec-compliance/compliance/issues/904).

### Policy Reference

*  [GitLab Audit Logging Policy](/handbook/engineering/security/audit-logging-policy.html)
*  [Monitoring of GitLab.com](/handbook/engineering/monitoring/)
*  [GitLab.com Logging Runbook](https://gitlab.com/gitlab-com/runbooks/tree/master/logging/doc)
    *  [GitLab.com audit logging infrastructure](https://gitlab.com/gitlab-com/runbooks/tree/master/logging/doc#logging-infrastructure-overview)
    *  [GitLab.com - what are we logging](https://gitlab.com/gitlab-com/runbooks/tree/master/logging/doc#what-are-we-logging)
*  [GitLab.com Main Monitoring Dashboards](/handbook/engineering/monitoring/#main-monitoring-dashboards)

## Framework Mapping

* ISO
  * A.12.4.1
* SOC2 CC
  * CC7.2
* NIST 800-53
  * AU-1 
  * AU-2
  * AU-9
  * AU-12
