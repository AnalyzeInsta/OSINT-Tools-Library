---
description: >-
  Tool Description : A browser-based domain and network intelligence platform
  that helps researchers examine a domain's public registration, DNS and TLS
  certificate information.
---

# CC.LA

| **CC.LA**        | **Quick Overview**                                                                                                                                                                                    |
| ---------------- | ----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| URL              | [https://cc.la/](https://cc.la/)                                                                                                                                                                      |
| What it does     | Displays WHOIS/RDAP registration records, DNS records, IP registration data and TLS certificate details.                                                                                              |
| How to use it    | Enter a public domain or IP in the relevant lookup tool, then compare the registration, DNS and certificate results.                                                                                  |
| Cost             | Free for core lookups. Paid account available for further functionality.                                                                                                                              |
| Account required | No for basic lookups. Yes for saved account features and monitoring.                                                                                                                                  |
| Cookies          | Auth.js security cookie, Google Analytics, and Google advertising-related cookies.                                                                                                                    |
| Ownership        | Independently maintained CC.LA; submitted by its maintainer, tinyhill.                                                                                                                                |
| Use in Reporting | Useful for researching domain registration, ownership information where publicly available, DNS infrastructure, IP addresses, nameservers, domain history, certificates and network characteristics.  |

### What does CC.LA do?

CC.LA is a browser-based domain and network research service. WHOIS and RDAP show the public registration fields returned by registries and registrars. DNS lookup shows record sets, and certificate lookup reports the certificate served by a host, including issuer and validity dates. IP WHOIS provides network registration information.&#x20;

For OSINT investigations, it can provide an initial picture of who appears to operate a domain, when it was registered, which registrar and nameservers are involved, where DNS points, what infrastructure is associated with it and whether historical changes have been observed.&#x20;

**The lowdown:** It’s essentially a domain and infrastructure reconnaissance tool.&#x20;

### How to Use:

**1. Type a target domain into the search bar or open** [**https://cc.la/whois/example.com**](https://cc.la/whois/example.com) **to inspect an example domain's public registration fields:**

<img src="../.gitbook/assets/unknown (679).png" alt="" height="216" width="602">

**2. Use the DNS Records tab, or https://cc.la/dns/example.com to inspect nameservers and DNS answers.**

<img src="../.gitbook/assets/unknown (680).png" alt="" height="428" width="602">

**3. View the certificates tab or open https://cc.la/certificates/example.com to compare the certificate issuer and validity dates for the example:**

<img src="../.gitbook/assets/unknown (681).png" alt="" height="424" width="602">

**4. Keep registration dates separate from certificate dates. Record the observation time and data source when documenting findings.**

**Note:** Make sure to corroborate important findings with authoritative records. Missing data is not proof of an unregistered domain, and an issued certificate is not proof that a website is trustworthy.

### Cost

* [ ] Free
* [x] Partially Free
* [ ] Paid

Core lookups are free. Optional account features and paid Pro monitoring are available.

## Data Processing

### Account Required:

* [x] Yes
* [x] No

No for basic lookups. Yes for saved account features and monitoring.

### Cookies:&#x20;

The site uses Auth.js security cookies for CSRF protection and authentication-flow management, alongside Google Analytics cookies for usage measurement and Google advertising-related cookies.

### Use in Reporting

CC.LA can be useful for:

* Identifying the registrar associated with a domain.
* Establishing domain creation, update and expiration dates.
* Examining publicly available registrant information where it has not been redacted.
* Identifying nameservers and associated DNS infrastructure.
* Mapping A, AAAA, MX, CNAME, TXT and other DNS records.
* Identifying IP addresses associated with domains.
* Reviewing historical WHOIS and DNS observations for evidence of infrastructure changes.
* Investigating changes to registrars, nameservers or domain-status records.
* Examining SSL/TLS certificate information and certificate-expiry issues.
* Investigating network reachability, latency, packet loss and routing from CC.LA's measurement infrastructure.
* Identifying infrastructure relationships that warrant further investigation.
* Monitoring domains for DNS, uptime and certificate changes where appropriate.
* Providing supporting technical evidence that can be cross-checked against registries, registrars, DNS providers and other authoritative sources.

A worked public example is [https://cc.la/whois/example.com](https://cc.la/whois/example.com) together with its DNS and certificate pages, as above.

**Important Reporting Note:** Shared infrastructure, privacy-redacted records and certificate issuance do not establish common ownership or malicious intent.

| **Capabilities**                                                       | **Limitations**                                                                     |
| ---------------------------------------------------------------------- | ----------------------------------------------------------------------------------- |
| Public WHOIS and RDAP domain registration lookups.                     | Results may be cached, rather than live on every visit.                             |
| DNS record inspection and IP WHOIS.                                    | Coverage and fields depend on registries, registrars and other upstream services.   |
| Host-specific TLS certificate issuer and validity lookup.              | Contact information may be redacted; history is incomplete and observation-based.   |
| Links between related views for the same domain.                       | A failed or empty lookup does not prove that a domain is unregistered.              |
| Limited historical observations and optional account-based monitoring. | <p>DNS and network observations can differ by location and resolver.</p><p><br></p> |
| No installation or account required for basic public lookups.          | Not a malware scanner, owner-identification service, or safety verdict.             |
| <p><br></p>                                                            | Analytics, ads and server-side processing are relevant to operational security.     |

### Summary

CC.LA is a convenient first-pass collection tool for public domain, DNS and certificate information, useful for comparing records in one browser workflow. An investigator can start with a domain, identify registration and DNS information, pivot to associated IP addresses and nameservers, examine historical changes and then use those findings to identify additional domains or infrastructure for further investigation.&#x20;

However, researchers must account for caching, incomplete history, redacted fields and measurement location, and independently corroborate attribution or security conclusions.

### Ownership

CC.LA is independently maintained. This submission is from its maintainer using the public handle tinyhill. The public site account is [https://x.com/ccdotla](https://x.com/ccdotla) and the maintenance contact is [https://cc.la/contact](https://cc.la/contact).

### Ethical Considerations

* Use public records lawfully and avoid publishing unnecessary personal information.
* Do not infer identity, common ownership or wrongdoing solely from shared infrastructure.
* Use active diagnostics only where appropriate and authorised.
* Preserve source and observation time, and disclose caching or missing coverage.
* Corroborate conclusions before publication.

### Related Tools:

* ICANN Lookup
* [CentralOps Domain Dossier](central-ops.md)
* [who.is](whois-api.md)

#### Sources

[https://cc.la/](https://cc.la/)&#x20;

[https://cc.la/about](https://cc.la/about)&#x20;

[https://cc.la/whois/example.com](https://cc.la/whois/example.com)&#x20;

[https://cc.la/rdap/example.com](https://cc.la/rdap/example.com)&#x20;

[https://cc.la/dns/example.com](https://cc.la/dns/example.com)&#x20;

[https://cc.la/certificates/example.com](https://cc.la/certificates/example.com)&#x20;

[https://cc.la/website-monitoring](https://cc.la/website-monitoring)&#x20;

[https://cc.la/contact](https://cc.la/contact)&#x20;



_With thanks to tinyhill for submitting this tool to the OSINT Tool Library_.
