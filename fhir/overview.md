[Go up a level](/snomed/overview.md) | [Go to the table of contents](/README.md)

# FHIR Terminology Basics

**FHIR** (Fast Healthcare Interoperability standard for exchanging healthcare data. Its terminology layer ensures that clinical concepts are represented consistently across systems.

Key resources:
- **CodeSystem**: Defines a set of codes (e.g., SNOMED CT concepts). The formulary, library or catalogue of codes you may already use is considered a CodeSystem as well (it's not tied to only SNOMED CT)
- **ValueSet**: Selects codes for a specific purpose (e.g., problem list). ValueSets are product of the FHIR Standard, hosted on FHIR Terminology Servers. A great feature of ValueSets is they readily contain mixtures of CodeSystems in them (e.g., combining local codes that don't exist in SNOMED CT-AU with a general set of SNOMED CT content). 
- **ConceptMap**: Maps codes between systems.

Common operations:
- `$expand`: Generate all codes in a ValueSet.
- `$validate-code`: Check if a code is valid in a ValueSet.
- `$lookup`: Retrieve details about a code.

FHIR terminology services often use SNOMED CT as the primary CodeSystem, enabling semantic interoperability and accurate data exchange.
