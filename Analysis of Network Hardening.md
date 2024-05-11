
# Scenario 

You are a security analyst working for a social media organization. The organization recently experienced a major data breach, which compromised the safety of their customers’ personal information, such as names and addresses. Your organization wants to implement strong network hardening practices that can be performed consistently to prevent attacks and breaches in the future. 

After inspecting the organization’s network, you discover four major vulnerabilities. The four vulnerabilities are as follows:

* The organization’s employees' share passwords.

* The admin password for the database is set to the default.

* The firewalls do not have rules in place to filter traffic coming in and out of the network.

* Multifactor authentication (MFA) is not used. 

If no action is taken to address these vulnerabilities, the organization is at risk of experiencing another data breach or other attacks in the future. 

In this activity, you will write a security risk assessment to analyze the incident and explain what methods can be used to further secure the network.

# Security Risk Assessment Report

##  Risk Prevention methods to implement

* Password Policies: Disallowing identical passwords for different users will deter an attacker from moving laterally or even escalating their privileges within the network. Following the current NIST password recommendations will also include salting and hashing which
 will make the attackers task much more difficult and time consuming.
 
* Port filtering: Filtering ununsed and insecure ports such as enforcing the use of port 443 and rejecting use of port 80 will ensure data in transit is not sent in clear text. Port filtering must be enforced on the firewall as well as the switch and routers within the
network to maximize security.

* Multifactor Authentication (MFA): The use of MFA requires much more skill from an attacker looking to brute force their way into the network. The combination of MFA and strong password policies may deter an attacker from wasting their time trying to get into the
 network.

# Summary 

While these network hardening methods do not result in a completely secure network, they are a few of the bare minimum security measures that must be taken. A network that includes PII of consumers must protect their customers if they want to survive as a business. 
There should also be a strong feeling of ethical responsibility for a company to desire integrity of data in their network.



