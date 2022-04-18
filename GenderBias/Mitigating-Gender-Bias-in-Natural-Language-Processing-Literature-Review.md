# Gender Bias

Gender bias is the preference or prejudice toward one gender over the other. 

This has real-world consequences; for example, concerns have been raised about automatic resume filtering systems giving preference to male applicants when the only distinguishing factor is the applicants’ gender.

### Categorization:

1. **Allocation Bias:**  economic issue in which a system unfairly allocates resources to certain groups over others. _Seen when models perform better on majority gender data._
2. **Representation Bias:** systems detract from the social identity and representation of certain group. _Seen within word embeddings and latent representations_
3. **Recognition Bias:** involves a given algorithm’s inaccuracy in recognition tasks
4. **Under-Representation Bias:** is the disproportionately low representation of a specific group.

## Observing Gender Bias:

1. **Adopting Psychological Tests:** Human tests like Implicit Association Test (_used to measure subconscious gender bias in humans_. Using time and accuracy as metrics for similar and different word-concept-associations) can be used as basis for tests like the Word Embedding Association Test (WEAT) /  Sentence Encoder Association
Test (SEAT).
2. **Analyzing Gender Sub-space in Embeddings:** A list of gender-specific words and gender-neutral words are articulated from the dataset. Authors then identify a gender direction by aggregating ten gender pairs (_her-his, she-he, etc._) and using PCA to find a single eigenvector that exhibits significantly greater variance than the rest. This eigen vector is then assessed within a gender-neutral word collection. Taken as the sub-space if these gender-neutral words display associations to particular genders, bias can be seen. However, removing this specific eigenvector may not mitigate bias, as gender-biased words still seem to cluster together --> `Cluster bias` of a word can be measured as the % of male or female stereotypical words among the k-NN of word's embedding.
3. **Measuring Performance Differences Across Genders:** `Gender-swapping` can be generalized to sentences by swapping each male-definitional word with its respective female equivalent and vice-versa for assessing model predictions. Difference in evaluation scores will show the ingrained bias. `Metrics in Abusive language detection` - False Positive Equality Difference (FPED) and False Negative Equality Difference (FNED), i.e. differences in the FPR and FNR for original and gender-swapped inputs.
_**Note:**_  Gender Bias Evaluation Testsets --- datasets to isolate the effect of gender of the output in order to be able to probe gender bias.
