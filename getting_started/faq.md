
[Go up a level](/README.md) | [Go to the table of contents](/README.md)

# Frequently Asked Questions (FAQs)

<details>
<summary>What is the difference between SNOMED CT and ICD?</summary>

**SNOMED CT** is a clinical terminology designed for detailed recording of patient data and interoperability across systems. It supports analytics, decision support, and semantic precision.

**ICD** (International Classification of Diseases) is a classification system primarily used for statistical reporting and billing. ICD groups conditions into categories for epidemiology and reimbursement, whereas SNOMED CT provides granular clinical detail.

Both can coexist: SNOMED CT for clinical documentation, ICD for reporting.

</details>

---

<details>
<summary>What is a ValueSet vs a Reference Set?</summary>

A **ValueSet** is a FHIR resource that defines which codes can be used in a specific context (e.g., a problem list or medication list). It is dynamic and often generated from queries.

A **Reference Set** (refset) is a curated subset of SNOMED CT concepts, packaged for distribution. Refsets can include metadata like language preferences or mapping tables.

Think of ValueSets as “rules for selection” and Reference Sets as “predefined collections.”

</details>

---

<details>
<summary>What is ECL?</summary>

**Expression Constraint Language (ECL)** is a query language for SNOMED CT. It allows you to retrieve concepts based on hierarchy and attributes.

Examples:
- `<< 404684003` → All descendants of “Clinical finding.”
- `< 71388002 |Procedure|` → All children of “Procedure.”

ECL is powerful for building ValueSets and performing advanced terminology searches.

</details>

---

<details>
<summary>How often is SNOMED CT updated?</summary>

**International Edition**: Released twice yearly by SNOMED International.  
**Australian Edition (SNOMED CT-AU)**: Includes the International release plus Australian-specific content. Updates follow shortly after each international release.

Regular updates ensure new concepts, corrections, and enhancements are available for clinical use.

</details>

---

<details>
<summary>Do I need a license to use SNOMED CT?</summary>

Yes. SNOMED CT is distributed under license. In Australia:
- Access to SNOMED CT-AU and NCTS services requires registration through the **Australian Digital Health Agency (ADHA)**.
- Most healthcare organizations are covered under national agreements, but individual developers may need to apply.

Check NCTS Portal for details.

</details>

---

<details>
<summary>What is Ontoserver and why use it?</summary>

**Ontoserver** is a FHIR-compliant terminology server developed by CSIRO. It provides:
- Fast access to SNOMED CT and AMT.
- Support for FHIR terminology operations (`$expand`, `$validate-code`, `$lookup`).
- Advanced querying with ECL.
- Syndication for local hosting and updates.

It’s the backbone of NCTS and widely used for interoperability in Australia.

</details>

---

<details>
<summary>How does SNOMED CT integrate with FHIR?</summary>

SNOMED CT concepts are represented as **codes** in FHIR resources.  
Key FHIR resources:
- **CodeSystem**: Defines SNOMED CT as a system.
- **ValueSet**: Selects subsets of SNOMED CT for specific contexts.
-- **ConceptMap**: Maps SNOMED CT codes to other terminologies (e.g., ICD).

Terminology servers like Ontoserver enable operations like `$expand` and `$validate-code` to ensure correct bindings.

