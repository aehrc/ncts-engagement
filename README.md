<h3>NCTS Engagement and Education</h3>

This site is a practical introduction to the **National Clinical Terminology Service (NCTS)** in Australia, focusing on the foundations first. Overviews and introductions to Clinical Terminology, its purpose and use cases, and the related software to store, extend and send terminology is covered here. Efforts have been made to include QuickStarts, Examples and References to validated information sources for newcomers. The content is broken down into small snippets so visitors can quickly find what they need.

---

<details>
  <summary>
    <h4>Navigating this site</h4>
  </summary>
  This is a lightweight "website" that's easy to update and share. If you open the <a href="https://github.com/aehrc/ncts-engagement/blob/main/README.md">README.md file</a> directly then you will see:<br>
  * A left-hand navigation menu that is a folder/file explorer<br>
  * A right-hand contents menu that shows the headings in the file that is open<br><br>
  <br>
  You can also use browser finding (e.g., CTRL-F, CMD-F) to keyword search the file that is open.<br>
  <br>
</details>

<details>
<summary><h4>Support</h4></summary>

This microsite is run by **James Grant** — `james.grant@csiro.au`.  
If you have additional queries or questions, send me an email!
<br>
More broadly, the NCTS is supported by the **Australian Digital Health Agency (ADHA)** with input from **CSIRO**.<br>
To make a general query please contact: `help@digitalhealth.gov.au`.<br>
<br>
</details>

<details>
<summary>
  <h4>
    What is Clinical Terminology?
  </h4>
</summary>

Clinical Terminology is essentially a dictionary of terms with agreed-upon meanings that enable consistent communication in healthcare.<br><br>
To illustrate, think of an English dictionary: it contains words and definitions that allow authors to write countless books. Each book is unique, and the words appear in different orders, yet readers can understand them—or look them up—because they share the same dictionary. Readers can even reuse words from one book to write another chapter or compare texts.<br><br>
Similarly, a Clinical Terminology provides a shared set of words and terms for the health system to document patient records. This common vocabulary makes it easier to share, search, and compare records within and across systems.<br><br>
Every clinical or health information system relies on terminology—it’s impossible to record anything without words. The goal is to adopt a single, standardized source of terminology to improve mutual understanding across the health system.<br><br>
In Australia, the primary general-purpose Clinical Terminology is SNOMED CT (Systematized Nomenclature of Medicine – Clinical Terms). Much of the material provided by the National Clinical Terminology Service (NCTS) focuses on the Australian edition, SNOMED CT-AU, though it’s not the only terminology in use.<br><br>
</details>

<details>
  <summary>
    <h4>
      What is a Terminology Server?
    </h4>
  </summary>

  A Terminology Server is a specialised software service that manages, publishes, and supports the use of clinical terminologies. It acts as a central, authoritative source for clinical concepts such as diagnoses, procedures, medications, laboratory tests, and observations. This helps ensure that these concepts or terms are represented consistently across systems and health settings.<br>
  <br>
  In practice, a terminology server stores standardised vocabularies (for example, SNOMED CT-AU, ICD, LOINC, or medication terminologies), along with their definitions, relationships, and versions. It provides operations or functions that allow clinical systems to look up codes, retrieve human-readable descriptions and translate between different coding systems where required.<br>
  <br>
The primary value of a terminology server is **consistency** and **interoperability**. By using a shared service rather than bespoke code lists, healthcare organisations reduce ambiguity, support accurate data exchange, and enable safer clinical decision-making. Terminology servers also simplify maintenance by managing updates and changes centrally, helping digital health systems remain aligned with evolving clinical standards while supporting analytics, reporting, and secondary uses of data.<br>
</details>

<details>
<summary><h4>
  Benefits & Use Cases</h4>
</summary>

