# Word Vectors
> A (word) type is an element of a vocabulary; a word in the abstract. A (word) token is an instance of a type in context.

- **Word Type**: A unique word in a language, irrespective of how often it is used.
- **Word Token**: Each occurrence or instance of a word in a text.

## Human and Language

- Human languages are tools for efficient communication, enabling us to share and store complex ideas, facts, and intentions.
- The capability of complex communication through language is a unique aspect of human intelligence compared to other species.
- Human language is a crucial area of interest for scientists and engineers focusing on creating and studying intelligent systems. It is a subject worthy of study due to its evolution to be learnable and useful and serves as a significant means of interaction with humans. This is especially relevant in contexts where other modalities, like vision, are also important.

## Representing Words

1. **Signifiers and Signified**:
    - Words are symbols that represent entities or concepts in the real or imagined world. For instance, "Zuko" represents a specific entity, while "tea" can refer to a specific instance or a broader class of tea.
    - The complexity of word meanings arises from the goals of human communication and the discrete symbolic structure of language. This makes representing words a challenging and intriguing problem.
2. **Independent Words, Independent Vectors**:
    - Words can be represented as independent, unrelated entities in a set, like {tea, coffee, antiridate}.
    - A word type is an abstract element of vocabulary, while a word token is a specific instance of that type in context. The representation provides a single representation for each word type, applicable to any occurrence of the word token.

    
    > **A (word) type is an element of a vocabulary; a word in the abstract. A (word) token is an instance of a type in context.**
    > 
3. **Vectors from Annotated Discrete Properties**:
    - This approach involves representing word semantics as a collection of features and relationships to linguistic categories and other words, rather than as one-hot vectors.
    - Examples include grammatical information (e.g., plurality), derivational information (e.g., "runners" from "to run"), and semantic information (e.g., "runners" as a hyponym of humans).
    - Resources like WordNet and UniMorph provide annotations for synonyms, hyponyms, and morphology across languages. However, these methods are not the norm due to limitations like incomplete vocabulary coverage, high-dimensional vectors required, and the tradeoff between dimensionality and utility.

### **One-hot Vectors**:

Each word in the vocabulary is represented by a vector where one element is 1, and all others are 0.

- **Example**:
    - For the word "tea", its one-hot vector representation might be 0,0,1,.....,0, denoted as $\text{v}_\text{tea}$ = $e_3$, the third standard basis vector.
    - For the word “coffee”, its one-hot vector could be represented as …., 0, 1, …, 0, denoted as $v_{coffee} = e_j$, the jth standard basis vector.
- **Why Use One-hot Vectors?**:
    - One-hot vectors are used to differentiate words in computational models. They ensure that different words are represented as different vectors.
    - However, one-hot vectors do not encode any meaningful notion of similarity or other relationships between words. For example, the dot product between any two different one-hot vectors is always 0, indicating that all words are equally dissimilar from each other, which is not representative of actual language use.

      ![1](https://github.com/ksdiwe/Blogs/assets/20944950/149e2baf-fd8a-44d7-af30-e6b41e08c3de)

## Distributional semantics and Word2vec

**The distributional hypothesis: the meaning of a word can be derived from the distribution of contexts in which it appears.**

### Co-occurrence matrices and document contexts
  - **Co-occurrence Matrices**: This concept revolves around the idea that the meaning of a word can be represented by the distribution of other words that occur around it. To code this concept:
