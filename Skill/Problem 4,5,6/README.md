
# Problems 4, 5 and 6 – Tokenization and LLM Budget Estimation

## 1. Aim

To explore different tokenization techniques, compare tokenization results across multiple languages, estimate LLM API costs and rate limits, and validate budget calculations using automated unit testing.

## 2. File Name

`Problem4,5,6.ipynb`

## 3. Description

This notebook covers three major problems.

**Problem 4 – Tokenizer Vocabulary and Comparison**

Uses GPT-2, BERT, and mT5 tokenizers to understand vocabulary size, token generation, token IDs, and multilingual tokenization.

**Problem 5 – LLM Feature Budget Estimation**

Calculates the monthly token consumption, API costs in USD and INR, peak requests per minute (RPM), peak tokens per minute (TPM), and budget feasibility for a Customer Support AI Assistant.

**Problem 6 – Budget Estimator and Unit Testing**

Creates a reusable Python budget calculation module and tests it using Python's `unittest` framework.

## 4. Concepts Used

- Natural Language Processing (NLP)
- Tokenization
- Byte Pair Encoding (BPE)
- WordPiece
- SentencePiece
- GPT-2, BERT and mT5
- Vocabulary Size
- Multilingual Tokenization
- LLM API Cost Estimation
- Input and Output Tokens
- Requests Per Minute (RPM)
- Tokens Per Minute (TPM)
- USD to INR Conversion
- Budget Feasibility
- Python Functions and Dataclasses
- Unit Testing

## 5. Implementation Steps

### Problem 4 – Tokenizer Vocabulary and Comparison

1. Install the Transformers and SentencePiece libraries.
2. Load the GPT-2 tokenizer.
3. Display its vocabulary size.
4. Tokenize words such as Artificial, Intelligence, learning, and computer.
5. Compare GPT-2, BERT, and mT5 tokenizers using the same English sentence.
6. Display tokens, token IDs, number of tokens, and vocabulary sizes.
7. Use mT5 to tokenize English, Telugu, and Hindi sentences.
8. Process additional multilingual sentences.

### Problem 5 – LLM Feature Budget Estimation

1. Define the feature name and traffic assumptions.
2. Set daily active users and requests per user.
3. Define average input and output tokens.
4. Select the model pricing preset or custom pricing.
5. Set the USD-to-INR conversion rate.
6. Configure provider RPM, TPM, and monthly budget limits.
7. Calculate monthly requests and token consumption.
8. Calculate input, output, and total API costs.
9. Calculate peak RPM and TPM.
10. Display the final budget and capacity verdict.

### Problem 6 – Budget Estimator and Unit Testing

1. Create `budget_estimator.py`.
2. Define the `BudgetReport` dataclass.
3. Implement the `calculate_budget()` function.
4. Create `test_budget.py`.
5. Define five test cases using `unittest`.
6. Execute the tests using:

   ```bash
   python -m unittest test_budget.py -v
   ```

7. Verify that all five tests pass.

## 6. Requirements

- Python 3
- Google Colab or Jupyter Notebook
- Transformers
- SentencePiece
- Requests
- Pandas (if used for further analysis)
- Internet connection for downloading pretrained tokenizers

The budget estimator and unit tests use Python standard libraries.

## 7. How to Execute

1. Open `Problem4,5,6.ipynb` in Google Colab.
2. Run the installation and import cells.
3. Execute the tokenizer comparison sections.
4. Run the multilingual tokenization section.
5. Execute the LLM budget estimator.
6. Check the monthly cost and rate-limit results.
7. Run the cells that create `budget_estimator.py` and `test_budget.py`.
8. Execute the unit tests.
9. Check the final test results.

## 8. Program Outputs and Explanation

### Problem 4 – Tokenizer Outputs

**Output 1: GPT-2 Vocabulary Size**

```text
Total Vocabulary Size: 50257
```

**Explanation:** The GPT-2 tokenizer contains 50,257 vocabulary entries. The notebook also displays tokens and token IDs for four sample words.

