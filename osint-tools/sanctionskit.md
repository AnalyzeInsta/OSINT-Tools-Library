---
description: >-
  Tool Description: A sanctions and public-source screening platform to search
  records relating to people, organisations, vessels and aircraft.
---

# SanctionsKit

| **SanctionsKit** | **Quick Overview**                                                                                                                                        |
| ---------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------- |
| URL              | [https://www.sanctionskit.com/search](https://www.sanctionskit.com/search)                                                                                |
| What it does     | Searches complete name words and aliases across currently available datasets approved for public display, with links to source records and datasets.      |
| How to use it    | Enter a name, open a candidate record, compare identifying details, and check the original source, dates and coverage.                                    |
| Cost             | Partially Free.                                                                                                                                           |
| Account required | No for public search. Yes for the API sandbox and private screening workspace.                                                                            |
| Cookies          | Authentication/security cookies used by WorkOS AuthKit.                                                                                                   |
| Ownership        | Operated by SanctionsKit, LLC.                                                                                                                            |
| Use in Reporting | Useful for sanctions research, restricted-party screening, source verification, counterparty research and documenting evidence behind a potential match.  |

### What does SanctionsKit do?

SanctionsKit’s public search helps researchers locate records by complete name words and aliases across datasets currently available for public display. Results identify the dataset and source publisher and link to a record page with available source details. The dataset and coverage pages provide scope and availability context.&#x20;

Public lookup does not calculate a screening score or create a retained customer screening. The separate authenticated API and dashboard support screening and review workflows; the free API sandbox contains invented records, while production screening requires a paid plan.&#x20;

**Note:** This submission concerns the public lookup at /search.

**The lowdown:** The public search allows you to search names and aliases across currently available public datasets. <br>

### How to Use:

**1. Enter a publicly known person, organization, vessel or aircraft name. Use complete name words or an alias. Do not enter confidential screening subjects in this public interface. (You don’t need to sign in to use the public search).**

<img src="../.gitbook/assets/unknown (653).png" alt="" height="144" width="602">

**2. Review the candidate records and their dataset/source labels.**

<img src="../.gitbook/assets/unknown (654).png" alt="" height="465" width="602">

**3. Open a record and compare the available identifying details. Follow its source references to the original publisher.**

<img src="../.gitbook/assets/unknown (655).png" alt="" height="288" width="602">

**4. Check the dataset page and** [**https://www.sanctionskit.com/coverage**](https://www.sanctionskit.com/coverage)  **for scope and current availability. Record the source URL, source/record identifier and access date for your research. Corroborate identity and current status independently before reporting a conclusion.**<br>

### Cost

* [ ] Free
* [x] Partially Free
* [ ] Paid

Public name lookup is free. API testing uses a free synthetic sandbox. Production screening and review workflows through the Dashboard require a paid plan.

## Data Processing

### Account Required:

* [x] Yes
* [x] No

No account for public search. An account is required for the API sandbox and private screening workspace.

### Cookies:&#x20;

The site uses WorkOS AuthKit for authenticated sessions. Testing identified wos-auth-verifier-\*, a temporary cookie used to secure the OAuth/PKCE sign-in process, and wos-session, an encrypted session cookie used to maintain authentication.

### Use in Reporting

SanctionsKit can be useful for:

* Checking whether a person, organisation, vessel or aircraft appears in relevant sanctions or restricted-party records.
* Identifying the government, regulator or other authority responsible for a particular record.
* Comparing records across different datasets and jurisdictions.
* Tracing a result back to the underlying source evidence for verification.
* Supporting due-diligence, counterparty, corporate and investigative research.
* Documenting potential matches and the evidence considered during review.
* Providing an auditable source trail for reporting, while keeping the distinction between a database result and a verified identity finding.

| **Capabilities**                                                                | **Limitations**                                                                                 |
| ------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------------- |
| Public name and alias lookup without an account.                                | Public lookup matches complete name words and aliases; it does not calculate a screening score. |
| Candidate records linked to datasets and source publishers.                     | Only currently available datasets approved for public display are searched.                     |
| Record pages expose available identifying details and source references.        | A shared name does not establish identity, wrongdoing or current sanctions status.              |
| Dataset and coverage pages explain scope and current availability.              | The same subject may have separate records in multiple datasets.                                |
| Separate API and dashboard workflows for structured screening and human review. | Source records can be incomplete, outdated or disputed; verify the original publisher.          |
| <p><br></p>                                                                     | Public search queries are exposed in the page URL.                                              |

### Summary

SanctionsKit is useful for locating public-source candidate records and following their provenance during preliminary research. Its strengths are accessible name lookup and source context. Its limits are name ambiguity, source-specific coverage and freshness, and lack of confidential-query handling in the public interface. It’s best used to find and corroborate leads before drawing identity or legal conclusions.

**Note:** The platform itself states that screening supports informed review rather than making a legal clearance decision.

### Ownership

SanctionsKit LLC based in the United States. It’s an independent business that states it is not affiliated with the government agencies, regulators, publishers or other organisations whose records appear in the service.&#x20;

### Ethical Considerations

* Corroborate identifying details before associating a person with a record.
* The appearance in a public dataset does not establish wrongdoing.
* Respect source-specific licences, privacy rights and correction mechanisms.
* Avoid sharing unnecessary personal information in reports or query URLs.
* Check dates and the original source before presenting a restriction as current.

### Related Tools:

* [OpenSanctions](open-sanctions.md)
* OFAC Sanctions List Search
* [EU Sanctions Map](eu-sanctions-map.md)
* [OpenCorporates](opencorporates.md)

#### Sources

[https://www.sanctionskit.com/search](https://www.sanctionskit.com/search)&#x20;

[https://www.sanctionskit.com/datasets](https://www.sanctionskit.com/datasets)

[https://www.sanctionskit.com/coverage](https://www.sanctionskit.com/coverage)

[https://www.sanctionskit.com/coverage/limitations](https://www.sanctionskit.com/coverage/limitations)

[https://www.sanctionskit.com/privacy](https://www.sanctionskit.com/privacy)

[https://www.sanctionskit.com/legal-notice](https://www.sanctionskit.com/legal-notice)

[https://www.sanctionskit.com/pricing](https://www.sanctionskit.com/pricing)

[https://www.sanctionskit.com/docs/quickstart](https://www.sanctionskit.com/docs/quickstart)<br>

_With thanks to Adam Smith for submitting this tool to the OSINT Tool Library._
