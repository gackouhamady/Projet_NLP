# Refining Syntactic Distinctions Using Decision Trees: A Paper on Postnominal 'That' in Complement vs. Relative Clauses

## Author
**Hamady GACKOU**  
Student at Paris Cité University  
1 Rue Pajol, 75018 Paris, France  
hamady.gackou@etu.u-paris.fr

## Abstract
This study evaluates the performance of the TreeTagger English model developed by Helmut Schmid in analyzing relative clauses and noun complement clauses in English. The focus is on distinguishing between the uses of "that" as a relative pronoun and as a complementizer. An algorithm was employed to reannotate a corpus originally parsed using the Universal Dependency framework with the EWT Treebank. An improved model was proposed by retraining TreeTagger, and its performance was compared with Schmid’s baseline model. The study also examined the impact of varying the training dataset size on TreeTagger’s accuracy and assessed the representativeness of the EWT Treebank files for the structures under investigation.

## Introduction
### Aim of the Study
The study aims to explore the syntactic distinctions in the usage of the postnominal "that" in English subordinate clauses, focusing on complement and relative clauses. The primary objective is to refine the understanding of how "that" functions in these two distinct syntactic contexts.

### Context and Motivation
Understanding the syntactic behavior of "that" is crucial for computational linguistics and natural language processing (NLP) as it enables more accurate syntactic parsing and semantic interpretation. Previous research has highlighted the nuanced challenge of distinguishing between the complementizer and relative pronoun uses of "that".

### Research Questions
1. How can we reliably distinguish between the relative pronoun and complementizer uses of "that" in English subordinate clauses?
2. What impact does retraining the TreeTagger model have on its ability to differentiate these two syntactic roles?
3. How does the size and quality of the training dataset influence the accuracy of syntactic parsing for these structures?
4. Is the EWT Treebank a representative dataset for capturing the subtleties in the use of "that"?

## Materials and Methods
### TreeTagger Model Evaluation
The TreeTagger model was evaluated using two different Treebank models: the Penn Treebank and the BNC Treebank. The evaluation focused on the performance of the word "that" across various categories using the CLAWS5 and Penn Treebank tagsets.

### Preprocessing and Annotation
The Brown Corpus was adapted to the CLAWS C8 tagset, annotated using the UDPipe REST API, and reannotated using a heuristic method to adjust the annotations according to the CLAWS C8 tagset.

### Lexicon Creation and Re-Training
A lexicon was created from the annotated files, and the TreeTagger model was retrained using different sizes of lexicons to improve the accuracy of syntactic analyses.

## Results
### Analysis of UD EWT Treebank
The study revealed limitations in distinguishing between relative clauses and nominal complement clauses introduced by "that" in the EWT Treebank, highlighting the need for reannotation to improve accuracy and consistency.

### Model Performance
The performance of TreeTagger with the Penn Treebank and BNC Treebank models was evaluated in terms of precision, recall, and F1-score for the word "that". The results showed varying performance depending on the tagset and categories analyzed.

## Discussion
### Challenges and Improvements
The study highlighted the challenges in distinguishing between the uses of "that" and suggested improvements in corpus annotation quality, handling of lexical ambiguities, and syntactic feature engineering.

## Conclusion
The study underscores the need for more sophisticated approaches in both annotation methodologies and model architectures to improve the accuracy of syntactic parsing for ambiguous words like "that".

## References
A comprehensive list of references used in the study is provided in the original article.

## Repository
For more details and access to the code and data used in this study, please visit the GitHub repository : https://github.com/gackouhamady/Projet_NLP
