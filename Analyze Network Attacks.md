
# Scenario

You work as a security analyst for a travel agency that advertises sales and promotions on the company’s website. The employees of the company regularly access the company’s sales webpage to search for vacation packages their customers might like. 

One afternoon, you receive an automated alert from your monitoring system indicating a problem with the web server. You attempt to visit the company’s website, but you receive a connection timeout error message in your browser.

You use a packet sniffer to capture data packets in transit to and from the web server. You notice a large number of TCP SYN requests coming from an unfamiliar IP address. The web server appears to be overwhelmed by the volume of incoming traffic and is losing its ability to respond to the abnormally large number of SYN requests. You suspect the server is under attack by a malicious actor. 

You take the server offline temporarily so that the machine can recover and return to a normal operating status. You also configure the company’s firewall to block the IP address that was sending the abnormal number of SYN requests. You know that your IP blocking solution won’t last long, as an attacker can spoof other IP addresses to get around this block. You need to alert your manager about this problem quickly and discuss the next steps to stop this attacker and prevent this problem from happening again. You will need to be prepared to tell your boss about the type of attack you discovered and how it was affecting the web server and employees.

# Solution

## Part 1: Identify the type of attack that may have caused this network interruption.

It is evident from the packet capture logs that a Denial of Service (DoS) attack occurred on the web server. The logs also indicate that a flood of SYN requests was made by one IP address in order to execute the DoS, revealing a direct SYN flood attack.

## Part 2: Explain how the attack is causing the website to malfunction:

### When website visitors try to establish a connection with the web server, a three-way handshake occurs using the TCP protocol. Explain the three steps of the handshake:

The three steps of a threeway handshake are: SYN, SYN/ACK, and ACK. The client requests a connection via a SYN packet, to which the server acknowledges and sends a SYN/ACK packet. Finally, the client sends the ACK packet to aknowledge the connection to the server.

### Explain what happens when a malicious actor sends a large number of SYN packets all at once:

When an attacker sends a high volume of SYN packets at once, the server's bandwidth is overwhelmed to the point of being unresponsive to all requests, including genuine SYN packets.

