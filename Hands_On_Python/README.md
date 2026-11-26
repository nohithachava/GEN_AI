
# Hands-On Python – GPT-2 Next Token Prediction

## Project Description
This project demonstrates how to use a pretrained GPT-2 language model to predict the next possible words or tokens in a given sentence using Python.

It uses the Hugging Face Transformers library and PyTorch to load the GPT-2 model, process input text, and calculate the probabilities of the next predicted tokens.

## Technologies Used
- Python
- PyTorch
- Hugging Face Transformers
- GPT-2 Pretrained Language Model
- Jupyter Notebook

## Files in This Project
**Hans_On_Python.ipynb**

This notebook contains the Python implementation of GPT-2 next token prediction.

## Working Process
1. Import PyTorch and Transformers libraries.
2. Load the pretrained GPT-2 tokenizer and language model.
3. Provide an input sentence: `Artificial Intelligence is`.
4. Convert the input sentence into token IDs.
5. Pass the tokens through the GPT-2 model.
6. Extract the logits for the last token.
7. Apply Softmax to calculate prediction probabilities.
8. Display the top 5 most probable next tokens.

## Sample Output

**Input:**
```text
Artificial Intelligence is
```

**Top 5 Next Token Predictions:**
```text
'a'   : 14.14%
'the' : 5.72%
'not' : 4.16%
'an'  : 3.73%
'one' : 2.13%
```

*Note: Prediction probabilities may vary depending on the model version and execution environment.*

## Installation

Install the required libraries:

```bash
pip install torch transformers
```

## How to Run
1. Open the `Hans_On_Python.ipynb` file in Jupyter Notebook or Google Colab.
2. Install the required libraries.
3. Run all notebook cells.
4. View the top 5 next-token predictions.

## Learning Outcomes
- Understanding pretrained language models.
- Learning how GPT-2 tokenization works.
- Understanding logits and Softmax.
- Calculating next-token prediction probabilities.
- Working with PyTorch and Hugging Face Transformers.

## Conclusion
This project provides a basic understanding of how GPT-2 predicts the next token in a sequence. It demonstrates the fundamental working process behind next-token prediction in Generative AI and Large Language Models (LLMs).
