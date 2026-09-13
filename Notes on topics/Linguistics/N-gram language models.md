#AI #Language #Coding 
### N-gram models

Prediction of words given the previous words given. The definition of the probability of a given word is given:

**General N-gram**: $P(w|w_{n-N+1}:w_{n-1})=C(w_{n-N+1}:w_{n-1}, w) / C(w_{n-N+1}:w_{n-1})$

**Unigram**: $P(w)$
**Bigram**: $P(w|w_{n-1})$
**Trigram**: $P(w|w_{n-2}:w_{n-1})$

In the model, every sentence is in \<s>...\</s>, so $p(w|<s>)$ means first word probability.

**Chain Rule**
With a sentence of words: $w_1, w_2, ..., w_n$, we have
$$
P(w_1:n)=P(w_1)P(w_2|w_1)P(w_3|w_1:w_2)...P(w_n|w_1:w_{n-1})
$$

**Python implementation**
Using nltk we can find N-grams:

![[Screenshot 2026-03-10 at 13.38.42.png|300]]

and count them (For bigrams)

![[Screenshot 2026-03-10 at 13.40.55.png|300]]

###### Maximum Likelihood Estimation
Tæl antal special cases og del med antal totale cases - Behøver ikke at være så svært:
- "Katten spiser en bolle med muskatnødskompot"
- P(Katten) = 1 / 6
- P(muskatnødskompot | med) = 1 / 1

#### Training, Development, Test Sets
Don't use the full set of data/sentences to train the set:
- **Training**: 80%
- **Validation:** 10% - Used to fine-tune
- **Testing**: 10% - Measure performance

**Perplexity**
Perplexity is per-word normalized, allowing comparison across texts of
different lengths
$perplexity(W)=P(w_1 w_2 ...w_N)^{-1/N}$
I dont fucking know - Men lavere perplexity er bedre åbenbart

Men meget små sandsynligheder kan potentielt føre til numerisk underflow (for lav værdi til floating point numbers) - **Log Probabilities**

In log space, addition replaces multiplication: $log(p_1\times p_2)=log(p_1)+log(p_2)$, so:
$$p_1 p_2...p_n=exp(log(p_1)+log(p_2)+...+log(p_n))$$


**All in all in python:**

Compute probabilities (Bigrams and unigrams)
![[Screenshot 2026-03-10 at 14.27.42.png|400]]

Calculate perplexity
![[Screenshot 2026-03-10 at 14.29.41.png|400]]

#### More stuff i guess
Unseen Sequences = Zeros
Any finite corpus will miss some acceptable word sequences, resulting in zero probability estimates

Solution: Smoothing techniques assign small non-zero probability to unseen n-gram

**Smoothing (Discounting)** 
Algorithms that shave off probability mass from frequent events and
redistribute it to unseen events

**Laplace smoothing:** Add *one* to all n-gram counts before normalizing
- $P(w_i)=(c_i+1)/(N+V)$, where $V$ is vocab size, $c_i$ is count of word $w_i$
 ![[Screenshot 2026-03-10 at 14.45.55.png|300]]
 ![[Screenshot 2026-03-10 at 14.49.27.png|300]]

**Flexible smoothing**: Add fractional count k instead of 1
- $P(w_i)=(c_i+1)/(N+kV)$, $k$ is learned from devset(?) to optimize performance
- Useful for text classification, but not recommended for large language models

**Combining N-grams**
Combine unigram, bigram, and trigram probabilities with weighted average
$$P(w_n|w_{n-2}:w_{n-1}) = λ_1P(w_n) + λ_2P(w_n|w_{n-1}) +
λ_3P(w_n|w_{n-2}:w_{n-1})$$
1. **Simple Linear**: Fixed λ-weights for all contexts
2. **Conditional**: λ-weights depends on context


