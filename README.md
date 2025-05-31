# NaiveBayes-Autocorrect
A simple Naive Bayes-based autocorrect system using edit distance for likelihood estimation. It calculates posterior probabilities to suggest the most likely correct words for a misspelled input based on a small unigram corpus.


# Naive Bayes Autocorrect System

This project implements a basic autocorrect system using a Naive Bayes approach. It suggests corrections for misspelled words by calculating the posterior probability of each candidate word based on:

- **P(C)**: Prior probability of the correct word (from word frequency)
- **P(W|C)**: Likelihood estimated using edit distance

### 🔍 Example

```python
misspelled_word = "helo"
````

Returns top suggestions like:

```
hello (Probability: 0.1)
```

### 📦 Dependencies

* Python
* `editdistance`
* `collections.Counter`

Install with:

```bash
pip install editdistance
```

### 📁 How It Works

* A sample vocabulary (corpus) is used with word counts.
* For each word in the corpus, it calculates:

  * **Prior**: frequency of the word
  * **Likelihood**: `1 / (edit distance + 1)`
  * **Posterior**: `prior × likelihood`
* Returns top N candidate corrections.

### 🚀 Run the Code

Simply run the Python script after installing the dependency.

### ⚙️ Future Improvements

* Use a larger corpus
* Add bigram or context-based modeling
* Improve likelihood estimation with real typo patterns
