# Programming Historian Lab Worksheet

Name: Abhi Mummaneni

## 1. What is the citation for the _Programming Historian_ lesson associated with this lab?

Avery Blankenship, Sarah Connell, and Quinn Dombrowski, "Understanding and Creating Word Embeddings," Programming Historian 13 (2024), <https://doi.org/10.46430/phen0116>.

## 2. What Python libraries does the lesson require you to download? (Use Markdown's list syntax to list them.)

The lesson requires:

- re
- os
- gensim
  - Word2Vec
- string
- glob
- pathlib
  - Path
- pandas

## 3. What aspects, if any, of the lab are out of date? How would you fix them?

The lab focuses on the older word2Vec algorithm instead of newer transformer based models, however this can be seen as a deliberate decision since the older Word2Vec models are more interpretable and easier to learn.
Some actual outdated aspects include the lesson using older versions such as Python 3.8.3 and Gensim 4.2.0 which are not current versions. However, since the code doesn't pin these versions, it doesn't effect the student since environments will choose the more modern versions.

## 4. What was the most important thing that you learned from this lab?

The most important thing I learned was the architecture of word embedding models and what linear analogies (such as e(king) - e(man) + e(woman) = e(queen)) actually mean from a probabilistic standpoint. I used the following sources to further understand these concepts:

- Omer Levy and Yoav Goldberg. 2014. Neural word embedding as implicit matrix factorization. In Proceedings of the 28th International Conference on Neural Information Processing Systems - Volume 2 (NIPS'14), Vol. 2. MIT Press, Cambridge, MA, USA, 2177–2185. <https://proceedings.neurips.cc/paper_files/paper/2014/file/b78666971ceae55a8e87efb7cbfd9ad4-Paper.pdf>
- Kawin Ethayarajh, David Duvenaud, and Graeme Hirst. 2019. Towards Understanding Linear Word Analogies. In Proceedings of the 57th Annual Meeting of the Association for Computational Linguistics, pages 3253–3262, Florence, Italy. Association for Computational Linguistics. <https://aclanthology.org/P19-1315.pdf>

I learned in what sense this algebra on word embeddings is precise and how it depends on and reflects the word co-occurrence distribution of the underlying corpus. This helped me understand the limitations of how word embeddings can be used to capture semantic relationships between words and what conclusions can be drawn from these relationships.
Furthermore, I learned how these models are used in a research setting, and what types of questions these methods are used to solve in computational digital humanities.

## 5. Design and briefly outline a follow-up _Programming Historian_ lesson

What skills would you build on? How would you measure results?

I would add a follow-up which includes more emphasis on how these embeddings are a function of the underlying corpus. The goal would be that students understand how these embeddings are explicitly calculated, what the embeddings actually mean, and to what degree algebra on the embeddings is permissible.
The lesson would start by outlining the specific loss function of the Word2Vec algorithm and how learning word embeddings under this optimization can be interpreted probabilistically.
Furthermore, the lesson would use multiple corpora and have students train the same model over each of them before evaluating the model and creating inferences form its output.
This would let students see how the model behaves differently when trained on a different corpus and highlights the embeddings as a function of the data.
I would measure results by assessing if students can clearly explain the general architecture of Word2Vec and how these embeddings are created. I would also verify that students can interpret the differences in model behavior by asking them to explain what has caused the difference in the model outputs and what implications this has.
