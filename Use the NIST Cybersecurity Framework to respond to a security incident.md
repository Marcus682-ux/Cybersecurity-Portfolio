
# Scenario

You are a cybersecurity analyst working for a multimedia company that offers web design services, graphic design, and social media marketing solutions to small businesses. Your organization recently experienced a DDoS attack, which compromised the internal network for two hours until it was resolved.

During the attack, your organization’s network services suddenly stopped responding due to an incoming flood of ICMP packets. Normal internal network traffic could not access any network resources. The incident management team responded by blocking incoming ICMP packets, stopping all non-critical network services offline, and restoring critical network services. 

The company’s cybersecurity team then investigated the security event. They found that a malicious actor had sent a flood of ICMP pings into the company’s network through an unconfigured firewall. This vulnerability allowed the malicious attacker to overwhelm the company’s network through a distributed denial of service (DDoS) attack. 

To address this security event, the network security team implemented: 

* A new firewall rule to limit the rate of incoming ICMP packets

* Source IP address verification on the firewall to check for spoofed IP addresses on incoming ICMP packets

* Network monitoring software to detect abnormal traffic patterns

* An IDS/IPS system to filter out some ICMP traffic based on suspicious characteristics

As a cybersecurity analyst, you are tasked with using this security event to create a plan to improve your company’s network security, following the National Institute of Standards and Technology (NIST) Cybersecurity Framework (CSF). You will use the CSF to help you navigate through the different steps of analyzing this cybersecurity event and integrate your analysis into a general security strategy. We have broken the analysis into different parts in the template below. You can explore them here:

* **Identify** security risks through regular audits of internal networks, systems, devices, and access privileges to identify potential gaps in security. 

* **Protect** internal assets through the implementation of policies, procedures, training and tools that help mitigate cybersecurity threats. 

* **Detect** potential security incidents and improve monitoring capabilities to increase the speed and efficiency of detections. 

* **Respond** to contain, neutralize, and analyze security incidents; implement improvements to the security process. 

* **Recover** affected systems to normal operation and restore systems data and/or assets that have been affected by an incident.

# Incident Report Analysis

## Identify

A malicious attacker identified a vulnerability in the organization's firewall, allowing them to send ICMP from any source. The problem was identified when the attacker gained access to several machines and flooded the network with traffic. This resulted in unresponsive network services.

## Protect

A new firewall rule was implemented in order to limit incoming ICMP packets. An IPS was also put in place to respond when suspicious activity is detected. It is imperative for the security team to regularly update the parameters for the IPS and firewall.

## Detect

Alongside the IPS is an IDS to detect and flag suspicious network traffic for further investigation. The organization has implemented IP verification to detect if an IP has been spoofed. To categorize and analyze logs and activity, a SIEM must be incorporated and viewed routinely.

## Respond

For future incidents, affected systems will be isolated to prevent further damage. The organization shall create alternative means to provide vital network services in the event of an attack. Non-essential ports have been closed and incoming traffic is limited for a particular user accessing the website at one time.

## Recover

Network services will be recovered once the attack is mitigated. Non-essential traffic will be halted in order to limit additional network traffic unrelated to the event. The security team will backup data often in order to reduce the recovery time and this backup shall be stored in a separated environment with increased security controls in place.



