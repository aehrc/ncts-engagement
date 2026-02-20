<h3>Finding Terms, Codes, Maps and more Information</h3>

As mentioned on the <a href='https://github.com/aehrc/ncts-engagement/blob/main/README.md'>top-level page</a> the initial foray into clinical terminology, such as SNOMED CT, is most readily done with the visualiser tool, <a href='https://ontoserver.csiro.au/shrimp/'>Shrimp</a>.

It does an excellent job of showing upstream terms from your search (e.g., Panadol 500mg, 100 tablets, blister pack <i>leads up to</i> Panadol 500mg, 100 tablets [any packaging] <i>leads up to</i> Paracetamol 500mg, 100 tablets [any brand, any packaging]). Clicking any of those 2 <i>higher</i> terms will show you their direct descendents (so I can see in 2-clicks that there are 52 different brand-and-packaging style combinations of paracetamol 500mg tablets in the Australian Medicines Terminology). 

Whilst useful and very quick for anyone to use there's a lot of detail either not displayed in the visualisation or not displayed all at once - there's simply a wealth of information about clinical terms and concepts and only so much can fit in one window.

Hence extracting the information into 'tables' is the method towards making full use of the information richness. 

To help gain that benefit as quickly and easily as possible there is a compilation of useful query patterns that can be used in browser - no fancy software^ - to start retrieving this data. <br>
^some 'fancy' software does become useful though for the beginner Excel (usually needing a licence) or Power BI (actually free for desktop use) will be enough to see value 

<details>
<summary><h4>Retrieving all the characteristics associated with a term (concept)</h4>
</summary>
So far the focus has been on finding a particular term in the SNOMED CT-AU clinical terminology. The codesystem contains a lot more information about each concept though and here's a pattern to retrieve that.<br><br>
https://tx.ontoserver.csiro.au/fhir/CodeSystem/$lookup?system=http://snomed.info/sct&code=20413011000036107&property=normalForm
<br>
A brief summary of the parts of the above query:
<br>* The terminology server address (where on the internet, or your network, the machine providing this service is located) - https://tx.ontoserver.csiro.au/
<br>* The type of data structure in use (which is typically 'fhir' though could be others; and can be omitted from the query depending on how the server is setup) - fhir/
<br>* The area of the terminology being looked within (more on this later; right now we're learning about pure concept information so look in the CodeSystem) - CodeSystem/
<br>* The operation (or function) being used (each area has a slightly different set, and these operations also tie back to the data structure [fhir] in use) - $lookup
<br>* The inputs into the operation (again, these vary per operation and there's documentation on each which will be linked here soon)
<br>  * ?system=http://snomed.info/sct (which [code]system is being looked up - in this case it's SNOMED's Clinical Terms [sct] though the server can hold any terminology it needs; and they can be queried in this way)
<br>  * &code=20413011000036107 (the specific code for the term that's having the operation run on it [$lookup, in this case]) -- within this pattern if you swap this code around to whatever you can find in Shrimp or your local systems - chances are it will return some helpful information!
<br>  * &property=normalForm (this is a 'switch' meaning the operation returns everything it can find about that term as a text string [nice and human readable; there are other ways to make it more machine-friendly])
<br><br>
<details>
<summary><h5>Example response</h5></summary>
The above query returns a JSON object, the key part of which is the long string of text describing the characteristics of this concept (Keppra 250mg tablets).<br><br>
=== 13620011000036108|Keppra (levetiracetam 250 mg) tablet, 60 tablets|:{774158006|Has product name|=3677011000036106|Keppra|},{1142142004|Has pack size|=#60.0,999000131000168101|Count of contained component ingredient|=#1,774163005|Has pack size unit|=732935002|Unit of presentation|,774160008|Contains clinical drug|=(23172011000036106|Levetiracetam 250 mg tablet|:411116001|Has manufactured dose form|=(385268001|Oral dose form|:{736475003|Has dose form release characteristic|=736849007|Conventional release|},{736476002|Has basic dose form|=(385055001|Tablet|:{736518005|Has state of matter|=736678006|Solid|})},{736474004|Has dose form intended site|=738956005|Oral|},{736473005|Has dose form transformation|=761954006|No transformation|},{736472000|Has dose form administration method|=738995006|Swallow|}){774158006|Has product name|=3677011000036106|Keppra|},{732943007|Has basis of strength substance|=387000003|Levetiracetam|,127489000|Has active ingredient|=387000003|Levetiracetam|,999000041000168106|Has total quantity value|=#250.0,999000051000168108|Has total quantity unit|=258684004|milligram|},{999000001000168109|Has other identifying information|=\"None\"},{1142140007|Count of active ingredient|=#1})},{30465011000036106|Has container type|=287011000036106|Blister pack|},{1142143009|Count of clinical drug type|=#1}
<br><br>
This is a little hard on the eye (and some machine processing will be needed to split it all up). For learning purposes see the below line-separated breakdown of the details the NCTS' OntoServer had on this medicine: <br>
<br>13620011000036108|Keppra (levetiracetam 250 mg) tablet, 60 tablets
<br>Has product name|=3677011000036106|Keppra
<br>Has pack size|=#60.0
<br>Count of contained component ingredient|=#1
<br>Has pack size unit|=732935002
<br>Unit of presentation|,774160008
<br>Contains clinical drug|=(23172011000036106|Levetiracetam 250 mg tablet
<br>Has manufactured dose form|=(385268001|Oral dose form
<br>Has dose form release characteristic|=736849007|Conventional release
<br>Has basic dose form|=(385055001|Tablet
<br>Has state of matter|=736678006|Solid
<br>Has dose form intended site|=738956005|Oral
<br>Has dose form transformation|=761954006|No transformation
<br>Has dose form administration method|=738995006|Swallow
<br>Has product name|=3677011000036106|Keppra
<br>Has basis of strength substance|=387000003|Levetiracetam
<br>Has active ingredient|=387000003|Levetiracetam
<br>Has total quantity value|=#250.0,
<br>Has total quantity unit|=258684004|milligram
<br>Has other identifying information|=\"None\"
<br>Count of active ingredient|=#1
<br>Has container type|=287011000036106|Blister pack
<br>Count of clinical drug type|=#1
<br><br>
A key facet to SNOMED CT as a terminology is that there is always a human-readable and computer readable pairing on any given component. This is why the above "looks a bit weird" as the response provided includes both. Fortunately, they can be separated through basic processes to keep it 'cleaner' for each audience.<br><br>
The computer coded identifiers serve a secondary purpose here too: they can be fed back into queries on the server to identify products with - or without - that particular characteristic. As an example yet to be written, the code for "Swallow" can be used to find every AMT product that is typically Swallowed. 
<details>
</details>