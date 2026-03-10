
Content stubs and thoughts to process

- **SNOMED CT vs ICD** (terminology vs classification; analytics vs reporting). Mentioned in README, needs detail.
- **ValueSet vs Reference Set** (selection for use vs packaged content/metadata).
- **ECL vs FHIR search** (expressive constraints vs standardized API ops).

-- CSIRO ECL Explanation by Senior Terminologist (https://mjosborne1.github.io/trove/)
-- SNOMED INT ECL scripts on git (https://github.com/IHTSDO/snomed-expression-constraint-language/tree/main/examples)
-- ECL Render (https://ecl-tester.onrender.com/)
-- ECL Builder (https://ecl-builder.vercel.app/) [think Shrimp>ECL works just as well and saves a bookmark]
-- Additional content dumps to be broken down into components 

Identifier Dominant and formatted version
(
  (
    (^933483571000036108 .<< 363704007)
    OR
    <! (^933483571000036108 .<< 363704007)
    OR
    (<! ((^933483571000036108 .<< 363704007) OR <! (^933483571000036108 .<< 363704007))
      : 272741003 = (<< 7771000 OR 24028007))
  )
  MINUS
  (
    (* {{ term = "entire" }})
    OR (* {{ term = "part" }})
    OR (* {{ term = "skin structure" }})
  )
)
OR
(
  (
    < 245849007
    OR << 38033009
    OR << 414403008
    OR << 118622000
    OR << 1360029003
    OR 13924000
  )
  MINUS < 41796003
)


Verbose version 
(( (( ( (<! ( (^ 933483571000036108 | Royal Australian and New Zealand College of Radiologists radiology procedure requesting reference set (foundation metadata concept) | .<<363704007 | Procedure site (attribute) | ) ) OR ( (^ 933483571000036108 | Royal Australian and New Zealand College of Radiologists radiology procedure requesting reference set (foundation metadata concept) | .<<363704007 | Procedure site (attribute) | ) )) ) MINUS ( (((* {{ term = "entire" }})) OR ((* {{ term = "part" }})) OR ((* {{ term = "skin structure" }}))) ) ) OR ( ( <! ( ( (<! ( (^ 933483571000036108 | Royal Australian and New Zealand College of Radiologists radiology procedure requesting reference set (foundation metadata concept) | .<<363704007 | Procedure site (attribute) | ) ) OR ( (^ 933483571000036108 | Royal Australian and New Zealand College of Radiologists radiology procedure requesting reference set (foundation metadata concept) | .<<363704007 | Procedure site (attribute) | ) )) ) MINUS ( (((* {{ term = "entire" }})) OR ((* {{ term = "part" }})) OR ((* {{ term = "skin structure" }}))) ) ) : (272741003 | Laterality (attribute) | = << 7771000 | Left (qualifier value) | OR 272741003 | Laterality (attribute) | = 24028007 | Right (qualifier value) | ) ) MINUS ( (((* {{ term = "entire" }})) OR ((* {{ term = "part" }})) OR ((* {{ term = "skin structure" }}))) ) )) ) OR ( ( (< 245849007 | Post-surgical anatomy (morphologic abnormality) | OR << 38033009 | Amputation stump (body structure) | OR << 414403008 | Herniated structure (morphologic abnormality) | OR << 118622000 | Fistula (morphologic abnormality) | OR << 1360029003 | Sinus tract (morphologic abnormality) | OR 13924000 | Wound (morphologic abnormality) | ) ) MINUS ( < 41796003 | Anastomosis (morphologic abnormality) | ) ))



- **Release cadence** (International → AU extension; how updates flow to NCTS).
- Benefits / Use Cases / Case Studies / User Stories
- Implementation guide (high-level): https://www.healthterminologies.gov.au/implementing-in-software/getting-started/implementation-whats-involved/ 
- Resources/materials: https://www.healthterminologies.gov.au/document-library/ 

