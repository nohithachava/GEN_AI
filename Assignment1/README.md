
# ASSIGNMENT 1 – Byte Pair Encoding (BPE) Tokenization

## 1. Aim

To implement Byte Pair Encoding (BPE) tokenization using Python and understand how frequently occurring character pairs are merged to form larger tokens.

## 2. File Name

`ASSIGNMENT1.ipynb`

## 3. Description

This assignment demonstrates a simple implementation of BPE tokenization.

The program takes four words with their frequencies:

- low: 5
- lower: 2
- newest: 3
- wildest: 6

Initially, each word is divided into individual characters. The program calculates the frequency of each character and adjacent character pair.

It then calculates a normalized score for every adjacent pair using the formula:

**Score = Pair Frequency / (Frequency of First Token × Frequency of Second Token)**

The pair with the highest score is selected and merged. This process is repeated for five iterations.

Finally, the program displays the resulting tokens and their frequencies.

## 4. Concepts Used

- Natural Language Processing (NLP)
- Byte Pair Encoding (BPE)
- Tokenization
- Character-level Tokenization
- Pair Frequency
- Normalized Pair Score
- Token Merging
- Python Dictionaries
- Counter from Collections

## 5. Implementation Steps

1. Import `Counter` from the collections module.
2. Define four input words with their frequencies.
3. Split each word into individual characters.
4. Calculate the frequency of individual tokens.
5. Calculate the frequency of adjacent character pairs.
6. Calculate normalized scores for all pairs.
7. Select the pair with the highest score.
8. Merge the selected pair in all words.
9. Repeat the merging process for five iterations.
10. Display the final tokenization and word frequencies.

## 6. Requirements

- Python 3
- Jupyter Notebook or Google Colab
- Python standard library (`collections`)

No external libraries or API keys are required.

## 7. How to Execute

1. Open `ASSIGNMENT1.ipynb` in Jupyter Notebook or Google Colab.
2. Run the code cell.
3. Observe the original words and their frequencies.
4. Check the initial character-level tokenization.
5. Observe the pair frequencies and normalized scores in each iteration.
6. Check the selected pair and merging process.
7. View the final tokenization.

## 8. Program Outputs and Explanation

### Output 1: Original Words

**Purpose:** Displays the input words and their frequencies.

**Output:**

```text
ORIGINAL WORDS:
low : 5
lower : 2
newest : 3
wildest : 6
```

**Explanation:** The program starts with four words. Their frequencies represent how often each word occurs in the input dataset.

### Output 2: Initial Tokenization

**Purpose:** Divides each word into individual characters.

**Output:**

```text
INITIAL TOKENIZATION:
l o w : 5
l o w e r : 2
n e w e s t : 3
w i l d e s t : 6
```

**Explanation:** Each word is initially represented as a sequence of individual character tokens. These tokens are used to calculate adjacent pair frequencies.

### Output 3: Pair Frequencies and Scores

**Purpose:** Calculates the frequency and normalized score of each adjacent character pair during every iteration.

**Explanation:** The program counts how frequently each adjacent pair occurs and calculates its normalized score. The pair with the highest score is selected for merging.

### Output 4: Selected Pair and Merging

**Purpose:** Displays the selected character pair and the updated words after merging.

**Explanation:** In each iteration, the selected pair is combined into a single token wherever that adjacent pair appears. The updated token sequences are used in the next iteration.

The program repeats this process five times.

### Output 5: Final Tokenization

**Purpose:** Displays the final tokens generated after five merging iterations.

**Explanation:** The final output contains:

- Original word.
- List of tokens after merging.
- Original word frequency.

This demonstrates how smaller character tokens are combined into larger subword tokens using BPE.

## 9. Learning Outcomes

After completing this assignment, I learned:

- How BPE tokenization works.
- How to split words into individual characters.
- How to calculate token and pair frequencies.
- How to calculate normalized pair scores.
- How to select the highest-scoring pair.
- How to merge adjacent tokens.
- How subword tokenization is performed using Python.

## 10. Conclusion

This assignment successfully implements a simple BPE tokenization algorithm using Python. It demonstrates character-level tokenization, pair-frequency calculation, normalized scoring, and iterative token merging. The experiment helps understand how BPE creates larger subword units from smaller character tokens.
