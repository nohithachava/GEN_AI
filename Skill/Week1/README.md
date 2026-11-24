# WEEK 1 – LLM Model Implementation

## File Name
`Week1_llm_Model.ipynb`

## 1. Aim
To connect a Python application with Google's Gemini Large Language Model (LLM) and generate AI-based responses using a user prompt.

## 2. Description
This practical demonstrates how to integrate the Gemini AI model into Python using the Google Gen AI SDK. It retrieves an API key securely from Google Colab Secrets, initializes the Gemini client, sends a prompt to the model, and displays the generated response.

## 3. Concepts Used
- Generative Artificial Intelligence
- Large Language Models (LLMs)
- Google Gemini API
- Python programming
- API key authentication
- Prompt engineering
- AI response generation

## 4. Implementation Steps

### Step 1: Install Google Gen AI SDK
```python
!pip install -q google-genai
```
Installs the Google Gen AI library required to communicate with Gemini.

### Step 2: Retrieve API Key
```python
from google.colab import userdata
api_key = userdata.get("Gemini_API_Key")
```
Retrieves the Gemini API key securely from Google Colab Secrets.

### Step 3: Initialize Gemini Client
```python
from google import genai
client = genai.Client(api_key=api_key)
```
Creates a Gemini client using the API key to establish a connection with the AI service.

### Step 4: Send Prompt to Gemini
```python
response = client.models.generate_content(
    model="gemini-3.5-flash",
    contents="What is Artificial intelligence? Explain in simple words."
)
```
Sends a question to the Gemini model and receives an AI-generated response.

### Step 5: Display Generated Response
```python
print("\nLLM Response:")
print(response.text)
```
Displays the generated answer in the output section.

## 5. Requirements
- Python
- Google Colab
- Google Gen AI SDK
- Gemini API Key
- Internet connection

## 6. How to Execute
1. Open the notebook in Google Colab.
2. Install the Google Gen AI SDK.
3. Add your Gemini API key in Colab Secrets using the name `Gemini_API_Key`.
4. Run all the notebook cells in sequence.
5. View the generated AI response in the output section.

## 7. Learning Outcomes
- Understand how Large Language Models work.
- Learn to connect Python with Gemini AI.
- Understand API key authentication.
- Learn how to send prompts to an AI model.
- Generate and display responses using Generative AI.

## 8. Conclusion
This practical demonstrates the integration of Google's Gemini Large Language Model with Python. It provides hands-on experience with API authentication, client initialization, prompt submission, and AI-generated response handling.


## 9. Program Outputs and Explanation

The notebook produces three important outputs during execution.

### Output 1: Gemini API Key Verification

**Code purpose:** Retrieves the Gemini API key from Google Colab Secrets.

**Output:**
```text
Gemini API Key loaded sucessfully.
```

**Explanation:** This message confirms that the Gemini API key was successfully retrieved. If the key is missing, the program raises a `ValueError`.

### Output 2: Gemini Client Initialization

**Code purpose:** Initializes the Gemini client using the retrieved API key.

**Output:**
```text
Gemini client intiallized successfully.
```

**Explanation:** This message confirms that the Gemini client was successfully created and is ready to communicate with the Gemini AI service.

### Output 3: LLM Generated Response

**Code purpose:** Sends a prompt to the Gemini model asking it to explain Artificial Intelligence in simple words.

**Prompt:**
```text
What is Artificial intilligence? Explain in simple words.
```

**Output:**
```text
LLM Response:

Artificial Intelligence (AI) is when smart computers or
machines are built to think, learn, and make decisions
just like humans do.

The response also explains AI using a child-learning
analogy and gives everyday examples such as smartphones,
Netflix, YouTube, voice assistants, Google Maps, and chatbots.
```

**Explanation:** The Gemini model processes the given prompt and generates a human-readable response. The program displays the generated response using `response.text`.

### Overall Result

All three outputs demonstrate the successful execution of the notebook:

1. Gemini API key retrieved successfully.
2. Gemini client initialized successfully.
3. Gemini model generated and displayed an AI response.
