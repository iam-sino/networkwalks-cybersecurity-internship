# **networkwalks-B084-cybersecurity-internship-W2**
Documentation of my cybersecurity internship practical exercises, including network footprinting, reconnaissance, network scanning, security analysis and hands-on lab activities.

## **Footprinting & Reconnaissance**


Target Domain: networkwalks.com

Operating System: Kali Linux

Tools Used: WHOIS, WhatWeb, Nslookup, cURL, WAFW00F, DNSRecon

Project Category: Cybersecurity | Network Security | Information Gathering | Ethical Hacking


# 1. Project Overview

The exercise focused on understanding how publicly available information about a domain and its web infrastructure can be collected using different reconnaissance tools available in Kali Linux.

Footprinting and reconnaissance are important stages in the cybersecurity assessment process. Before attempting to identify security weaknesses in a system, a security professional needs to understand the target's publicly exposed information, technologies, domain infrastructure and potential attack surface.

During this exercise, I conducted reconnaissance against the networkwalks.com domain using six different tools. Each tool served a specific purpose, allowing me to examine different aspects of the target's infrastructure.

The practical activities covered:

- Domain registration information gathering.
- Identification of web technologies and server information.
- Domain-to-IP address resolution.
- HTTP response header inspection.
- Web Application Firewall identification.
- DNS record enumeration.
- Analysis of publicly exposed infrastructure information.
- Identification of potential security implications associated with reconnaissance findings.

The objective was not to exploit the target or gain unauthorised access. Rather, the exercise focused on learning how security professionals gather, interpret and document information during the initial stages of an authorised security assessment.

# 2. Project Objectives

The main objectives of this exercise were to:

1. Understand the concept of footprinting and its importance in cybersecurity.
2. Learn how to gather publicly available domain registration information using WHOIS.
3. Identify website technologies and frameworks using WhatWeb.
4. Understand how DNS resolution works through Nslookup.
5. Inspect HTTP response headers using cURL.
6. Understand how Web Application Firewalls can be identified using WAFW00F.
7. Enumerate DNS records using DNSRecon.
8. Interpret reconnaissance results from a security perspective.
9. Understand how information gathered during reconnaissance can assist an attacker in profiling a target.
10. Develop the ability to document technical findings in a structured security assessment report.

# 3. Understanding Footprinting and Reconnaissance

Footprinting is the process of collecting information about a target organisation, domain, network or system.

It helps security professionals understand what information is publicly accessible and what technologies or infrastructure are associated with a target.

Reconnaissance is commonly divided into two categories:

# 3.1 Passive Reconnaissance

Passive reconnaissance involves gathering information without directly interacting with the target's systems in a way that generates active scanning traffic.

Examples include:

- Reviewing publicly available domain registration records.
- Examining publicly accessible DNS information.
- Researching publicly available information about an organisation.
- Reviewing information available through search engines.

# 3.2 Active Reconnaissance

Active reconnaissance involves directly interacting with a target system or service to collect additional information.

Examples include:

- Sending requests to a web server.
- Identifying web technologies.
- Inspecting HTTP response headers.
- Performing DNS queries.
- Identifying security technologies protecting a web application.

In this practical, I used different reconnaissance utilities to examine the publicly accessible information associated with networkwalks.com.

Understanding the distinction between passive and active reconnaissance is important because the techniques used can generate different levels of interaction with the target infrastructure.

# 4. Scope and Methodology

# 4.1 Scope of Assessment


## 4.1 Scope of Assessment

The assessment focused on the following domain:

**Target:** networkwalks.com

The activities were limited to information gathering and reconnaissance.

The following areas were examined:

| Assessment Area | Purpose |
|---|---|
| Domain registration | Identify registrar and registration-related information |
| Name servers | Identify DNS hosting infrastructure |
| Web technologies | Identify technologies used by the website |
| IP resolution | Determine the IP address associated with the domain |
| HTTP headers | Examine server responses and exposed information |
| WAF identification | Identify the reported Web Application Firewall |
| DNS enumeration | Examine available DNS records |


## 4.2 Methodology

I followed a structured reconnaissance methodology.

Step 1: Domain Information Gathering

I started by examining publicly available registration information using WHOIS.

Step 2: Technology Identification

I used WhatWeb to identify the website's server and application technologies.

Step 3: DNS Resolution

I used Nslookup to determine the IP address associated with the domain.

Step 4: HTTP Header Inspection

I used cURL to examine the website's HTTP response headers.

