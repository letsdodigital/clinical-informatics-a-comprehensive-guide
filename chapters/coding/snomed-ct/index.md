# SNOMED CT

Questions:

1. Why is SNOMED important?
2. What is it? I hear about it a lot but why should I learn this?
3. How is it useful?
    - Streamline data entry
    - Semantic interoperability
    - Data processing - understanding /
     
4. What is it used for?
    - Diagnoses, procedures, problems, occupations, drugs, devices
5. Can I build something using SNOMED CT?
    - data analytics e.g. you're using Python or R and processing health and care data
    - writing applications e.g. I'm writing software to be used by other clinicians


-----

SNOMED CT is a very large and comprehensive terminology. 
Importantly terms can be linked by multiple relationships to other terms.
This makes it possible for software to determine that multiple sclerosis is a disease defined by demyelination of the central nervous system. 

SNOMED CT can be considered an ontology for health and care. 
An ontology is defined as a "set of concepts and categories in a subject area or domain that shows their properties and the relations between them".

When implemented properly, SNOMED CT enables software to make intelligent decisions about what to show, what data to request and what forms to present, based on the diagnoses entered. For example, the database would know that a patient had epilepsy if they were given a diagnosis of juvenile myoclonic epilepsy or frontal lobe epilepsy or any of the hundreds of other terms that are equivalent to a diagnosis of epilepsy. 

Thus a command to ‘send an alert when a patient, belonging to a particular consultant, with motor neurone disease loses 5% of their body mass compared to their baseline at dia- gnosis’, can be implemented easily. SNOMED CT allows the underlying logic to simply ask whether the patient has a type of motor neurone disease and this would automatically include all patients with related diagnoses such as primary lateral sclerosis and pseudobulbar palsy.

SNOMED CT is not confined to diagnostic and procedural information. There are hierarchies covering a wide range of medical terminology including anatom- ical structures, pathology, occupations and ethnic origins. With local extensions such as the NHS’ dm+d (dictionary of medicines and devices) these codes can be used in any field that needs structured coded information.

Another advantage is support for synonyms. A distinct clinical concept can and usually has multiple synonyms - for example Granulomatosis with poly- angiitis was previously known as Wegener granulomatosis. With synonym support, a user entering an outdated or synonymous term would find the synonym and see it mapped into the new modern preferred description of the term.

Within SNOMED CT, clinical terms are concepts, synonyms are descriptions and the relationships between concepts are recorded as relationships. While seem- ingly simple, as relationships themselves are defined by concepts (such as ‘IS-A’ as in “’Motor neurone disease—IS-A—Disorder of nervous system”) it means that the relationship tree is infinitely extendable over time.

![SNOMED CT ontology](assets/img/snomed.png "SNOMED CT")

SNOMED CT is owned by the SNOMED International and is an international terminology, with the UK version managed by the UK Terminology Centre (UKTC) of the Health and Social Care Information Centre (HSCIC). There are online training resources provided by SNOMED Internationalas well as a simple online SNOMED CT browser3 .

## Where might I use SNOMED CT?

You may wish to implement SNOMED CT in your application



I have developed an open-source terminology server4 that provides fast free- text search and navigation around the SNOMED CT hierarchy as well as providing semantic understanding for any concept, allowing client software to answer questions like “does this patient have a type of granulomatous disease?”, “was this patient born in Europe?” or even “is this drug a type of β-blocker?” . It would answer yes to the first question simply by understanding the diseases that the patient has been listed as having, answering ‘yes’ if a patient had sarcoidosis and ‘no’ if they had multiple sclerosis. Similarly, it would respond with ‘yes’ if a patient was recorded as being born in France but ‘no’ if they were born in Afgh- anistan. SNOMED CT provides the logical relationships in order to drive such computerised decision-making.

- useful to understand the logical model - ie concepts, descriptions, relationships, reference set items

- useful to spend some time browsing SNOMED CT using e.g. the UK browser. Other editions are available internationally


* [SNOMED-CT Browser](https://termbrowser.nhs.uk/?)
* [SNOMED CT starter guide](https://confluence.ihtsdotools.org/display/DOCSTART)    
    - SNOMED Basics
    - [SNOMED logical model](https://confluence.ihtsdotools.org/display/DOCSTART/5.+SNOMED+CT+Logical+Model)


