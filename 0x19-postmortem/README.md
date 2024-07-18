2:00 PM: Issue detected by monitoring alert indicating high failure rates on incoming web requests.
2:05 PM: On-call engineer confirmed the outage and began investigation.
2:15 PM: Assumed a database connectivity issue due to recent maintenance work.
2:30 PM: Database team confirmed no issues on their end.
2:45 PM: Investigated application server logs; found no anomalies.
3:00 PM: Escalated to network engineering team.
3:15 PM: Network team identified recent firewall rule changes.
3:30 PM: Misleading assumption that firewall rules were correct.
3:45 PM: Full review of firewall configuration initiated.
4:00 PM: Identified and corrected the misconfigured firewall rule.
4:15 PM: Confirmed restoration of service.
4:30 PM: Monitoring confirmed normal traffic patterns and user access.
Root Cause and Resolution
Root Cause: The root cause was a firewall rule update intended to enhance security. The new rule inadvertently blocked all traffic to the web servers. This configuration error occurred due to a lack of thorough review and testing procedures for firewall changes.
Resolution: The network engineering team reviewed the firewall configuration and identified the erroneous rule. The rule was corrected to allow traffic to the web servers while maintaining the intended security enhancements. Post-correction, the web application functionality was restored, and normal traffic resumed.
Corrective and Preventative Measures
Improvements:

Implement a more rigorous review process for firewall rule changes.
Enhance monitoring to detect traffic anomalies caused by firewall configurations.
Conduct regular training for engineers on the importance of testing changes in a staging environment before production deployment.
Tasks:

Patch Firewall Configuration: Correct the specific firewall rule to prevent future disruptions.
Add Monitoring: Implement monitoring for firewall rule changes and traffic patterns.
Update Change Management Process: Include mandatory peer review for all network configuration changes.
Training Sessions: Conduct training for network and application engineers on best practices for configuration changes.
Staging Environment: Set up a comprehensive staging environment to test firewall rules before production deployment.
Incident Review Meetings: Schedule regular incident review meetings to discuss root causes and preventative measures with the entire engineering team.
