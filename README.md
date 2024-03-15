### Text Similarity Analysis with Stemming, Stop-word Removal, and Vector Encoding

This repository contains Python code and analysis for assessing the similarity between two short pieces of English text. The evaluation involves experimenting with different preprocessing techniques such as stemming, stop-word removal, and various vector encoding methods to understand their impact on similarity assessment.

### Analysis

#### 1. Stop-word Removal Impact

- **Stop-word removal increases recall:**
  - Experimented by setting `to_stem` to False and `encoding_type` to one-hot.
  - Selected pairs of sentences where removing stop-words increased the similarity score.
  - Demonstrated how the similarity scores changed before and after stop-word removal.

- **Stop-word removal decreases precision:**
  - Similar approach as above, but focused on pairs of sentences where precision decreased after stop-word removal.

#### 2. Stemming Impact

- **Stemming increases recall:**
  - Tested with `stop_word_removal` set to False and `encoding_type` to one-hot.
  - Selected pairs where stemming increased the similarity score.

- **Stemming decreases precision:**
  - Conducted experiments similar to the previous case but focused on pairs where precision decreased after stemming.

#### 3. Impact of Vector Encoding Methods

- **Bag of words vs. one-hot encoding:**
  - Both `to_stem` and `stop_word_removal` set to False.
  - Demonstrated how bag of words encoding resulted in higher precision compared to one-hot encoding.

- **TF vs. bag of words:**
  - Similar setup as the previous case but compared TF encoding with bag of words.

- **TF-IDF vs. TF:**
  - Continued with the same setup but compared TF-IDF encoding with TF.

### Code

The Python code for the implementation of the text similarity assessment function and the experiments conducted for the analysis can be found in the provided Python files.

### Update - Building Lexicon

To build a lexicon for this assignment, one approach is provided below:

```python
import nltk

nltk.download('words')

english_words = set(nltk.corpus.words.words())
```

This code snippet fetches English words from NLTK's corpus, which can be used as a lexicon for preprocessing tasks like stop-word removal.

### Conclusion

The analysis and experiments conducted provide insights into how different preprocessing techniques and vector encoding methods impact the assessment of text similarity. By examining various scenarios and test cases, we can better understand the nuances of similarity assessment in natural language processing tasks.
