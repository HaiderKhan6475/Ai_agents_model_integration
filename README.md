# Model Integration with LangChain

This notebook covers integrating multiple AI models using LangChain — Groq, Google Gemini, and OpenAI.

## What's Covered

### 1. Environment Setup
- Loading API keys securely using `python-dotenv`
- Setting up environment variables for Groq and Google Gemini

### 2. Groq Model Integration
- Using `init_chat_model()` with `llama-3.1-8b-instant`
- Sending basic prompts and getting responses

### 3. Google Gemini Model Integration
- Using `init_chat_model()` with `gemini-2.5-flash`
- Using `ChatGoogleGenerativeAI` directly with `gemini-2.5-flash-lite`

### 4. ChatGroq (Direct Integration)
- Using `ChatGroq` class from `langchain_groq`
- Running inference with `llama-3.1-8b-instant`

### 5. Streaming
- Streaming responses token by token using `model.stream()`
- Real-time output with `flush=True`

### 6. Batch Processing
- Sending multiple prompts at once using `model.batch()`
- Using `max_concurrency` for parallel requests

## Setup

1. Clone the repo and navigate to the folder
   ```
   git clone https://github.com/HaiderKhan6475/agenticai.git
   cd agenticai
   ```

2. Create and activate virtual environment
   ```
   python -m venv .venv
   .venv\Scripts\activate
   ```

3. Install dependencies
   ```
   pip install -r requirement.txt
   ```

4. Add your API keys
   ```
   cp .env.example .env
   ```
   Open `.env` and add your real API keys.

5. Open the notebook
   ```
   jupyter notebook model_integration.ipynb
   ```

## Requirements

```
langchain
langchain-groq
langchain-openai
langchain-google-genai
python-dotenv
```

## Models Used

| Provider | Model |
|----------|-------|
| Groq | llama-3.1-8b-instant |
| Google Gemini | gemini-2.5-flash / gemini-2.5-flash-lite |

## Key Concepts

- `model.invoke()` — Single prompt, single response
- `model.stream()` — Real-time streaming output
- `model.batch()` — Multiple prompts at once