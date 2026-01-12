[Go up a level](/fhir/overview.md) | <a href="/README.md">Go Home</a>

# Ontoserver

In Australia, the NCTS uses **Ontoserver**, a FHIR-compliant terminology service developed by CSIRO.

Ontoserver is a high-performance FHIR terminology server, designed for runtime and analysis-time use of clinical and other terminologies using the FHIR Terminology resources and API which can be used to help with requirements such as user search and entry of coded data, analytics of coded data, or mapping.

Ontoserver supports integration with clinical systems, decision support tools, and analytics platforms, ensuring consistent terminology use across healthcare applications.

Key capabilities:
- **Functions**: `$expand`, `$validate-code`, `$lookup` for CodeSystems and ValueSets.
- **ECL (Expression Constraint Language)**: Advanced queries for SNOMED CT hierarchies and attributes.
- **Versioning**: Access specific releases of SNOMED CT-AU and AMT.
- **Syndication**: Keep local servers up to date with official releases.
  
# Local Hosting & Integration

You can host your own copy of SNOMED CT and other terminologies using **Ontoserver**. 

**Why host locally?**
- Faster access for internal systems.
- Control over versioning and update cycles.
- Ability to integrate directly with local applications and workflows.

The technical documentation is available online at <a href="https://ontoserver.csiro.au/docs" target="_blank" rel="noopener noreferrer">https://ontoserver.csiro.au/docs</a>, as well as a publicly accessible test server available for testing at https://r4.ontoserver.csiro.au/fhir (which is a backend service that can be used with the sample requests in our technical documentation, or through our free terminology browser at https://ontoserver.csiro.au/shrimp). The Ontoserver product is distributed as a Docker image, which can be stood up on any machine that supports Docker, including the major cloud providers.

Ontoserver is licensed on a per instance/endpoint, per region/country, annual basis, with the base price of free **in Australia** for **use in healthcare.** 
For non-Australia-based use or the use for non-healthcare reasons in Australia, pricing for an instance commences at USD$27,500 per year. The exact pricing depends on the configuration you would require to suit your needs.

The best way to explore Ontoserver is to start with the public end point (details above) though 60 day technical evaluation agreements are available so that you can then deploy your own instance on a trial basis.

**Steps to get started:**
For Australia-based, Healthcare-related use the Australian Digital Health Agency facilitates licences. Contact `help@digitalhealth.gov.au` to request a licence.
For all other use cases, contact `ontoserver-support@csiro.au` to request a licence.
