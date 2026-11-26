
# WEEK 6 – LLM Evaluation using Golden Set and Baseline Results

## 1. Aim

To evaluate Large Language Model (LLM) responses using a Golden Set dataset and Baseline Results by comparing generated answers with expected answers, matching keywords, calculating scores, and identifying PASS or REVIEW status.

## 2. Technologies Used

- Python
- JSON
- CSV
- Requests
- Llama 3.2
- Keyword Matching
- Baseline Evaluation

## 3. Folder Structure

```text
WEEK6/
├── golden_set.json
├── baseline_results.csv
├── requirements.txt
└── README.md
```

## 4. Installation

### Step 1: Activate the Shared Virtual Environment

Open the terminal and execute:

```powershell
cd C:\GENAI
.\venv\Scripts\Activate.ps1
```

### Step 2: Navigate to Week 6

```powershell
cd PRACTICAL\WEEK6
```

### Step 3: Install Dependencies

```bash
pip install -r requirements.txt
```

## 5. Configuration

The project uses two important files:

### 1. golden_set.json

Contains 30 evaluation questions with the following details:

- Question ID
- Question
- Expected Answer
- Keywords
- Source Reference

### 2. baseline_results.csv

Contains baseline evaluation information with the following details:

- Question ID
- Question
- Expected Answer
- LLM Answer
- Matched Keywords
- Missing Keywords
- Score
- Status
- Source
- Model
- Release

**Model Used:**

```text
llama3.2
```

**Release:**

```text
v0.1
```

## 6. Implementation Steps

1. Prepare a Golden Set containing evaluation questions.
2. Define expected answers for each question.
3. Identify important keywords for every question.
4. Store the questions in JSON format.
5. Use LLM-generated answers as baseline responses.
6. Compare generated answers with expected answers.
7. Identify matched keywords.
8. Identify missing keywords.
9. Calculate evaluation scores.
10. Assign PASS or REVIEW status based on evaluation results.
11. Store the baseline evaluation results in CSV format.

## 7. Execution

The project contains the Golden Set and Baseline Results datasets.

### Step 1: Inspect the Golden Set

Run the following command:

```bash
python -c "import json; print(len(json.load(open('golden_set.json', encoding='utf-8'))))"
```

This command displays the total number of evaluation questions available in the Golden Set.

### Step 2: Inspect the CSV File

Run:

```bash
python -c "import csv; f=open('baseline_results.csv', encoding='utf-8-sig'); print(next(csv.reader(f)))"
```

This command displays the column names available in the baseline results CSV file.

**Note:** The uploaded project contains the Golden Set and Baseline Results datasets but does not include a Python evaluation script for generating new baseline results.

## 8. Sample Input

**Question:**

```text
What is tokenization in large language models?
```

**Expected Answer:**

```text
Tokenization is the process of splitting input text
into smaller units called tokens.
```

**Keywords:**

- splitting
- text
- tokens

## 9. Expected Output

The project provides baseline evaluation results containing:

- Expected Answers
- LLM-Generated Answers
- Matched Keywords
- Missing Keywords
- Evaluation Scores
- PASS or REVIEW Status

### Baseline Dataset Summary

| Metric | Value |
|---|---:|
| Total Questions | 30 |
| PASS | 12 |
| REVIEW | 18 |
| Model | llama3.2 |
| Release | v0.1 |

## 10. Result

Successfully organized a Golden Set dataset and baseline LLM evaluation results to analyze generated answers using expected answers, keyword matching, evaluation scores, and PASS or REVIEW status.