Step 5: WAF Identification

I used WAFW00F to identify the Web Application Firewall reported by the tool.

Step 6: DNS Enumeration

I used DNSRecon to examine different DNS record types and collect additional infrastructure information.

Step 7: Result Analysis

I reviewed the information collected from each tool and considered its potential security implications.

# 5. Tools and Technologies Used

The following tools were used during the practical exercise.

## 5.1 WHOIS

Purpose: Domain registration information gathering.

WHOIS is a query and response protocol used to retrieve publicly available information about registered internet resources, including domain names.

During a reconnaissance exercise, WHOIS can help identify:

- Domain registrar.
- Registration-related information.
- Name servers.
- Domain creation and expiration information, where available.
- Registrant information, where publicly accessible.

Why it matters in cybersecurity:

An attacker may use domain registration information to understand who manages a domain and identify aspects of its internet infrastructure.

A security professional can also use this information to establish an initial picture of the domain's ownership and DNS arrangements.


## 5.2 WhatWeb

Purpose: Website technology identification.

WhatWeb is a web reconnaissance tool designed to identify technologies used by websites.

It can detect information such as:

- Web server software.
- Content Management Systems (CMS).
- JavaScript libraries.
- Web frameworks.
- Plugins.
- Other identifiable web technologies.

Why it matters in cybersecurity:

Knowing which technologies a website uses can help a security professional determine which components may require further security review.

Attackers may also use technology fingerprinting to identify software associated with publicly documented vulnerabilities.



## 5.3 Nslookup

Purpose: DNS resolution.

Nslookup is a command-line utility used to query DNS servers and retrieve information about domain names.

It helps determine how a domain name resolves to an IP address.

Why it matters in cybersecurity:

DNS resolution provides information about the network location associated with a domain.

This information can help security professionals understand how internet-facing services are identified and accessed.


## 5.4 cURL

Purpose: HTTP communication and response inspection.

cURL is a command-line tool used to transfer data to and from servers using supported network protocols.

In this practical, I used the "-I" option to request HTTP response headers.

HTTP headers can provide information about:

- Server responses.
- Content types.
- Server technologies, where disclosed.
- Security-related response settings.
- Application behaviour.

Why it matters in cybersecurity:

Exposed HTTP headers may reveal technical information about a web application and help security professionals understand how a server responds to incoming requests.



## 5.5 WAFW00F

Purpose: Web Application Firewall identification.

WAFW00F is a security reconnaissance tool used to identify Web Application Firewalls protecting websites.

A Web Application Firewall (WAF) monitors and filters HTTP traffic to help protect web applications against certain malicious requests.

Why it matters in cybersecurity:

Identifying a WAF can provide insight into the security architecture of a web application.

However, identifying a WAF does not automatically establish how effectively it protects the application.


## 5.6 DNSRecon

Purpose: DNS enumeration.

DNSRecon is a DNS reconnaissance tool used to collect information about DNS infrastructure.

It can examine different DNS record types, including:

- A records.
- AAAA records.
- NS records.
- MX records.
- SOA records.
- TXT records.
- SRV records.

Why it matters in cybersecurity:

DNS records can reveal information about domain infrastructure, mail services, name servers and other internet-facing services.

This information can help security professionals understand the organisation's external infrastructure and identify areas that may require further review.

## 6. Practical Implementation and Findings

# 6.1 Domain Registration Information Gathering Using WHOIS

I started the reconnaissance exercise by using WHOIS to obtain publicly available registration information about networkwalks.com.

The purpose was to identify the domain registrar, examine the registration information and determine which name servers were associated with the domain.

Observations:

The WHOIS results identified:

- Domain Registrar: GoDaddy.com, LLC.
- Registrant Privacy Service: Domains By Proxy, LLC.
- Name Server 1: NS6135.HOSTGATOR.COM.
- Name Server 2: NS6136.HOSTGATOR.COM.
- Name Server 3: NS29.DOMAINCONTROL.COM.

The results showed that the registrant information was protected through a domain privacy service.

The identified name servers also provided information about the domain's DNS infrastructure.

Security Implications:

Domain registration information can help security professionals understand the administrative and technical arrangements associated with a domain.

From an attacker's perspective, identifying name servers and registration-related information may assist in building an initial infrastructure profile.

However, the presence of publicly available WHOIS information is not itself a vulnerability.


WHOIS command: whois networkwalks.com


![WHOIS Result 1](./Whois%20Result%201.png)

![WHOIS Result 2](./Whois%20Result%202.png)

