<h3>NCTS Engagement and Education</h3>

This site is a practical introduction to the **National Clinical Terminology Service (NCTS)** in Australia, focusing on the foundations first. Overviews and introductions to Clinical Terminology, its purpose and use cases, and the related software to store, extend and send terminology is covered here. Efforts have been made to include QuickStarts, Examples and References to validated information sources for newcomers. The content is broken down into small snippets so visitors can quickly find what they need.

---

<details>
  <summary>
    <h4>Navigating this site</h4>
  </summary>
  This is a lightweight "website" that's easy to update and share. If you open the <a href="https://github.com/aehrc/ncts-engagement/blob/main/README.md">README.md file</a> directly then you will see:<br>
  * A left-hand navigation menu that is a folder/file explorer<br>
  * A right-hand contents menu that shows the headings in the file that is open (needs a click to expand)<br>
  <br>
  You can also use browser finding (e.g., CTRL-F, CMD-F) to keyword search the file that is open. *Note this only searches the current page, not the entire site.*<br>
  <br>
</details>

<details>
<summary><h4>Support</h4></summary>

This microsite is run by **James Grant** ( `james.grant@csiro.au` ) to support the accessibility and approachability of the NCTS and its services and offerings. If you have queries or questions not answered here please send me an email!<br>
<br>
Formal contact with the NCTS via the **Australian Digital Health Agency** is available through `help@digitalhealth.gov.au` and the NCTS team will respond to you shortly.<br>
<br>
</details>

<details>
<summary>
  <h4>
    What is Clinical Terminology?
  </h4>
</summary>

Clinical Terminology is essentially a dictionary of terms with mutually understood meanings that enable consistent communication in healthcare.<br><br>
To illustrate, think of an English dictionary: it contains words and definitions that allow authors to write countless books. Each book is unique, and the words appear in different orders, yet readers can understand them — or look them up — because they share the same dictionary. Readers can even reuse words from one book to write another chapter or compare texts.<br><br>
Similarly, a Clinical Terminology provides a shared set of words and terms for the health system to document patient records. This common vocabulary makes it easier to share, search, and compare records within and across systems.<br><br>
Every clinical or health information system relies on terminology — it is impossible to record anything without words. The goal is to adopt a single, standardized source of terminology to improve mutual understanding across the health system.<br><br>
In Australia, the primary general-purpose Clinical Terminology is SNOMED CT (Systematized Nomenclature of Medicine – Clinical Terms). Much of the material provided by the National Clinical Terminology Service (NCTS) focuses on the Australian edition, SNOMED CT-AU, though it is not the only terminology in use.<br><br>
</details>

<details>
  <summary>
    <h4>
      What is a Terminology Server?
    </h4>
  </summary>

  A Terminology Server is a specialised software service that manages, publishes, and supports the use of clinical terminologies. It acts as a central, authoritative service for clinical concepts representing diagnoses, procedures, medications, laboratory tests, observations and more. This helps ensure that these concepts or terms are represented consistently across systems and health settings.<br>
  <br>
  In practice, a terminology server stores standardised vocabularies (for example, SNOMED CT-AU, LOINC, or medication terminologies), along with their definitions, relationships, and versions. It provides operations or functions that allow clinical systems to look up codes, retrieve human-readable descriptions and translate between different coding systems where required.<br>
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