To recap the above benefits for clinical terminology and terminology servers: <br>
- Consistency: the "dictionary" of terms being available across the continuum of systems within and alongside health organisations and solutions
- Interoperability: more organisations and solutions are using nationally or internationally recognised terminology vocabularies allowing concepts sent out to be understood by other systems and incoming concepts to be understood by the local system
- (there's a related messaging/exchange standard to this known as "FHIR" though that's for later on) 
<br>
These seemingly smaller and simpler outcomes of using standardised clinical terminology and server systems multiplies to more specific outcomes: <br>
- Less Maintenance: particularly across large or multiple solutions the "clinical jargon" is one spot and updates synchronise through
- Larger Markets: the entire globe is moving towards standardised terminologies and separating clinical terminology into a terminology server separate to a core system(s) means changing the terminology source can be enough to try a solution in a new region 
- Easier Tinkering: developed on well-established web standards with a mature community there's lots of references to learn from, people to talk with, and exploration can all occur from within a single web browser (more below!)
<br>
There are also next-generation solutions beyond initial implementation and embedding: clinical decision support systems fed by local and non-local information, complex analytics using the ontological and meta-data of a full clinical terminology and allowing higher quality artificial intelligence (AI) methods through access to standardised (cleaner) training and run-time data 

</details>

<details>
<summary><h4>
  Getting Started</h4>
</summary>

  <details>
    <summary><h5>
      Look at the medication concept 'prednisolone'
    </h5></summary>
    Some test content. Visuals. 
  </details>

<!-- 
**Explore SNOMED CT**
- Use **Shrimp** to browse concepts, relationships, hierarchies, and AU extension content.  
  Guide: /tools/shrimp.md

**Query SNOMED CT via NCTS**
- Try **Postman** with FHIR endpoints and ECL queries.  
  Quickstart: /quickstarts/postman-ecl.md

**Understand FHIR structures**
- Learn **CodeSystem**, **ValueSet**, **ConceptMap**, and bindings.  
  Tutorial: /fhir/terminology-basics.md
--> 

</details>


<details>
  
<summary><h4>
  Popular Questions and Answers (FAQ subset)</h4>
</summary>
  These Q&As are the ones seen the most often. Of course, there's plenty more curiosity and a full list of queries and inquisitiveness raised is available on the (full) Frequently Asked Questions page.<br>
  
  <details>
    <summary><h5>
      Clinical terminology versus clinical classification - what's the difference?
    </h5></summary>
    Answer to go here.
  </details>
  <details>
    <summary><h5>
     How do I access the NCTS' clinical terminology information?
    </h5></summary>
    Answer to go here.
  </details>
  <details>
    <summary><h5>
      Where can I learn more?
    </h5></summary>
    Answer to go here.
  </details>
  
</details>
<!-- 
- **SNOMED CT vs ICD** (terminology vs classification; analytics vs reporting).
- **ValueSet vs Reference Set** (selection for use vs packaged content/metadata).
- **ECL vs FHIR search** (expressive constraints vs standardized API ops).
- **Release cadence** (International → AU extension; how updates flow to NCTS).
- **Licensing & access** (who can use AU content; endpoint access considerations).
<!-- 
FAQs: [/guides/faqs.md](/guides/faqs.md)  
Glossary: /guides/glossary.md
--> 



<!-- 
Working Graveyard (to delete)
* SEARCH through SP/Slack/Teams for other mentions of Benefits / Use Cases / Case Studies / User Stories.
* Plus general web / articles.
* List of who's known to be using SCT-AU already: https://www.healthterminologies.gov.au/understanding-clinical-terminology-landing/whos-using-snomed-ct-au/ 
* Implementation guide (high-level): https://www.healthterminologies.gov.au/implementing-in-software/getting-started/implementation-whats-involved/ 
* Resources/materials: https://www.healthterminologies.gov.au/document-library/ 
* Other code set relationships (not as relevant here): https://www.healthterminologies.gov.au/understanding-clinical-terminology-landing/the-big-picture-snomed-and-other-code-sets/ 

-->