![WHOIS Result 3](./Whois%20Result%203.png)



# 6.2 Website Technology Identification Using WhatWeb

After gathering domain registration information, I used WhatWeb to identify the technologies running on networkwalks.com.

The objective was to understand the website's underlying technology stack and identify the web server, content management system and other detectable components.

Observations:

The WhatWeb results identified the following technologies:

Technology| Identified Result
Web Server| Apache
Content Management System| WordPress 7.1.4
WordPress Plugin| WP Download Manager 3.3.76
Front-end Framework| Bootstrap 7.1.4
JavaScript Library| jQuery 3.7.1

These results provided an overview of the technologies identified by the scanning tool.

Security Implications:

Technology fingerprinting is an important part of reconnaissance because different software components may have different security requirements.

For example, an outdated or misconfigured content management system or plugin may introduce security risks.

Attackers may compare identified software versions against publicly documented vulnerabilities to determine whether further investigation is necessary.

However, identifying a software version does not prove that the software is vulnerable.

Further authorised testing and version verification would be required.


WhatWeb command: whatweb networkwalks.com

![WhatWeb Results](./whatweb%20Result.png)


# 6.3 DNS Resolution Using Nslookup

I then used Nslookup to resolve networkwalks.com into its corresponding IP address.

The purpose of this activity was to understand how DNS translates human-readable domain names into IP addresses used for network communication.

Observation:

The result identified the following IP address:

192.232.216.135

This was the IP address returned for networkwalks.com during the practical exercise.

Technical Explanation:

DNS resolution allows users and applications to access internet services using domain names instead of having to remember numerical IP addresses.

When a user enters a domain name into a browser, DNS resolution helps determine the IP address associated with that domain.

Security Implications:

An identifiable IP address provides information about the network location associated with a web service.

An attacker may use this information as part of broader infrastructure reconnaissance.

Security professionals can use the same information to understand their external exposure and identify the systems associated with their organisation.


Nslookup command: nslookup networkwalks.com

![Nslookup Results](./nslookup%20Result.png)


# 6.4 HTTP Response Header Inspection Using cURL

The next activity involved using cURL to inspect the HTTP response headers returned by the website.

I used the "-I" option to request the response headers without downloading the complete webpage content.

Observations:

The request returned:

HTTP/2 200

This indicated that the server successfully processed the request and returned a successful HTTP response.

The response headers also exposed technical information about the server.

Additionally, the results revealed the WordPress REST API endpoint:

"/wp-json/"

Technical Explanation:

HTTP response headers provide additional information about communication between a client and a web server.

The HTTP status code 200 indicates that the request was successful.

The WordPress REST API provides an interface through which applications can interact with WordPress resources.

Security Implications:

Exposed response headers may provide information that assists technology fingerprinting.

The availability of a REST API endpoint may also provide additional information about the application's functionality and publicly accessible resources.

However, the existence of a REST API endpoint does not automatically indicate a security weakness.

The endpoint would require further authorised assessment to determine whether access controls and information exposure are appropriately configured.


cURL command: curl -I https://networkwalks.com

![cURL Results](./curl%20Result.png)



# 6.5 Web Application Firewall Identification Using WAFW00F

I used WAFW00F to determine whether a Web Application Firewall was identifiable on networkwalks.com.

The objective was to understand whether the website's infrastructure used a security technology designed to inspect and filter web traffic.

Observation:

The result identified:

ModSecurity (SpiderLabs)

This indicated that WAFW00F detected ModSecurity (SpiderLabs) as the Web Application Firewall associated with the target.

Technical Explanation:

A Web Application Firewall operates at the application layer and helps protect web applications by inspecting incoming HTTP requests.

Depending on its configuration, it may help detect or block malicious requests associated with attacks such as:

- SQL injection.
- Cross-Site Scripting (XSS).
- Malicious request patterns.
- Certain forms of automated application abuse.

Security Implications:

Identifying the WAF provides information about the website's security architecture.

An attacker may use this information to understand the defensive technologies present on a target.

From a defensive perspective, identifying the WAF is useful, but it does not confirm that every attack is prevented.

The effectiveness of a WAF depends on its configuration, rules, updates and overall security management.


WAFW00F command: wafw00f networkwalks.com

![WAFW00F Results](./wafw00f-result.png)


# 6.6 DNS Enumeration Using DNSRecon

Finally, I used DNSRecon to enumerate the DNS records associated with networkwalks.com.

