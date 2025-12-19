
# NCTS Engagement and Education

This site is a practical introduction to the **National Clinical Terminology Service (NCTS)** in Australia, focusing on **SNOMED CT**, **FHIR terminology**, and **terminology servers** (including **Ontoserver**). It includes quickstarts, examples, and references for new starters.

**Support**
- Project lead: **James Grant** — `james.grant@csiro.au`
- General NCTS queries: `ncts@digitalhealth.gov.au`
- NCTS is supported by the **Australian Digital Health Agency (ADHA)** with input from **CSIRO**.

---

## 1) What is the NCTS?

The **NCTS** provides national clinical terminology services and content for Australia:
- **SNOMED CT-AU** (Australian edition and extension).
- **AMT (Australian Medicines Terminology)** and other curated content.
- Hosted **terminology services** and **syndication** options for local hosting.
- Guidance on **FHIR terminology operations** and best-practice use.

See the overview: /snomed/overview.md

---

## 2) Core Concepts at a Glance

### SNOMED CT (clinical terminology)
- A comprehensive, precise, multilingual clinical terminology (concepts, descriptions, relationships).
- AU edition builds on **SNOMED CT International**, adding Australian-specific content.
- Designed for **interoperability**, **analytics**, and **decision support**.
- Works with **ValueSets** to define the terms used in specific clinical contexts.

Learn more: /snomed/snomed-ct.md  
Benefits overview: /snomed/benefits/general.md

### FHIR (data standard for interoperability)
- FHIR’s **terminology layer** uses **CodeSystem**, **ValueSet**, and **ConceptMap** resources.
- Key operations: **`$expand`**, **`$validate-code`**, **`$lookup`** against a terminology server.
- Bindings connect clinical data elements to terminology content (e.g., SNOMED CT-AU).

Intro page: /fhir/terminology-basics.md

### Terminology Servers (Ontoserver)
- Provide fast, standards-based access to **SNOMED CT**, **AMT**, and other code systems.
- Support **ECL** (Expression Constraint Language) and **FHIR** terminology operations.
- Common use cases: finding concepts, building/expanding **ValueSets**, validating codes.

Start here: /servers/ontoserver.md

---

## 3) Benefits & Use Cases

High-level: /snomed/benefits/general.md  
Details: 
- Providers: /snomed/benefits/benefits-providers.md  
- Patients: /snomed/benefits/benefits-patients.md  
- Vendors: /snomed/benefits/benefits-vendors.md  
- Global: /snomed/benefits/benefits-global.md

---

## 4) Getting Started (Hands-on)

**Explore SNOMED CT**
- Use **Shrimp** to browse concepts, relationships, hierarchies, and AU extension content.  
  Guide: /tools/shrimp.md

**Query SNOMED CT via NCTS**
- Try **Postman** with FHIR endpoints and ECL queries.  
  Quickstart: /quickstarts/postman-ecl.md

**Understand FHIR structures**
- Learn **CodeSystem**, **ValueSet** (preferred camel case), **ConceptMap**, and bindings.  
  Tutorial: [/fhir/erminology-basics.md

---

## 5) Hosting & Integration

**Host your own copy of SNOMED CT**
- **Syndication** to pull releases; **Docker** to run a local **Ontoserver**.
- Version pinning, indexing, and update strategy.

Guide: /hosting/ontoserver-docker.md

---

## 6) Practical Topics & FAQs

- **SNOMED CT vs ICD** (terminology vs classification; analytics vs reporting).
- **ValueSet vs Reference Set** (selection for use vs packaged content/metadata).
- **ECL vs FHIR search** (expressive constraints vs standardized API ops).
- **Release cadence** (International → AU extension; how updates flow to NCTS).
- **Licensing & access** (who can use AU content; endpoint access considerations).

FAQs: /guides/faqs.md  
Glossary: /guides/glossary.md

---

## 7) References
Each of the more detailed pages in this structure contain direct links to websites with dedicated information on the topic. The links below will take you to the general homepages of these sites if you'd prefer to start there. 

- SNOMED CT basics and benefits: SNOMED Docs, [Benefits overview](https://docs.snomed.org/snomed-ct-practical-guides/snomed-ct-starter-guide/2-snomed-ct-benefits)  
- SNOMED International value proposition: [snomed.org/value-proposition](https://www.snomed.org/value-proposition)

<details>
  <summary>WIP TEST</summary>
  This is some collapsed text?
</details>
<details>
  <summary>REALLY?</summary>
  .
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
