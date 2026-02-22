# M. Siddartha Reddy
# 700774070

## home-assignment-2
## Q5 ) 3.

This code evaluates a **multi-class classifier** using a **confusion matrix** (rows = predicted classes, columns = true classes).

* **Diagonal values** = correct predictions (**True Positives**)
* **Row sums** = total predicted for each class (used for **Precision**)
* **Column sums** = total actual for each class (used for **Recall**)

### Metrics computed

* **Per-class Precision**: how often each predicted class is correct
* **Per-class Recall**: how many actual items of each class were found

### Averages

* **Macro average**: average of class-wise metrics (treats all classes equally)
* **Micro average**: computes using all predictions together (gives more weight to larger classes)

This helps measure model performance more clearly than using only accuracy.




## Q5 , 3. Programming ImplementationWrite Python code that:
## . Accepts the confusion matrix above as input.
## . Computes per-class precision and recall.
## . Computes macro-averaged and micro-averaged precision and recall.
## . Prints all results clearly.


A **bigram language model** estimates the probability of a word based only on the **previous word**.

Instead of modeling the full sentence directly, it uses:

[
P(w_1, w_2, ..., w_n) = approx _ P(w_i | mid w_{i-1})
]

In this assignment, bigram probabilities are computed using **Maximum Likelihood Estimation (MLE)**:

[
P(w_i \mid w_{i-1}) = Count}(w_{i-1}, w_i)} / {Count}(w_{i-1})}
]

The program:

* reads the training corpus,
* computes **unigram counts** and **bigram counts**,
* calculates **bigram MLE probabilities**,
* computes the probability of a given sentence by multiplying its bigram probabilities.

The model prefers the sentence with the **higher probability**.
For this corpus:

* (P(<s> I love NLP  </s>) = 1/3)
* (P(<s> I love deep learning </s>) = 1/6)

So, the model prefers **“<s> I love NLP </s>”** because it has a higher probability.


Tiny caveat (the fun kind): with plain **MLE and no smoothing**, any unseen bigram gets probability **0**, which can make a whole sentence probability zero.

