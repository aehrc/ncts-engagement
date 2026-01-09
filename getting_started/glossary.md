
[Go up a level](/README.md) | [Go to the table of contents](/README.md)

# Glossary of Key Terms

<details>
<summary>SNOMED CT</summary>

A comprehensive, multilingual clinical terminology used worldwide. It contains concepts, descriptions, and relationships that enable precise recording of clinical information. SNOMED CT supports interoperability, analytics, and decision support.

</details>



<details>
<summary>SNOMED CT-AU</summary>

The Australian edition of SNOMED CT. It includes the International release plus Australian-specific content such as local clinical terms and medicines. Maintained by the Australian Digital Health Agency.

</>
<summary>AMT (Australian Medicines Terminology)</summary>

A terminology for medicines used in Australia. It standardizes medicine names for prescribing and dispensing, ensuring consistency across systems.

</details>



<details>
<summary>Concept</summary>

A unique identifier in SNOMED CT representing a clinical idea (e.g., “Diabetes mellitus”). Each concept has descriptions (terms) and relationships to other concepts.

</details>



<details>
<summary>Description</summary>

The human-readable term associated with a concept (e.g., “Diabetes mellitus” or “Type 2 diabetes”). Multiple descriptions can exist for one concept.

</details>



<details>
<summary>Relationship</summary>

Defines how concepts are connected (e.g., “Is a” hierarchy or attribute relationships like “Finding site = Heart structure”).

</details>



<details>
<summary>ValueSet</summary>

A FHIR resource that specifies a set of codes for a particular use case (e.g., all SNOMED CT codes for “Allergy”). Generated dynamically or curated manually.

</details>



<details>
<summary>Reference Set (Refset)</summary>

A curated subset of SNOMED CT concepts packaged for distribution. Often includes metadata like language preferences or mapping tables.

</details>



<details>
<summary>CodeSystem</summary>

A FHIR resource that defines a terminology system (e.g., SNOMED CT or AMT). It includes metadata about the system and its codes.

</details>



<details>
<summary>ConceptMap</summary>

A FHIR resource that maps codes from one system to another (e.g., SNOMED CT to ICD-10). Useful for interoperability andA FHIR resource that maps codes from one system to another (e.g., SNOMED CT to ICD-10). Useful for interoperability and reporting.

</details>



<details>
<summary>ECL (Expression Constraint Language)</summary>

A query language for SNOMED CT. It retrieves concepts based on hierarchy and attributes. Example: `<< 404684003` returns all descendants of “Clinical finding.”

</details>



<details>
<summary>Ontoserver</summary>

A FHIR-compliant terminology server developed by CSIRO. Provides fast access to SNOMED CT and AMT, supports FHIR terminology operations, and enables advanced queries using ECL.

