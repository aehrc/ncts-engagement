
[Go up a level](/fhir/overview.md) | [Go to the table of contents](/README.md)

# Ontoserver

In Australia, the NCTS uses **Ontoserver**, a FHIR-compliant terminology service developed by CSIRO.

Ontoserver supports integration with clinical systems, decision support tools, and analytics platforms, ensuring consistent terminology use across healthcare applications.

Key capabilities:
- **Functions**: `$expand`, `$validate-code`, `$lookup` for CodeSystems and ValueSets.
- **ECL (Expression Constraint Language)**: Advanced queries for SNOMED CT hierarchies and attributes.
- **Versioning**: Access specific releases of SNOMED CT-AU and AMT.
-- **Syndication**: Keep local servers up to date with official releases.
  
# Local Hosting & Integration

You can host your own copy of SNOMED CT and other terminologies using **Ontoserver**. 

**Why host locally?**
- Faster access for internal systems.
- Control over versioning and update cycles.
- Ability to integrate directly with local applications and workflows.

**Steps to get started:**
(to update)
1. **Syndication**: Subscribe to NCTS syndication feeds to download SNOMED CT-AU and AMT releases.
2. **Docker deployment**: Use the official Ontoserver Docker image for quick setup.
3. **Configuration**: Set up API endpoints, authentication, and indexing for performance.
4. **Updates**: Apply new releases regularly to stay aligned with NCTS and SNOMED CT International.