The objective was to gather additional information about the domain's DNS configuration and identify records associated with different internet services.

Observations:

The DNSRecon results revealed information relating to the following DNS record types:

DNS Record| Purpose
SOA| Provides administrative information about a DNS zone
NS| Identifies authoritative name servers
MX| Identifies mail servers responsible for receiving email
A| Maps a domain name to an IPv4 address
TXT| Stores text-based information associated with a domain
SRV| Provides information about specific network services

The TXT records included SPF information and a Google site verification entry.

The scan also reported that no SRV records were found and returned no answer for the DNSSEC query.

Technical Explanation:

DNS records play an important role in the operation of internet services.

For example:

- A records help direct domain names to IPv4 addresses.
- MX records identify mail servers.
- NS records identify the authoritative DNS servers.
- TXT records can contain domain verification and email authentication information.
- SOA records contain administrative information about a DNS zone.

SPF information is particularly relevant to email security because it helps identify which mail servers are authorised to send email on behalf of a domain.

Security Implications:

DNS enumeration can reveal information about an organisation's external infrastructure.

Attackers may use this information to understand its DNS configuration, identify associated services and build a broader picture of the target environment.

From a defensive perspective, organisations should review their DNS records regularly and ensure that unnecessary or sensitive information is not exposed.

The absence of an SRV record in this scan does not establish that the organisation has no other services. Similarly, receiving no answer to a DNSSEC query is not sufficient by itself to conclude that DNSSEC is disabled.


DNSRecon Commad:  dnsrecon -d networkwalks.com

![DNSRecon Results](./dnsrecon%20Result.png)


7. Consolidated Findings

The following table summarises the major findings from the six reconnaissance activities.

Tool| Main Finding| Security Relevance
WHOIS| GoDaddy.com, LLC registrar and identified name servers| Provides domain registration and infrastructure information
WhatWeb| Apache, WordPress 7.1.4, WP Download Manager 3.3.76, Bootstrap and jQuery| Reveals identifiable web technologies
Nslookup| 192.232.216.135| Identifies the resolved IP address
cURL| HTTP/2 200 and "/wp-json/" endpoint| Reveals response and application information
WAFW00F| ModSecurity (SpiderLabs)| Identifies reported WAF technology
DNSRecon| SOA, NS, MX, A and TXT information| Provides insight into DNS infrastructure

8. Risk Analysis and Potential Security Impact

Based on the information collected during the reconnaissance activities, I identified several potential security considerations.

No.| Risk / Finding| Evidence| Potential Impact| Risk Level
1| Web technology information exposed| WhatWeb identified Apache, WordPress and associated technologies| May help attackers identify software components requiring further security review| Medium
2| Server IP address identifiable| Nslookup resolved the domain to 192.232.216.135| Provides information about the network location of the web service| Low
3| HTTP technical information exposed| cURL returned HTTP response headers and exposed "/wp-json/"| May assist technology fingerprinting and further enumeration| Low
4| WAF technology identifiable| WAFW00F identified ModSecurity (SpiderLabs)| Reveals information about the web application's security architecture| Low
5| DNS infrastructure information exposed| DNSRecon identified DNS, mail and service-related records| May help attackers build a broader infrastructure profile| Medium

Risk assessment note: These ratings represent preliminary risk considerations based on information exposure. They are not confirmed vulnerability severity ratings. No exploitation or vulnerability validation was conducted during this practical.

9. Understanding the Difference Between Information Exposure and a Vulnerability

One important lesson from this exercise was understanding that information gathering and vulnerability identification are two different activities.

For example, identifying WordPress 7.1.4 through WhatWeb does not automatically mean the website has a WordPress vulnerability.

Similarly, identifying an IP address through DNS resolution does not mean that the server is insecure.

The same applies to the discovery of HTTP headers, DNS records and WAF technologies.

These findings provide information that may assist further security assessment, but they do not independently establish that a system can be compromised.

A proper vulnerability assessment would require additional investigation, verification and testing within an authorised scope.

This distinction is important because cybersecurity professionals must avoid reporting ordinary technical information as confirmed security vulnerabilities.

10. Key Security Lessons Learned

This practical exercise helped me understand several important cybersecurity concepts.

1. The importance of reconnaissance

I learned that reconnaissance provides an initial understanding of a target before more advanced security testing begins.

2. Domain registration and DNS infrastructure

I gained practical experience using WHOIS and DNSRecon to examine domain registration information and DNS records.

3. Web technology fingerprinting

