
# Cybersecurity Incident Report: Network Traffic Analysis

# Scenario

You are a cybersecurity analyst working at a company that specializes in providing IT services for clients. Several customers of clients reported that they were not able to access the client company website www.yummyrecipesforme.com, and saw the error “destination port unreachable” after waiting for the page to load. 

You are tasked with analyzing the situation and determining which network protocol was affected during this incident. To start, you attempt to visit the website and you also receive the error “destination port unreachable.” To troubleshoot the issue, you load your network analyzer tool, tcpdump, and attempt to load the webpage again. To load the webpage, your browser sends a query to a DNS server via the UDP protocol to retrieve the IP address for the website's domain name; this is part of the DNS protocol. Your browser then uses this IP address as the destination IP for sending an HTTPS request to the web server to display the webpage  The analyzer shows that when you send UDP packets to the DNS server, you receive ICMP packets containing the error message: “udp port 53 unreachable.” 

# Logs

_13:24:32.192571 IP 192.51.100.15.52444 > 203.0.113.2.domain: 35084+ A?
yummyrecipesforme.com. (24)_

_13:24:36.098564 IP 203.0.113.2 > 192.51.100.15: ICMP 203.0.113.2
udp port 53 unreachable length 254_

_13:26:42.192571 IP 192.51.100.15.52444 > 203.0.113.2.domain: 35084+ A?
yummyrecipesforme.com. (24)_

_13:27:15.934126 IP 203.0.113.2 > 192.51.100.15: ICMP 203.0.113.2
udp port 53 unreachable length 320_

_13:28:32.192571 IP 192.51.100.15.52444 > 203.0.113.2.domain: 35084+ A?
yummyrecipesforme.com. (24)_

_13.28.50.022967 IP 203.0.113.2 > 192.51.100.15: ICMP 203.0.113.2
udp port 53 unreachable length 150_

# Solution

## Part 1: Provide a summary of the problem found in the DNS and ICMP traffic log.

The UDP protocol reveals that the domain server is not listening on port 53 and this may be due to port filtering or a DoS attack.

This is based on the results of the network analysis, which show that the ICMP echo reply
returned the error message: _udp port 53 unreachable length 254._

The error message indicates that the UDP protocol is blocked by the DNS server; further investigation must be performed to deduce whether or not the DNS server was overloaded by a flood of incoming requests.

# Part 2: Explain your analysis of the data.

Several customers complained about being unable to reach the website and received the error message "destination port unreachable". Upon analysis of the logs, it was determined that the DNS servers are unresponsive. Logs from a previous timeframe shall be investigated in order to determine the root cause of the issue.




