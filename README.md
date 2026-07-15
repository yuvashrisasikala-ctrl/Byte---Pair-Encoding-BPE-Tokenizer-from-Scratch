# Byte Pair Encoding (BPE) Tokenization Project

## 1. Project Overview

This project implements **Byte Pair Encoding (BPE)**, a subword tokenization technique commonly used in Natural Language Processing (NLP). The program reads words from a text corpus, splits them into individual characters, identifies the most frequent adjacent symbol pairs, and repeatedly merges them to create subword tokens. The project also supports encoding and decoding of words using the learned BPE rules.

## 2. Objective

The main objective of this project is to understand and implement the **Byte Pair Encoding algorithm** for text tokenization. It aims to:

* Read and process text from a corpus file.
* Convert words into character-level tokens.
* Find frequently occurring adjacent symbol pairs.
* Merge frequent pairs to generate subword tokens.
* Build a final BPE vocabulary.
* Encode new words using learned BPE rules.
* Decode tokens back into their original words.

## 3. Features

* Reads input words from a `corpus.txt` file.
* Converts text into lowercase for consistent processing.
* Creates an initial character-level vocabulary.
* Calculates word frequency statistics.
* Identifies the most frequent adjacent token pairs.
* Performs multiple BPE merge operations.
* Generates a final subword vocabulary.
* Displays learned merge rules.
* Supports BPE encoding of sample words.
* Supports decoding of tokens back to words.

## 4. Applications

Byte Pair Encoding is widely used in Natural Language Processing applications such as:

* Machine Translation
* Large Language Models
* Text Generation
* Chatbots
* Sentiment Analysis
* Search Engines
* Speech Processing
* Handling unknown and rare words
* Subword tokenization in modern NLP systems

## 5. Project Structure

```text
BPE_Tokenization_Project/
│
├── BPE_Tokenization.ipynb    # Main Jupyter Notebook
├── corpus.txt                # Input text corpus
└── README.md                 # Project documentation
```

## 6. Workflow

The project follows the steps below:

**Step 1: Read Corpus**
The program reads the input words from the `corpus.txt` file.

**Step 2: Text Preprocessing**
The words are converted to lowercase and empty lines are removed.

**Step 3: Initial Tokenization**
Each word is divided into individual characters, and the end-of-word symbol `</w>` is added.

Example:

```text
low → l o w </w>
```

**Step 4: Count Adjacent Pairs**
The program counts the frequency of adjacent symbol pairs.

Example:

```text
(l, o)
(o, w)
(w, </w>)
```

**Step 5: Find the Most Frequent Pair**
The pair with the highest frequency is selected.

**Step 6: Merge Tokens**
The selected pair is merged into a single subword token.

Example:

```text
l + o → lo
```

**Step 7: Repeat the Process**
The counting and merging process is repeated for a fixed number of iterations.

**Step 8: Generate Final Vocabulary**
The final set of characters and subword tokens is created.

**Step 9: Encoding**
New words are converted into BPE tokens using the learned merge rules.

**Step 10: Decoding**
The encoded tokens are joined together to reconstruct the original word.

## 7. Technologies Used

* **Python** – Main programming language
* **Jupyter Notebook** – Development and execution environment
* **NumPy** – Used for frequency statistics
* **Collections.Counter** – Used to count adjacent token pairs
* **Text File (`corpus.txt`)** – Used as the input corpus

## 8. Algorithm Used

### Byte Pair Encoding (BPE) Algorithm

1. Read all words from the input corpus.
2. Split each word into individual characters.
3. Add the end-of-word symbol `</w>`.
4. Count the frequency of all adjacent symbol pairs.
5. Find the most frequent pair.
6. Merge the most frequent pair into a new token.
7. Store the merge rule.
8. Repeat the process for a specified number of iterations.
9. Generate the final subword vocabulary.
10. Use the learned rules to encode and decode words.

## 9. Application Result

The program successfully:

* Reads the input corpus.
* Creates initial character-level tokens.
* Calculates word frequency statistics.
* Learns frequent BPE merge rules.
* Generates a final subword vocabulary.
* Encodes sample words into BPE tokens.
* Decodes the tokens back into the original words.

### Sample Input

```text
low
low
lowest
newer
newest
wide
wider
```

### Sample Testing Words

```text
newest
lowest
lower
```

The program displays the encoded tokens and successfully reconstructs the original words through decoding.

## 10. Conclusion

This project successfully demonstrates the working of the **Byte Pair Encoding (BPE) tokenization algorithm**. It shows how words can be divided into smaller subword units by repeatedly merging frequently occurring character pairs. BPE helps reduce vocabulary size and efficiently handles rare or unknown words. This project provides a basic understanding of subword tokenization techniques used in modern Natural Language Processing and Large Language Models.
