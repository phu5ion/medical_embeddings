# medical_embeddings
Given 2 files: 
A list of related medical entities pairs 
“MedicalConcepts.csv” contains a list of related medical entities pairs (Term1 and Term2 are related to each other) that has been curated by domain experts

Sample notes collected from patient visits
“ClinNotes.csv” contains notes (column=’notes’) from three departments (column=’category’), i.e. Cardiovascular / Pulmonary, Neurology, and Gastroenterology

I use these information and come up with two approaches to generate vector representations of medical text:
1. Word2Vec model (code under 1. Word2Vec.ipynb)
3. ClinicalBERT word/phrase embeddings (code under 2. ClinicalBERT.ipynb)

In these two notebooks, I detail my way of 
- Generating the word embedding. 
- Evaluating the generated word embeddings. My idea is that related medical concepts should be more similar in terms of clinical meaning, compared to a random word pair. Thus, we can use the MedicalConcept pairs as evaluation criteria, and the approach is detailed in both notebooks.
