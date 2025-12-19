
[Go up a level](/README.md) | [Go to the table of contents](/README.md)

# Getting Started

There's a good smattering of jargon in this space and seeing is believing. Let's explore clinical terminology (SNOMED CT-AU) in a visual sense to see what's in there and how it interconnects and run some queries on the NCTS' server to understand the API use in this space.

**1. Browse SNOMED CT**
- Use **Shrimp**, a web-based browser, to explore SNOMED CT concepts, hierarchies, and AU extension content.
- Shrimp Guide

**2. API queries** 
You can actually copy the queries provided straight into a browser tab and they'll work; looks a bit better on platforms like Postman or even using a Web Connector in Power BI.
- Try **ECL (Expression Constraint Language)** for advanced queries like “all descendants of a concept.”
- Postman Quickstart

**3. Understand FHIR Terminology**
- Learn how **CodeSystem**, **ValueSet**, and **ConceptMap** resources work.
- Practice `$expand`, `$validate-code`, and `$lookup` operations against Ontoserver.
- FHIR Basics

These steps help you move from browsing to making API calls and understanding terminology bindings in FHIR. Once comfortable, explore hosting your own Ontoserver for local integration.
