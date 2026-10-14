---
description: 'Tool Description: An open search engine for domain research and OSINT recon.'
---

# cl0q

| **cl0q**         | **Quick Overview**                                                                                                                                      |
| ---------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------- |
| URL              | [https://cl0q.com/](https://cl0q.com/)                                                                                                                  |
| What it does     | Searches an index of 38.5M scanned domains and 24.8M pages for domain research, favicon lookup, and OSINT recon.                                        |
| How to use it    | Enter a domain, keyword, or favicon hash in the search box at cl0q.com, or query the free API following [https://cl0q.com/docs](https://cl0q.com/docs). |
| Cost             | Free.                                                                                                                                                   |
| Account required | No.                                                                                                                                                     |
| Cookies          | None noted but analysts should review the site's privacy notice before use.                                                                             |
| Ownership        | Operated by [@chrisknowshtml](https://x.com/chrisknowshtml) on X.                                                                                       |
| Use in Reporting | Web discovery, infrastructure mapping, domain research, passive subdomain discovery and identifying links between websites.                             |

### What does cl0q do?

cl0q is an open search engine built for domain research and OSINT recon. It operates a distributed crawler network that has scanned 38.5M domains (working toward a 100M-domain goal) and indexed 24.8M pages.&#x20;

Analysts can search the index by domain, keyword, or favicon to investigate website infrastructure, discover related sites, and support reconnaissance workflows.&#x20;

Documentation is published at [https://cl0q.com/docs/](https://cl0q.com/docs/) and a free API tier is offered.

**The lowdown:** Its main OSINT value is connecting a conventional web search to infrastructure-level pivots, particularly IP/ASN/CNAME and favicon-hash relationships.&#x20;

### How to Use:

**1. Simply enter a domain, keyword, or favicon hash in the search box.**

<img src="../.gitbook/assets/unknown (707).png" alt="" height="285" width="602">

**2. Review results to pivot between domains and pages during an investigation.**

<img src="../.gitbook/assets/unknown (708).png" alt="" height="484" width="602">

**Refine results by using the search tips as below:**

<img src="../.gitbook/assets/unknown (709).png" alt="" height="340" width="602">

&#x20;**3. For automation, use the free API tier (30 requests/minute, 1,000/day) following the documentation at https://cl0q.com/docs/**&#x20;

### Cost

* [x] Free
* [ ] Partially Free
* [ ] Paid

## Data Processing

### Account Required:

* [ ] Yes
* [x] No

### Cookies:&#x20;

Not noted during our site session on 29 September 2026. Analysts should review the site's privacy notice before use.

### Use in Reporting

Cl0q can be useful for:

* Discovering publicly indexed websites, pages and domains relevant to an investigation.
* Mapping websites sharing the same IP address, ASN, organisation or CNAME infrastructure.
* Using favicon hashes to identify other domains serving the same icon and generate infrastructure leads.
* Conducting passive subdomain discovery without actively probing the target's infrastructure.
* Identifying connections between websites, hosting networks and related infrastructure requiring further investigation.
* Supporting domain attribution and infrastructure research in investigative reporting.
* Providing a route to original webpages and technical metadata that can then be independently verified and cited.

| **Capabilities**                            | **Limitations**                                                             |
| ------------------------------------------- | --------------------------------------------------------------------------- |
| Domain search across 38.5M scanned domains. | Corpus covers 38.5M of the stated 100M-domain goal, so coverage is partial. |
| Page search across 24.8M indexed pages.     | Index freshness/recency is not publicly documented.                         |
| Favicon search for infrastructure pivoting. | Free API rate limits (30 req/min, 1,000/day) constrain bulk use.            |
| Deep-dive domain investigation views.       | No public information on data retention or historical depth.                |
| Free API tier (30 req/min, 1,000/day).      | <p><br></p>                                                                 |

### Summary

Cl0q is most useful in the discovery/reconnaissance phase of the OSINT workflow, for domain research and infrastructure mapping.

**Note:** Shared infrastructure, favicons or hosting organisations can indicate a possible relationship, but they do not by themselves establish common ownership or malicious activity. Its own documentation describes the favicon-hash capability as an OSINT pivot, while noting that shared icons can also result from common frameworks or default assets.&#x20;

### Ownership

cl0q is operated under the cl0q name. Country of origin and company base are not publicly stated.

Contact details are: [@chrisknowshtml ](https://x.com/chrisknowshtml)on X and cl0qsearch@gmail.com.

### Ethical Considerations

* Only query domains in the context of legitimate investigations; avoid using results for doxxing or harassment.
* Verify findings with independent sources before including them in reports.
* Respect the site's terms of service and API rate limits.
* Be mindful that indexed data may include stale or inaccurate information.

### Related Tools:

* [urlscan.io](urlscan.md)
* SecurityTrails
* [Shodan](shodan.md)
* [Censys](censys.md)
* crt.sh

#### Sources

[https://cl0q.com/](https://cl0q.com/)&#x20;

[https://x.com/chrisknowshtml](https://x.com/chrisknowshtml)&#x20;



_With thanks to the Cl0q team for submitting this tool to the OSINT Tool Library._

<br>