I learned how WhatWeb can identify technologies used by a website and why exposed technology information may be relevant during security assessments.

4. DNS resolution

Using Nslookup helped me understand how domain names are translated into IP addresses.

5. HTTP communication

Using cURL helped me understand HTTP response headers and the meaning of successful HTTP status codes.

6. Web Application Firewalls

WAFW00F introduced me to the process of identifying web application protection technologies.

7. Security interpretation

I learned that not every piece of exposed technical information represents a vulnerability. Findings must be interpreted carefully before assigning security risks.

8. Technical documentation

I gained experience documenting commands, observations, technical findings and their potential security implications.

11. Challenges and Technical Considerations

During reconnaissance, it is important to understand that tools provide information based on the responses they receive.

Different tools may produce different results depending on DNS configuration, server responses, network conditions and the availability of publicly accessible information.

Some important considerations include:

- WHOIS information may be protected by domain privacy services.
- Web technology detection may not identify every technology used by a website.
- DNS resolution may return different addresses depending on DNS configuration.
- HTTP headers may disclose only limited server information.
- WAF detection tools identify technologies based on observable responses and detection signatures.
- DNS enumeration results may not contain every possible record or service.
- A missing DNS response should not automatically be interpreted as proof that a record or security feature does not exist.

Understanding these limitations is necessary when interpreting reconnaissance results.

12. Recommendations and Defensive Considerations

Based on the observations made during this exercise, the following general defensive considerations are relevant:

1. Regular Technology Updates

Organisations should regularly review and update their content management systems, plugins, frameworks and server software.

2. Minimise Unnecessary Information Disclosure

Web servers should avoid exposing unnecessary technical information through response headers or publicly accessible resources.

3. Review DNS Configuration

DNS records should be reviewed periodically to ensure that they remain accurate and that unnecessary records are removed.

4. Maintain Email Authentication Controls

SPF and other applicable email authentication mechanisms should be reviewed and properly configured to reduce email spoofing risks.

5. Review Web Application Security

Publicly accessible application endpoints should be reviewed to ensure appropriate authentication, authorisation and access controls.

6. Maintain WAF Security Rules

Web Application Firewall rules should be reviewed and updated regularly to ensure that they provide appropriate protection.

7. Conduct Periodic Security Assessments

Organisations should perform authorised security assessments to identify weaknesses that cannot be established through reconnaissance alone.

13. Conclusion

This practical exercise provided hands-on experience with six important reconnaissance tools available in Kali Linux.

By using WHOIS, WhatWeb, Nslookup, cURL, WAFW00F and DNSRecon, I was able to examine different aspects of the networkwalks.com domain, including its registration information, web technologies, IP address, HTTP response headers, Web Application Firewall and DNS infrastructure.

More importantly, the exercise helped me understand how seemingly small pieces of publicly available information can contribute to a broader understanding of an organisation's external attack surface.

I also learned the importance of interpreting findings correctly. Identifying a technology, IP address or DNS record does not automatically establish that a security vulnerability exists.

Overall, this exercise strengthened my practical understanding of footprinting, reconnaissance, DNS operations, web technology identification and the importance of structured security documentation.

It also provided a foundation for more advanced cybersecurity activities involving network scanning, vulnerability assessment and security analysis.

14. Skills Demonstrated

The following skills were developed or practised during this exercise:

- Cybersecurity reconnaissance.
- Domain information gathering.
- WHOIS investigation.
- Web technology fingerprinting.
- DNS resolution.
- DNS enumeration.
- HTTP response header analysis.
- Web Application Firewall identification.
- Attack surface awareness.
- Preliminary risk identification.
- Technical security documentation.
- Kali Linux command-line operations.

15. Project Evidence

Screenshots and terminal outputs should be included to demonstrate the activities performed and support the findings documented in this repository.

Recommended evidence structure:

1. WHOIS command and output.
2. WhatWeb command and output.
3. Nslookup command and output.
4. cURL HTTP response headers.
5. WAFW00F command and output.
6. DNSRecon command and output.

Each screenshot should be clearly labelled and placed under its corresponding section.

16. Disclaimer

This project was completed as part of a cybersecurity learning and internship exercise.

The activities documented here were limited to reconnaissance and information gathering. No exploitation, unauthorised access or destructive testing was performed.

The findings represent observations made during the practical exercise and should not be interpreted as confirmation of exploitable vulnerabilities.

All security testing should be conducted with appropriate authorisation and within an agreed scope.
# **Network Scanning with Zenmap**

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
