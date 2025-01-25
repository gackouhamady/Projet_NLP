# LABS: Treetagger for POS-tagging


# Keywords:
- TreeTagger, POS Annotation, That, Precision, Recall, Retraining, Penn and BNC Models, C8 Tagset, Training Corpus, Comparative Analysis.

## Introduction
In this lab, we will explore the *TreeTagger* tool used for performing POS-tagging of words in a text. The focus will be on annotating the morphosyntactic category for different realizations of the word *that* in English using tagsets like CLAWS and Penn. We will also compare the performance of different models with *TreeTagger* and analyze the results based on the size of training data.

## Lab Objectives

1. **Execution of TreeTagger**: Analyze the different realizations of the word *that* (e.g., as adverb, relative pronoun, conjunction, etc.) and measure precision for each category.
2. **Retraining TreeTagger**: Use a specific tagset to distinguish the various uses of *that*.
3. **Comparative Analysis**: Compare the performance of the *Penn* and *BNC* models in TreeTagger.
4. **Precision and Recall**: Evaluate the precision and recall for annotating *that* using training and test corpora.

## 1. TreeTagger for POS-tagging
*TreeTagger* is a linguistic annotation tool that uses a probabilistic model to predict the POS categories of words in a text.

### Steps:

1. **Installation of TreeTagger**
   - Download and install *TreeTagger* by following the instructions on the official website: [TreeTagger](https://www.cis.uni-muenchen.de/~schmid/tools/TreeTagger/).
   - Ensure that Java and Perl are installed on your machine.

2. **Execution of TreeTagger**
   - Use test files to analyze the different realizations of *that*. For instance, in *BNC.par* or *Penn.par*, the word *that* should be tagged according to its specific role:
     - As an adverb (RB),
     - As a relative pronoun (WPR), or
     - As a conjunction (CJT).

3. **Testing Different Configurations**
   - Test various *TreeTagger* configurations with distinct parameter files to observe the precision of annotations obtained.
   - Example:
     ```bash
     ./tree-tagger English.par textfile.txt
     ```
     - Replace `English.par` with the desired parameter file (e.g., `penn.par` or `bnc.par`).
     - **Precision**: Compare the precision of each realization based on different training datasets.

4. **Compare Penn and BNC Models** (Bonus)
   - Using *penn.par* and *bnc.par* parameter files, compare *TreeTagger*'s performance in annotating *that* in various contexts.
     - **Penn Model**: [Penn Treebank Tagset](https://www.ling.upenn.edu/courses/Fall_2003/ling001/penn_treebank_pos.html)
     - **BNC Model**: [BNC Tagset](http://ucrel.lancs.ac.uk/claws5tags.html)

### Expected Output:
- Precision of annotated realizations for each category: Adverb (RB), Conjunction (CJT), Relative Pronoun (WPR).

## 2. Retrain TreeTagger

### Objective:
Retrain *TreeTagger* with a specific tagset to distinguish the various uses of the word *that* in English.

#### Steps:

1. **Select a Tagset**
   - Use the **C8** tagset (adapted from CLAWS8) for more precise annotation of *that*. The tagset includes categories such as:
     - `WPR`: Relative Pronoun (e.g., *The man that I saw*),
     - `CST`: Subordinating Conjunction (e.g., *The fact that*),
     - `CJT`: Conjunction for verbs (e.g., *I think that*),
     - `DT`: Singular Determiner (e.g., *that* in *that man*),
     - `RB`: Adverb (e.g., *It's not that difficult*).

2. **Retrain TreeTagger with New Tags**
   - Adapt the training model using sentences annotated with the C8 tagset.
   - To retrain *TreeTagger*, use the following command:
     ```bash
     ./tree-tagger train model.txt
     ```

3. **Measure Precision and Recall**
   - Evaluate the precision and recall of the retrained model by testing it on specific datasets.

#### C8 Tagset:
- Refer to this document for more details about the C8 tagset: [C8 Tagset](https://ucrel.lancs.ac.uk/claws8tags.pdf).

### Expected Output:
- Precision and recall report for each use of the word *that* in test datasets.

## 3. Collaborations and CRediT Attribution

If working in a team, follow the CRediT method to specify contributions. For example:
- **Conceptualization**: Hamady Gackou
- **Implementation**: [Your teammate's name]

Refer to this article for more details: [Beyond authorship](https://www.researchgate.net/publication/274098676_Beyond_authorship_Attribution_contribution_collaboration_and_credit).

## 4. Submission Instructions

Submit your work file on Moodle under the appropriate sections:
- **M1 Alternance**: [Moodle M1 Alternance](https://moodle.u-paris.fr/course/view.php?id=28636#section-1)
- **M1 Initial Training**: [Moodle M1 Formation Initiale](https://moodle.u-paris.fr/course/view.php?id=28339#section-0)

### Deadline: February 9, 2025, at midnight.

## 5. Report Outline

The report must follow the ACL format (Latex or Word) and include the following sections:

### 5.1 Introduction
- Examples of *that* usage in different contexts.
- Overview of tag properties and grammatical structures.

### 5.2 Previous Work on *That* Analysis
- References to previous studies, notably on CLAWS8, Penn Treebank, and UD tagsets.

### 5.3 Methods and Tools
- Describe the reannotation and retraining method using TreeTagger.
- Present examples of reannotated sentences.

### 5.4 Results
- Baseline: Results of TreeTagger with the default parameter file.
- Partial and complete reannotation experiments.

### 5.5 Discussion
- Accuracy improvements based on the size of the training corpus.
- Impact of overfitting on certain categories (e.g., technical English).

### 5.6 Conclusion and Future Research Directions

### 5.7 Appendices
- Jupyter Notebook with reproducible experiments.
- Retraining file(s).
- Prompts used for synthetic corpora.

## Bonus: Analysis of *That* in Nominal Complements
- Study the incorporation of the [+singular] or [+plural] feature using tools like *skweak* for feature engineering.
- Analyze *that* as a pronoun in sentences like *I love that!*.

### Additional Resources
- [TreeTagger Documentation](https://www.cis.uni-muenchen.de/~schmid/tools/TreeTagger/)
- [CoreNLP Demo](https://stanfordnlp.github.io/CoreNLP/demo.html)
- [UDpipe Python Package](https://github.com/ufal/udpipe)
