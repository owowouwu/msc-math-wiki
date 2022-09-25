Stands for Term Frequency Inverse Document Frequency.

Used in NLP.

## Definition

Let $t$ be a term, and $d$ be a document

$w_{d,t} = f_{d,t} \times \log \frac{N}{f_t}$

where $f_{d,t}$ is the frequency of term $t$ in document $d$, and $f_t$ is the number of documents containing $t$ ($d$ marginalised out)

## Intuition

To be relevant, a word should be both

- frequent enough in the corpus
- "special enough" in the sense that it occurs in less documents