**Output 2: Tokenizer Comparison**

| Tokenizer | Number of Tokens | Vocabulary Size |
|---|---:|---:|
| BPE – GPT-2 | 8 | 50,257 |
| WordPiece – BERT | 8 | 30,522 |
| SentencePiece – mT5 | 9 | 250,100 |

**Explanation:** The same English sentence is processed using three different tokenizers. Each tokenizer generates different token sequences and vocabulary sizes.

**Output 3: Multilingual Tokenization**

The mT5 tokenizer processes English, Telugu, and Hindi sentences.

| Language | Total Tokens |
|---|---:|
| English | 7 |
| Telugu | 21 |
| Hindi | 17 |

**Explanation:** The results demonstrate how one tokenizer handles different languages and how the number of tokens varies depending on the language and text.

### Problem 5 – LLM Budget Estimator Output

**Output 1: Traffic and Token Consumption**

```text
Total Requests:       600,000 req/month
Input Tokens:         720,000,000 tokens
Output Tokens:        210,000,000 tokens
Total Tokens:         930,000,000 tokens
```

**Explanation:** The program calculates monthly requests and total input and output token consumption based on 5,000 daily active users and four requests per user per day.

**Output 2: Estimated API Cost**

```text
Input Cost:           ₹50,365.80 ($540.00)
Output Cost:          ₹73,450.12 ($787.50)
Total Monthly Cost:   ₹123,815.92 ($1,327.50)
Cost per Request:     ₹0.2064
Cost per Active User: ₹24.76 / month
```

**Explanation:** The program calculates API costs using the selected Gemini 3.8 Flash pricing preset and converts the total USD cost into Indian Rupees.

**Output 3: Rate Limit Feasibility**

```text
Estimated Peak RPM: 41.7 / 2,000 RPM (2.1%)
Estimated Peak TPM: 64,583 / 1,000,000 TPM (6.5%)
```

**Explanation:** The estimated peak requests and tokens are below the configured provider limits. Therefore, both RPM and TPM checks pass.

**Output 4: Final Verdict**

```text
Budget Check: FAIL
Over budget by ₹73,815.92
247.6% used

RPM Limit Check: PASS
TPM Limit Check: PASS
```

**Explanation:** The monthly estimated cost exceeds the configured ₹50,000 budget. However, the estimated traffic remains within the RPM and TPM limits.

### Problem 6 – Unit Testing Output

The notebook creates two Python files:

- `budget_estimator.py`
- `test_budget.py`

It performs five automated tests.

| Test Case | Purpose | Result |
|---|---|---|
| `test_token_and_inr_cost_calculation` | Verifies token counts and cost calculations | PASS |
| `test_budget_exceeded` | Checks monthly budget failure | PASS |
| `test_rate_limits_within_capacity` | Checks RPM and TPM within limits | PASS |
| `test_rpm_and_tpm_limits_exceeded` | Checks rate-limit violations | PASS |
| `test_zero_traffic_edge_case` | Checks calculations when there are no active users | PASS |

**Actual Test Output:**

```text
Ran 5 tests in 0.001s

OK
```

**Explanation:** All five tests passed successfully. This confirms that the budget calculation function handles normal conditions, budget violations, rate-limit violations, and zero-traffic conditions as expected.

## 9. Learning Outcomes

After completing these problems, I learned:

- How to load and compare pretrained tokenizers.
- How GPT-2, BERT, and mT5 generate tokens.
- How to perform multilingual tokenization.
- How to calculate vocabulary sizes and token counts.
- How to estimate LLM monthly token consumption.
- How to calculate API costs in USD and INR.
- How to check RPM and TPM limits.
- How to create reusable Python modules.
- How to implement automated unit testing.
- How to validate budget calculations under different conditions.

## 10. Conclusion

These three problems demonstrate important concepts in Generative AI and Natural Language Processing. The notebook compares tokenization methods, performs multilingual tokenization, estimates LLM API costs and resource requirements, and validates the calculations using automated unit tests. All five unit tests completed successfully.
