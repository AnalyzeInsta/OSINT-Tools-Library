---
description: >-
  Tool Description: A free online service for exploring DNS records by CIDR, ASN
  or domain wildcards.
---

# ActiveDNS

| **ActiveDNS**    | **Quick Overview**                                                                                                                                   |
| ---------------- | ---------------------------------------------------------------------------------------------------------------------------------------------------- |
| URL              | [https://activedns.net/](https://activedns.net/)                                                                                                     |
| What it does     | Searches observed DNS resolutions by domain, IP/CIDR or ASN and supports subdomain, reverse-IP and infrastructure research.                          |
| How to use it    | Enter a query into the search bar and run the search. Review the findings and pivot into the results to explore more of the target's infrastructure. |
| Cost             | Free.                                                                                                                                                |
| Account required | No.                                                                                                                                                  |
| Cookies          | None.                                                                                                                                                |
| Ownership        | [Erlend Leiknes](https://www.linkedin.com/in/erlend-leiknes/)                                                                                        |
| Use in Reporting | Domain and infrastructure discovery, subdomain enumeration, reverse-IP research, hosting analysis and tracking newly observed DNS relationships.     |

### What does ActiveDNS do?

ActiveDNS is an online service that aims to provide an accurate picture of the internet's DNS records. Access to its database is provided by an intuitive search interface on its webpage.

It is particularly useful for infrastructure mapping and pivoting. Results are displayed newest first, allowing investigators to identify recently observed infrastructure, while CNAME-chain support provides additional context on how domains connect to other names and addresses.&#x20;

**The lowdown:** It’s a DNS-intelligence search engine that shows which domains resolve to which IP addresses, which domains sit behind an IP or network, and what has recently been observed within an ASN.&#x20;

### How to Use:

**1. Search a domain e.g. \`”example.com” (or an exact name such as \`www.example.com) into the search box and press Search or Enter. The mode switches automatically if you type an address or an ASN instead of what associations ActiveDNS have been able to find.**

<img src="../.gitbook/assets/unknown (650).png" alt="" height="211" width="602">

**2. Read the results. Each row is one name → address observation: domain, IP, IP version, ASN, country and the time it was observed (UTC), newest first. Load more pages, or download the loaded records as CSV.**

<img src="../.gitbook/assets/unknown (651).png" alt="" height="333" width="602">

**3. Pivot. Click an IP address to see everything else that resolves to it, or an ASN to see everything in that network. The URL updates with every search, so a finding can be shared as a link.**

<img src="../.gitbook/assets/unknown (652).png" alt="" height="420" width="602">

### Cost

* [x] Free
* [ ] Partially Free
* [ ] Paid

## Data Processing

### Account Required:

* [ ] Yes
* [x] No

### Cookies:&#x20;

Privacy friendly. No external tracking. Self-hosted privacy friendly analytics.

No cookies noted during our site session on 1 October 2026.

### Use in Reporting

ActiveDNS can be useful for:

* Identifying subdomains and the IP addresses to which they resolve.
* Finding other domains associated with a particular IP address or network.
* Mapping infrastructure associated with an ASN.
* Tracing CNAME relationships between domains and underlying infrastructure.
* Identifying recently observed DNS relationships and infrastructure changes.
* Supporting investigations into hosting arrangements, domain infrastructure and attack-surface exposure.
* Providing timestamped DNS observations that can be corroborated with other technical sources before inclusion in reporting.

The service was developed during [the hunt for Darcula](https://www.mnemonic.io/resources/blog/exposing-darcula-a-rare-look-behind-the-scenes-of-a-global-phishing-as-a-service-operation/) in the aid to find infrastructure owned by scammers.

| **Capabilities**                                                                 | **Limitations**                                                   |
| -------------------------------------------------------------------------------- | ----------------------------------------------------------------- |
| CIDR, Domain wildcard and ASN lookup.                                            | CIDR search is limited to /24 networks for IPv4 and /48 for IPv6. |
| Discover subdomains and associated IP addresses.                                 | Wildcard search is subdomain only.                                |
| Shows CNAME chains and domain relationships.                                     | DNS relationships can change and may become stale.                |
| Newest observations are shown first, useful for spotting recent infrastructure.  | Public searches are limited to 100 records per page .             |
| Can export search results as CSV.                                                | No API access on public pages.                                    |

### Summary

ActiveDNS is an ideal tool for finding domain names by ASN, CIDR or wildcards for domains that are active. It fits primarily into the discovery and analysis stages of the OSINT workflow, with a strong infrastructure pivoting role.

A fast and accurate database is at the cost of access to historical DNS records. It aims to have a complete picture of DNS records for 90 days.

### Ownership

ActiveDNS is a project made to solve DNS recon up front and is a free service to the security community. The tool is made by [Erlend Leiknes ](https://www.linkedin.com/in/erlend-leiknes/)who works as a security consultant in the Norwegian cyber security company mnemonic.

### Ethical Considerations

* Treat shared IP, ASN and CNAME relationships as investigative leads rather than proof of common ownership.
* DNS records may change without ActiveDNS picking them up. Verify that the records are relevant for your work.
* Check the observation timestamp before drawing conclusions about infrastructure at a particular point in time.
* Corroborate important DNS findings with independent sources such as Certificate Transparency, WHOIS/RDAP and historical DNS providers.
* Minimise unnecessary collection or publication of technical or personal information discovered during research.

### Related Tools:

* [Shodan](shodan.md)
* [Censys](censys.md)
* [DNS Dumpster](dns-dumpster.md)

#### Sources

[https://activedns.net/](https://activedns.net/)&#x20;

[https://www.linkedin.com/in/erlend-leiknes/](https://www.linkedin.com/in/erlend-leiknes/)&#x20;

[https://www.mnemonic.io/resources/blog/exposing-darcula-a-rare-look-behind-the-scenes-of-a-global-phishing-as-a-service-operation/](https://www.mnemonic.io/resources/blog/exposing-darcula-a-rare-look-behind-the-scenes-of-a-global-phishing-as-a-service-operation/)&#x20;

[https://alternativeto.net/software/activedns/about/](https://alternativeto.net/software/activedns/about/) <br>

_With thanks to Erlend Leiknes for submitting this tool to the OSINT Tool Library._
