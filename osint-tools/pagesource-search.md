---
description: >-
  Tool Description: A search engine for the raw HTML and first-party JavaScript
  of crawled websites.
---

# PageSource Search

| **Tool name**    | **Quick Overview**                                                                                                                                              |
| ---------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| URL              | [https://www.pagesourcesearch.com](https://www.pagesourcesearch.com)                                                                                            |
| What it does     | Searches stored website source code (HTML and first-party JavaScript) for exact strings or regular expressions and lists the matching sites, grouped by domain. |
| How to use it    | Type an exact, case-sensitive string, or switch to regex mode under Filters. Then open a match to see it highlighted in the stored file.                        |
| Cost             | Free.                                                                                                                                                           |
| Account required | No. The JSON API needs a key, which is issued on request.                                                                                                       |
| Cookies          | Google Analytics 4 (GA4) cookies.                                                                                                                               |
| Ownership        | Independent project. The operator's company and location are not published.                                                                                     |
| Use in Reporting | Linking websites through shared code, tracking IDs, scripts or injected snippets, and finding every crawled site that carries a known indicator.                |

### What does PageSource Search do?

PageSourceSearch crawls websites and stores the exact bytes of each site's HTML pages and of the JavaScript the site serves from its own hosts. The index covers that stored source rather than the visible text of pages. A query returns every crawled site whose source contains the given string or matches the given pattern.

For each site, the crawler fetches robots.txt, the home page, up to four more pages linked from it, and the first-party scripts those pages load (following imports up to three levels deep). Library code such as jQuery or React is recognised and left out of the index, so matches reflect each site's own code.

Results are grouped by domain, then by file. Each match shows a snippet, its byte offset and its line number. It links to the stored file with the match highlighted, the URL it was fetched from and the time of the fetch. Sites are recrawled about once a week, and earlier versions of a stored file are kept when its content changes.

**The lowdown:** It searches the source code of websites rather than their visible page text.

### How to Use:

**1. Type an exact string, for example a tracking ID such as UA-1234567 or a distinctive code fragment. Literal queries match byte for byte and are case-sensitive.**

<img src="../.gitbook/assets/unknown (656).png" alt="" height="139" width="602">

To use a regular expression, open Filters and set mode to regex. The syntax is .NET. The pattern must contain a fixed run of at least 3 characters. Start the pattern with (?i) for a case-insensitive match.

Separate terms with spaces to require all of them (up to 8). With "Same site" (the default), the terms may appear anywhere on one domain. With "Same page", they must all be in one file. Put a phrase in double quotes to keep its spaces.

**2. Narrow the results with the "kind" filter (html, js or inline\_js) and the "since" filter (collection date).**<br>

<img src="../.gitbook/assets/unknown (657).png" alt="" height="81" width="602">

**3. Open a result to see the stored file with each match highlighted. Tick "every domain (slower)" to count and page through every matching site.**

<img src="../.gitbook/assets/unknown (658).png" alt="" height="281" width="602">

The full query syntax is available here: [https://www.pagesourcesearch.com/help](https://www.pagesourcesearch.com/help)

### Cost

* [x] Free
* [ ] Partially Free
* [ ] Paid

## Data Processing

### Account Required:

* [ ] Yes
* [x] No

No account needed.&#x20;

The JSON API needs a key, which is issued on request.

### Cookies:&#x20;

The site uses Google Analytics 4 cookies for website usage measurement.

### Use in Reporting

PageSourceSearch can be useful for:

* Attribution and network mapping: searching  for an analytics, tag-manager, advertising or site-verification ID to list other crawled sites that carry the same ID. This is a common technique in influence-operation research.
* Indicator hunting: searching for a malicious script marker, an injected snippet or a compromised third-party host to find every crawled site still serving it.
* Recon: finding sites that expose a given endpoint, source-map reference, framework version string or copied template code.
* Corroboration: each match links to the stored file with its URL and fetch time, which can be cited alongside a live check or an archived copy.

**Note:** The index was only first built in September 2026. Bellingcat describes the ID-pivot method [here.](https://www.bellingcat.com/res%20ources/2024/01/09/using-the-wayback-machine-and-google-analytics-to-uncover-disinformation-networks/)

| **Capabilities**                                                                                                       | **Limitations**                                                                                                                                                           |
| ---------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| Exact byte-for-byte search over stored HTML and first-party JavaScript.                                                | The index is new (first crawl September 2026). Its coverage is smaller than long-running engines such as PublicWWW, and there is no history before the first crawl.       |
| .NET regular-expression search, including case-insensitive (?i).                                                       | It stores at most 5 pages per site (the home page plus up to 4 linked pages) and first-party scripts only. Scripts on public CDNs or tag hosts are noted but not fetched. |
| Up to 8 terms combined within one site or within one file                                                              | It does not execute JavaScript, so content rendered client-side is not captured. CSS, images and fonts are not stored.                                                    |
| Results grouped by domain, each with a snippet, byte offset, line number and a highlighted preview of the stored file. | Sites are recrawled about weekly, so results can be days old. Confirm with a live check before reporting.                                                                 |
| Filters for file kind (page, script file, inline script) and collection date.                                          | Sites that block the crawler in robots.txt, or answer it with a bot challenge, are missing.                                                                               |
| Library code (jQuery, React, etc.) kept separate from site code, plus a library filter.                                | Literal queries are case-sensitive. A regex needs a fixed run of 3 characters. Very common strings are rejected, and large result counts can be estimated ("about N").    |
| Earlier versions of stored files kept across weekly recrawls.                                                          | A literal that straddles two stored chunks of a file is not found.                                                                                                        |

### Summary

PageSourceSearch is most useful in the pivot and discovery stage of the OSINT workflow: going from one website, identifier or indicator to the other sites that share it, then verifying each lead with live checks and archives. Its main value is exposing information that may not appear in visible webpage text, particularly source-code fingerprints, tracking identifiers and historical changes.

However, remember a shared script, tracking ID, host or code fragment may indicate a relationship but does not by itself prove common ownership or control.

### Ownership

PageSourceSearch is an independent project. The operator's company and location are not published on the site. The crawler identifies itself as PageSourceSearchBot and is documented at [https://www.pagesourcesearch.com/about](https://www.pagesourcesearch.com/about)

### Ethical Considerations

* The index holds only what websites serve publicly, but page source can contain personal data (names, email addresses, account IDs) or leaked secrets. Do not republish such data beyond what the investigation needs.
* A shared identifier suggests common ownership but does not prove it: IDs get copied between templates, agencies and cloned sites. Corroborate before attributing.
* If a search surfaces compromised or vulnerable sites, notify the owners before publishing details.
* Queries travel in the URL, so do not paste sensitive values as queries.
* Site owners can opt out through robots.txt.

### Related Tools:

* [PublicWWW](publicwww.md)
* NerdyData
* [urlscan.io](urlscan.md)
* BuiltWith
* DNSlytics
* SpyOnWeb

#### Sources

[https://www.pagesourcesearch.com/](https://www.pagesourcesearch.com/)

&#x20;[https://www.pagesourcesearch.com/help](https://www.pagesourcesearch.com/help)&#x20;

[https://www.pagesourcesearch.com/about](https://www.pagesourcesearch.com/about)

[https://www.bellingcat.com/resources/2024/01/09/using-the-wayback-machine-and-google-analytics-to-uncover-disinformation-networks/](https://www.bellingcat.com/resources/2024/01/09/using-the-wayback-machine-and-google-analytics-to-uncover-disinformation-networks/)<br>

_With thanks to Jim for submitting this tool to the OSINT Tool Library._

<br>
