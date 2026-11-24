# WEEK 5 – Token Economics

## 1. Aim

To calculate and analyze token usage, API costs, rate limits, and budget requirements for an AI-based application.

## 2. File Name

`week5.ipynb`

## 3. Description

This experiment demonstrates how to estimate the cost and resource requirements of using a Large Language Model (LLM).

The program calculates daily and monthly input and output token usage, estimates API costs, checks Requests Per Minute (RPM) and Tokens Per Minute (TPM) limits, and verifies whether the estimated costs are within the configured budget.

It also uses Python's `unittest` framework to test the correctness of the calculations.

## 4. Concepts Used

- Token Economics
- Input and Output Tokens
- API Cost Estimation
- Requests Per Minute (RPM)
- Tokens Per Minute (TPM)
- Daily and Monthly Budget
- Safety Margin
- Python Dataclasses
- Unit Testing
- ValueError Handling

## 5. Implementation Steps

1. Import the required Python modules:
   - `os`
   - `unittest`
   - `dataclass` from `dataclasses`

2. Create a `FeatureBudget` class to store usage assumptions, token prices, rate limits, and budget limits.

3. Implement the `calculate()` method to calculate:
   - Daily input tokens.
   - Daily output tokens.
   - Total daily tokens.
   - Daily and monthly API costs.
   - Peak RPM and TPM with a safety margin.
   - Budget and capacity checks.

4. Define sample assumptions:
   - Requests per day: 2000
   - Average input tokens: 1200
   - Average output tokens: 300
   - Peak requests per minute: 30
   - Input price per million tokens: $0.30
   - Output price per million tokens: $1.20
   - RPM limit: 60
   - TPM limit: 100000
   - Monthly budget: $50
   - Daily budget: $2
   - Safety margin: 20%

5. Generate a Token Economics Report.

6. Perform budget and capacity checks.

7. Execute automated unit tests to verify the calculations.

## 6. Requirements

- Python 3
- Jupyter Notebook or Google Colab
- Python standard libraries:
  - `os`
  - `unittest`
  - `dataclasses`

No external packages or API keys are required.

## 7. How to Execute

1. Open `week5.ipynb` in Jupyter Notebook or Google Colab.
2. Run the code cell.
3. View the Token Economics Report.
4. Check the RPM, TPM, daily budget, and monthly budget results.
5. View the automated test results.

## 8. Program Outputs and Explanation

### Output 1: Token Economics Report

**Purpose:** Displays the calculated daily token usage and estimated API costs.

**Calculated output:**

```text
TOKEN ECONOMICS REPORT
----------------------------------------
Input tokens/day: 2,400,000
Output tokens/day: 600,000
Total tokens/day: 3,000,000

Estimated daily cost: $1.4400
Estimated monthly cost: $43.20

Peak RPM with margin: 36.0
Peak TPM with margin: 54000
```

**Explanation:**

- The application uses 2.4 million input tokens per day.
- It generates 600,000 output tokens per day.
- The total daily token usage is 3 million tokens.
- The estimated daily API cost is $1.44.
- The estimated monthly API cost is $43.20.
- After applying the 20% safety margin, peak RPM is 36 and peak TPM is 54,000.

### Output 2: Budget and Capacity Checks

**Purpose:** Checks whether the application stays within the configured RPM, TPM, daily budget, and monthly budget limits.

**Calculated output:**

```text
CHECKS
----------------------------------------
RPM capacity: PASS
TPM capacity: PASS
Daily budget: PASS
Monthly budget: REVIEW

Recommendation: REVISE assumptions, limits, or design before build.
```

**Explanation:**

- RPM capacity passes because 36 is below the limit of 60.
- TPM capacity passes because 54,000 is below the limit of 100,000.
- Daily budget passes because the cost with safety margin is $1.728, below the $2 limit.
- Monthly budget requires review because the cost with safety margin is $51.84, which exceeds the $50 limit.

Therefore, the program recommends revising the assumptions, limits, or design before building the application.

### Output 3: Automated Test Results

**Purpose:** Uses Python's `unittest` framework to verify the token cost and capacity calculations.

The notebook contains four test cases:

1. `test_cost_estimate` – Checks whether daily and monthly costs are calculated correctly.
2. `test_capacity_passes` – Checks whether RPM and TPM limits pass.
3. `test_rpm_limit_fails` – Checks whether the program identifies an RPM limit violation.
4. `test_monthly_budget_fails` – Checks whether the program identifies a monthly budget violation.

**Expected test result when executed:**

```text
Ran 4 tests

OK
```

**Explanation:** All four tests should pass if the calculations work correctly. The tests verify both successful capacity checks and situations where configured limits are exceeded.

## 9. Learning Outcomes

After completing this experiment, I learned:

- How to calculate daily and monthly token usage.
- How to estimate API costs using input and output token prices.
- How to calculate RPM and TPM requirements.
- How to apply a safety margin to resource estimates.
- How to check daily and monthly budget limits.
- How to use Python dataclasses.
- How to write automated tests using `unittest`.

## 10. Conclusion

This experiment demonstrates how Token Economics helps estimate the cost and resource requirements of an AI application. It calculates token consumption, API costs, rate limits, and budget checks. Automated testing verifies the calculations and helps identify budget or capacity issues before building the application.