The purpose of the following QuickStarts is to showcase the first steps in interacting with SNOMED CT-AU and demystify it. It's a comprehensive system with plenty of context considerations and that can be challenging.<br>
<br>
So, let's dive in and see what it's all about (because a little does go a long way!).

  <details>
    <summary><h5>
      Visualising SNOMED CT-AU (using the medication example of labetalol)
    </h5></summary>
    Clinical terminology is about detail and richness. The CSIRO has developed a visualiser for terminology so users can "see" what that means (which is essentially a concept of interest connected to all the elements to which it is related).<br>
    <br>
    This image is a snapshot of the term 'labetalol', a heart medication, and where it sits within the structure of SNOMED CT-AU:<br>
    <img src="https://s3.amazonaws.com/cloud.kumu.io/accounts/204453/1134260/7999b714-7179-4ee7-a22d-f87bca36e645.png" />
    <br>
    <a href="https://ontoserver.csiro.au/shrimp/?concept=46547007&version=http%3A%2F%2Fsnomed.info%2Fsct%2F32506021000036107%2Fversion%2F20251231&valueset=http%3A%2F%2Fsnomed.info%2Fsct%2F32506021000036107%3Ffhir_vs&fhir=https%3A%2F%2Ftx.ontoserver.csiro.au%2Ffhir">Open this for yourself (you will need to agree to usage terms and conditions if you're a first time user of the Shrimp Browswer</a>.
    <br>
    <br>
    The elements on the (1) side are 'higher' up the structure. Labetalol is considered an adrenergic receptor antagonist, a beta blocker and is derived from Ethanolamine. Clicking any of those elements (which are concepts too) will show you what is related to them in turn. The elements on the (2) side are 'lower' down the structure. As a concept, labetalol comes in a combined product with hydrochlorothiazide, comes as itself only, comes in an oral dose form and comes in a parenteral (injectable) form. Clicking any of those elements will show you what's related to those (which become increasingly specific concepts eventually ending in what physically exists).<br>
  </details>
  <details>
    <summary><h5>
      Visualising SNOMED CT-AU (search for your own)
    </h5></summary>
    The link above goes directly to the labetalol concept in Shrimp. To find a different medication use the search field and type whatever you like!<br><br>
    <img src="https://s3.amazonaws.com/cloud.kumu.io/accounts/204453/1134260/01bae7ab-acd8-4b9e-b739-67dfb173dcc0.png" />
    <br><br>
    99% of the time all you need to do to see if something exists in SNOMED CT-AU or find out how it connects in the system (and therefore what it is related to) is type if into the search field (1) as soon as <a href="https://ontoserver.csiro.au/shrimp/">Shrimp</a> opens.<br>
    <br>
    The other 1% might mean changing the CodeSystem (2) to something else. For example, LOINC - a pathology and labratory reference - is another popular catalogue to search.<br>
    <br>
  </details>
  <details>
    <summary><h5>
      Visualising SNOMED CT-AU (a finding or symptom of "chest pain")
    </h5></summary>
    SNOMED CT-AU contains over 700,000 clinical terms at the time this microsite has been written and there's plenty more than medications in there!<br>
    <br>
    Let's use this example to also illustrate how different concept types should be used in different parts of a clinical information system. Searching for "chest pain" displays the following:<br>
    <img src="https://s3.amazonaws.com/cloud.kumu.io/accounts/204453/1134260/0beaea50-470f-4b5f-8ade-e25cc9b6f541.png" /><br>
    <a href="https://ontoserver.csiro.au/shrimp/?concept=29857009&version=http%3A%2F%2Fsnomed.info%2Fsct%2F32506021000036107%2Fversion%2F20251231&valueset=http%3A%2F%2Fsnomed.info%2Fsct%2F32506021000036107%3Ffhir_vs&fhir=https%3A%2F%2Ftx.ontoserver.csiro.au%2Ffhir">Direct link to open the chest pain concept in Shrimp</a><br>
    <br>
    SNOMED CT-AU has many more detailed concepts for chest pain to enable healthcare professionals and health teams to record with specificity what is or has happened in a patient's history.<br>
    <br>
    A nuance here is that "chest pain" has a concept type of "Finding". It's distinct to a diagnosis that a doctor/medical professional may end up making after the patient presented with chest pain.
  </details>
  <details>
    <summary><h5>
      Visualising SNOMED CT-AU (a diagnosis or disorder of "myocardial infarction") [a heart attack]
    </h5></summary>
    Should the diagnosis that the health professional determine is a "heart attack" then a set of clinical terms to describe that exist:<br>
    <img src="https://s3.amazonaws.com/cloud.kumu.io/accounts/204453/1134260/e5bca1c3-24bf-4860-8abf-44cd9cd2255b.png" /><br>
    <a href="https://ontoserver.csiro.au/shrimp/?concept=22298006&version=http%3A%2F%2Fsnomed.info%2Fsct%2F32506021000036107%2Fversion%2F20251231&valueset=http%3A%2F%2Fsnomed.info%2Fsct%2F32506021000036107%3Ffhir_vs&fhir=https%3A%2F%2Ftx.ontoserver.csiro.au%2Ffhir">Direct link to myocardial infarction concept in Shrimp</a>.<br>
    <br>
    This example showcases two additional facets of the NCTS' Ontoserver hosted copy of SNOMED CT-AU.<br>
    - Most clinical terms have Synonyms that are recognised during searching or filtering. Typing in "heart attack" will find the same concept as "myocardial infarction".<br>
    <img src="https://s3.amazonaws.com/cloud.kumu.io/accounts/204453/1134260/b0585f41-e201-4867-935f-a7fc6ab71722.png" /><br>
    - Click around as much as you like and you will not find a direct line between "chest pain" (finding/symptom) and "myocardial infarction" (disorder/diagnosis). A clinical terminology is limited to describing all the "stuff" that goes into clinical care and surrounding environment. It does not contain health "knowledge" - such that chest pain could be indicative of a myocardial infarction. That knowledge is captured in training programs, dedicated knowledgebases and decision support systems. And it is deliberately kept separate.<br>
  </details>
  <details>
    <summary><h5>
      Beyond the visuals - the data itself
    </h5></summary>
    All the data that is used to generate the visuals in Shrimp is available as tables or structured responses from the NCTS service (or your own terminology server).<br>
    <br>
    The first foray you should have is downloading the tables of data from the <a href="https://www.healthterminologies.gov.au/">NCTS website</a>. If you don't have a username and password yet follow the prompts to Register - accounts for health-related use cases in Australia are free.<br>
    <br>
    Once logged in there's a lot of information there. Let's start with finding the myocardial infarction (heart attack) disorder in a Reference Set (refset) table. Navigating through the menus: [Access clinical terminology > SNOMED CT-AU > Search reference sets] will take you to a filterable search. <a href="https://www.healthterminologies.gov.au/access-clinical-terminology/access-snomed-ct-au/reference-sets/?ui:filter=disorder">Type in 'disorder'</a> and the top hit is "Clinical finding foundation reference set." Clicking the "LATEST" button opens the download view and you can choose what specific format you'd like to use. 
    <br>
    <br>
    If you're at the stage where you want to skip the graphical and deal in purer data then the NCTS' FHIR Terminology Server (Ontoserver) has an open endpoint to enable that. Using the reference set id seen above the following API call will retrieve the same file in a JSON format. This link will work in your browser (though it may render more nicely in a platform like Postman): https://tx.ontoserver.csiro.au/fhir/ValueSet/$expand?url=http://snomed.info/sct?fhir_vs=refset/32570071000036102 <br>
    Even if you're not technical I encourage you to copy and paste this URL into your browser - it just works! One of the benefits to building Australia's clinical terminology with the adjacent Standard, FHIR^, in mind - it adopts general web compliant queries and responses. <br>
    ^Fast Healthcare Interoperable Resource - a topic covered here (pending)<br>
    <br>
    Example of the browser-based return seen at time of writing:<br>
    <img src="https://s3.amazonaws.com/cloud.kumu.io/accounts/204453/1134260/cf7a1f6d-9cd7-4ace-a524-add02d309d60.png" /><br>
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
      Clinical terminology (or an ontology) versus clinical classification (or a taxonomy) - what's the difference?
    </h5></summary>
    Taxonomies classify; Ontologies specify.<br><br>
    A taxonomy is like a filing system - it puts things into categories so they’re easy to find. For example, the Dewey Decimal System groups books by topic, and biology groups animals into classes like mammals or reptiles. Ontologies go deeper: they define how those categories work, what relationships exist, and what rules apply. Think of an ontology as the blueprint for organizing information - it says what kinds of things exist and how they connect.<br>
    In healthcare: ICD is a taxonomy - it classifies diseases into codes. SNOMED CT is an ontology - it defines clinical concepts, their attributes, and relationships for richer, structured data.<br>
    Thus there is a push to use ontologies (clinical terminology) in clinical information systems so the most precise and information-rich concept is used. Taxonomies (classifications) almost always sacrifice richness or nuance for simplicity.<br>
    <a href="https://www.forbes.com/sites/cognitiveworld/2019/03/24/taxonomies-vs-ontologies/">Learn more</a> (external link).
  </details>
  <details>
    <summary><h5>
     Where can I learn more?
    </h5></summary>
    The NCTS website is the place to go and can be found here: https://www.healthterminologies.gov.au/ (external link).<br><br>
    It includes far more information than this microsite on topics such as each of the Terminologies supported by the NCTS, details on what the team does, and both video and written documentation about terminology and the related technologies.<br>
  </details>
  <details>
    <summary><h5>
      Where do I ask questions if I'm stuck? 
    </h5></summary>
    Contact us! We'd love to help. Email help@digitalhealth.gov.au and one of the team will reply to you shortly.<br>
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
