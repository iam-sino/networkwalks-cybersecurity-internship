# networkwalks-B084-cybersecurity-internship-W2
Documentation of my cybersecurity internship practical exercises, including network footprinting, reconnaissance, network scanning, security analysis and hands-on lab activities.

## Footprinting & Reconnaissance

I performed reconnaissance against the networkwalks.com domain using six Kali Linux tools: WHOIS, WhatWeb, Nslookup, cURL, WAFW00F, and DNSRecon. Each tool was used to gather a different type of information about the target domain and its web infrastructure.

First, I used WHOIS to obtain publicly available domain registration information. The results identified GoDaddy.com, LLC as the domain registrar and showed that the registrant information was protected by a privacy service, Domains By Proxy, LLC. The results also revealed the domain's name servers, including NS6135.HOSTGATOR.COM, NS6136.HOSTGATOR.COM, and NS29.DOMAINCONTROL.COM.

Next, I used WhatWeb to identify the technologies running on the website. The results identified Apache as the web server, WordPress 7.1.4 as the content management system, and WP Download Manager 3.3.76. Other technologies identified included Bootstrap 7.1.4 and jQuery 3.7.1.

Using Nslookup, I resolved the domain name to its corresponding IP address. The result identified 192.232.216.135 as the IP address associated with networkwalks.com.

I then used cURL with the "-I" option to inspect the website's HTTP response headers. The result returned an HTTP/2 200 response, indicating that the server successfully responded to the request. The headers also exposed information about the server and revealed a WordPress REST API endpoint through "/wp-json/".

Next, I used WAFW00F to identify whether a Web Application Firewall was protecting the website. The result identified ModSecurity (SpiderLabs) as the WAF protecting the domain.

Finally, I used DNSRecon to enumerate the domain's DNS records. The results revealed information about the Start of Authority (SOA), name servers (NS), mail servers (MX), address records (A), and text records (TXT). The TXT records included SPF information and a Google site verification entry. The scan also reported that no SRV records were found and returned no answer for the DNSSEC query.

These activities helped me understand how different reconnaissance tools can be used to collect publicly available information about a domain, identify its underlying technologies, and examine aspects of its DNS and web infrastructure.

# Network Scanning with Zenmap

For the second activity, I used Zenmap to perform network discovery on my local network. The practical required me to identify my local IP address and subnet, discover live hosts, identify their IP and MAC addresses, and generate a network topology.
I first used the Windows "ipconfig" command to identify my local IP address and LAN subnet. I then entered the subnet into Zenmap and selected Ping Scan to identify active hosts.
The scan was performed against the 192.168.56.0/24 subnet. The results identified three live hosts:
- 192.168.56.100
- 192.168.56.101
- 192.168.56.1
The scan also identified two MAC addresses:
- 08:00:27:9E:D1:21
- 08:00:27:DC:F0:92
A total of 256 IP addresses were scanned, with 3 hosts found active. The MAC addresses identified by the scan were associated with Oracle VirtualBox virtual network interfaces.
After completing the scan, I opened the Topology section in Zenmap to view the discovered hosts and their network relationships. The topology displayed the three discovered devices connected within the local network.
