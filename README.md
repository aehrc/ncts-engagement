
# NCTS Engagement and Education

This site is a practical introduction to the **National Clinical Terminology Service (NCTS)** in Australia, focusing on **SNOMED CT**, **FHIR terminology**, and **terminology servers** (including **Ontoserver**). It includes quickstarts, examples, and references for new starters. Intended to cover the gist of these components you can read this page through in 5 minutes; or use CTRL (or CMD)+F to find keywords of interest.

---

<details>
<summary>1) Support</summary>

This project is run by **James Grant** — `james.grant@csiro.au`.  
If you have additional queries or questions, send me an email!

More broadly, the NCTS is supported by the **Australian Digital Health Agency (ADHA)** with input from **CSIRO**.  
General contact: `ncts@digitalhealth.gov.au`.

</details>

---

<details>
<summary>2) What is the NCTS?</summary>

The **NCTS** provides national clinical terminology services and content for Australia:
- **SNOMED CT-AU** (Australian edition and extension).
- **AMT (Australian Medicines Terminology)** and other curated content.
- Hosted **terminology services** and **syndication** options for local hosting.
- Guidance on **FHIR terminology operations** and best-practice use.

See the overview: /snomed/overview.md

</details>

---

<details>
<summary>3) Core Components Introduction</summary>

### SNOMED CT (a clinical terminology)

SNOMED CT:
- Is the most comprehensive and precise, multilingual health terminology in the world.
- Developed collaboratively to meet diverse global medical needs.
- Assists with the electronic exchange of clinical health information.
- Can be mapped to other coding systems (ICD-9, ICD-10) for semantic interoperability.
- Accepted as a common global language for health terms in over 50 countries.
- Provides extensive, scientifically validated clinical content.

Learn more: /snomed/snomed-ct.md

### FHIR (a [data] standard)
*TBC*

### The NCTS (an Australian Government service)
*TBC*

</details>

---

<details>
<summary>4) Benefits & Use Cases</summary>

High-level: /snomed/benefits/general.md  
Details:
- Providers: [/snomed/benefits/benefits-providers.md](/snomed/benefits/benefits-providers.mdtients.md
- Vendors: [/snomed/benefits/benefits-vendors.md](/snomed/benefmed/benefits/benefits-global.md](/snomed/benefits/benefits
<summary>5) Getting Started</summary>

**Explore SNOMED CT**
- Use **Shrimp** to browse concepts, relationships, hierarchies, and AU extension content.  
  Guide: /tools/shrimp.md

**Query SNOMED CT via NCTS**
- Try **Postman** with FHIR endpoints and ECL queries.  
  Quickstart: /quickstarts/postman-ecl.md

**Understand FHIR structures**
- Learn **CodeSystem**, **ValueSet**, **ConceptMap**, and bindings.  
  Tutorial: /fhir/terminology-basics.md

</details>

---

<details>
<summary>6) Hosting & Integration</summary>

**Host your own copy of SNOMED CT**
- **Syndication** to pull releases; **Docker** to run a local **Ontoserver**.
- Version pinning, indexing, and update strategy.

Guide: /hosting/ontoserver-docker.md

</details>

---

<details>
<summary>7) Practical Topics & FAQs</summary>

- **SNOMED CT vs ICD** (terminology vs classification; analytics vs reporting).
- **ValueSet vs Reference Set** (selection for use vs packaged content/metadata).
- **ECL vs FHIR search** (expressive constraints vs standardized API ops).
- **Release cadence** (International → AU extension; how updates flow to NCTS).
- **Licensing & access** (who can use AU content; endpoint access considerations).

FAQs: [/guides/faqs.md](/guides/faqs.md)  
Glossary: /guides/glossary.md

</details>

---

<details>
<summary>8) References</summary>

- SNOMED CT basics and benefits: SNOMED Docs, [Benefits overview](https://docs.snomed.org/snomed-ct-practical-guides/snomed-ct-starter-guide/2-snomed-ct-benefits)  
- SNOMED International value proposition: [snomed.org/value-proposition](https://www.snomed.org/value-proposition)

</details>
 

<!-- 
Working Graveyard (to delete)
* SEARCH through SP/Slack/Teams for other mentions of Benefits / Use Cases / Case Studies / User Stories.
* Plus general web / articles.
* List of who's known to be using SCT-AU already: https://www.healthterminologies.gov.au/understanding-clinical-terminology-landing/whos-using-snomed-ct-au/ 
* Implementation guide (high-level): https://www.healthterminologies.gov.au/implementing-in-software/getting-started/implementation-whats-involved/ 
* Resources/materials: https://www.healthterminologies.gov.au/document-library/ 
* Other code set relationships (not as relevant here): https://www.healthterminologies.gov.au/understanding-clinical-terminology-landing/the-big-picture-snomed-and-other-code-sets/ 

-->
