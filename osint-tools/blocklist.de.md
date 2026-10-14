---
description: >-
  Tool Description : A free threat-intelligence and abuse-reporting service that
  collects reports of malicious or abusive activity against participating
  systems.
---

# blocklist.de

| **blocklist.de** | **Quick Overview**                                                                                                                                                  |
| ---------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| URL              | [https://www.blocklist.de/en/index.html](https://www.blocklist.de/en/index.html)                                                                                    |
| What it does     | Collects and publishes reports of attacks and abusive activity against participating systems so you can search IP addresses and ASNs and examine attack history.    |
| How to use it    | Search an IP address or ASN, review attack history and service type, and use the DNS/RBL, API or downloadable lists for larger-scale technical investigation.       |
| Cost             | Free for normal searches and reporting.                                                                                                                             |
| Account required | No for public IP/ASN searches and basic data access. Yes for submitting reports and managing reporting servers.                                                     |
| Cookies          | A Cloudflare security cookie.                                                                                                                                       |
| Ownership        | Not publicly disclosed. Operated as a free and voluntary service by a fraud/abuse specialist.                                                                       |
| Use in Reporting | iInvestigating suspicious IP addresses, infrastructure, brute-force activity, attack history, malicious services and potential relationships between IPs and ASNs.  |

### What does blocklist.de do?

blocklist.de collects attack reports from participating systems and publishes information about IP addresses that have attacked those systems. The service covers activities such as SSH attacks, mail-login attacks, FTP attacks, web-server attacks, bots, brute-force logins, SQL injection and other categories supported by its reporting system.

You can search an IP address or AS number and see information such as the service targeted, last attack, number of attacks, number of reports and whether the IP is currently listed/blocked.

Its standard export lists contain IP addresses that have attacked participating systems or partners during the previous 48 hours and have not used the available delisting mechanism.

**The lowdown:** It’s an IP-based abuse and attack-history intelligence source which is able to take a suspicious IP address and determine whether it has been reported for activity.

### How to Use:

**1. Search the IP address or ASN using the search function. Review the returned IPs, services, attack dates, attack counts, reports and current status.**

<img src="../.gitbook/assets/unknown (717).png" alt="" height="300" width="602">

**2. Open the relevant IP's history and examine the reported service and attack timeline. Compare the information with other infrastructure intelligence such as WHOIS/RDAP, ASN information, passive DNS and other reputation databases.**

<img src="../.gitbook/assets/unknown (718).png" alt="" height="392" width="602">

**You can also view stats for the last month on reported attacks as below:**

<img src="../.gitbook/assets/unknown (719).png" alt="" height="355" width="602">

**3. For technical or large-scale investigations, use the DNS/RBL, downloadable lists or API. The API permits IP queries without an API key, while queries relating to a user's or server's statistics require the appropriate credentials.**

### Cost

* [x] Free
* [ ] Partially Free
* [ ] Paid

Free for normal searches and reporting. Very large-volume list downloads may be subject to restrictions.&#x20;

## Data Processing

### Account Required:

* [x] Yes
* [x] No

No for public IP/ASN searches and basic data access. Yes for submitting reports and managing reporting servers.

### Cookies:&#x20;

The site uses a Cloudflare security cookie used to retain proof that the browser has passed a Cloudflare security/anti-bot challenge.

### Use in Reporting

blocklist.de can be useful for:

* Investigating whether an IP address has previously been reported for malicious or abusive activity.
* Identifying the types of services targeted by a suspicious IP.
* Establishing an attack timeline using reported attack dates and times.
* Identifying repeated or high-volume attack activity associated with an IP address.
* Investigating groups of suspicious IP addresses through ASN searches.
* Identifying infrastructure associated with SSH, FTP, mail, web, SIP and brute-force activity.
* Checking whether an IP appears in blocklist.de's current attacker lists.
* Correlating blocklist.de findings with WHOIS/RDAP, ASN, DNS and other infrastructure intelligence.
* Generating investigative leads for compromised servers, bot activity and hostile infrastructure.
* Supporting reporting about cyber incidents by providing an additional independent source of historical attack indicators.
* Preserving the IP, ASN, service, attack date, report count and retrieval date as part of an evidence trail.

As a working example, an OVHcloud Trust & Safety investigation published by [Abuse.watch in April 2023](https://abuse.watch/2023/04/23/abuse-vxvfrldwrs-abusive-use-of-your-service-ns3034758-ip-91-121-81-eu/) reproduced an automated abuse report from blocklist.de concerning IP address 91.121.81.184. The blocklist.de report identified the activity as a login-attack against an apacheddos service and included timestamps, the source IP, destination port and HTTP request logs. OVHcloud's Trust & Safety team subsequently warned the hosting provider about the reported activity.

| **Capabilities**                                                                           | **Limitations**                                                                                                                                |
| ------------------------------------------------------------------------------------------ | ---------------------------------------------------------------------------------------------------------------------------------------------- |
| Searches IP addresses and ASNs for reported attack activity.                               | A listing is an indicator/report, not proof that the IP owner intentionally carried out an attack.                                             |
| Provides attack types, services, dates, counts and report information.                     | Coverage depends on attacks observed and reported by participating systems.                                                                    |
| Provides downloadable attacker-IP lists covering recent activity.                          | Standard export lists primarily cover the previous 48 hours.                                                                                   |
| Provides DNS/RBL access and an HTTP API for technical integration.                         | API and list data should be interpreted according to blocklist.de's reporting methodology                                                      |
| Covers multiple attack categories including SSH, mail, FTP, web and brute-force activity.  | IP addresses may represent compromised machines, shared infrastructure, VPNs, proxies or other intermediaries rather than the ultimate actor.  |

### Summary

blocklist.de is is particularly useful during the collection, verification and analysis stages of an OSINT investigation.&#x20;

A useful workflow is to start with a suspicious IP, check its blocklist.de history, identify the relevant service and attack dates, investigate the associated ASN, and then corroborate the finding using independent infrastructure and threat-intelligence sources.&#x20;

### Ownership

Not publicly disclosed. The [website](https://www.blocklist.de/en/index.html) describes itself as a free and voluntary service provided by a fraud/abuse specialist.&#x20;

### Ethical Considerations

* Do not automatically attribute activity to the organisation or individual associated with an IP address.
* Be careful when interpreting ASN-level results as an ASN can contain many unrelated customers or systems.
* Do not treat a blocklist.de listing as proof that an entire hosting provider or network is malicious.
* Avoid publishing unnecessary personal information associated with IP addresses.
* When reporting cyber incidents, distinguish between observed activity, reported activity and attribution.

### Related Tools:

* Spamhaus
* GreyNoise
* [AlienVault OTX](alien-vault-otx.md)
* [VirusTotal](virustotal.md)

#### Sources

[https://www.blocklist.de/en/index.html](https://www.blocklist.de/en/index.html)&#x20;

[https://abuse.watch/2023/04/23/abuse-vxvfrldwrs-abusive-use-of-your-service-ns3034758-ip-91-121-81-eu/](https://abuse.watch/2023/04/23/abuse-vxvfrldwrs-abusive-use-of-your-service-ns3034758-ip-91-121-81-eu/)&#x20;
