# ICUB-Improvised-Christ-University-ChatBot
AI-powered chatbot for Christ University using GPT-4o-mini via OpenRouter API. Provides accurate, domain-specific answers on admissions, academics, hostels, placements, and more with prompt engineering, multi-turn memory, guided suggestions, and an interactive ipywidgets UI for enhanced user experience.
# ICUB Improvised Christ University ChatBot  (CUB)

# 🔷 1. WHAT THIS SYSTEM IS (ABSOLUTE BASICS)

This system is a:

> **Domain-restricted AI chatbot for Christ University, powered by a Large Language Model (LLM), accessed through an external API, and wrapped in an interactive UI built using Python widgets.**

It **does NOT store data**, **does NOT browse the web**, and **does NOT fine-tune models**.

It **CALLS an AI model through an API** and displays the response intelligently.

---

# 🔷 2. DOES THIS PROJECT USE AN API?

### ✅ YES — IT USES AN AI API

Specifically:

| Component | Used                    |
| --------- | ----------------------- |
| API       | **OpenRouter API**      |
| SDK       | **OpenAI Python SDK**   |
| Model     | **GPT-4o-mini**         |
| Call Type | **Chat Completion API** |

---

# 🔷 3. WHAT IS OPENROUTER & WHY IT IS USED

### 🔹 OpenRouter is:

* An **API gateway**
* Gives access to **multiple LLM providers**
* Acts as a **proxy** between your code and models like GPT-4

### 🔹 Why you used it:

* Cost-effective
* Easier access
* Model flexibility
* Same OpenAI-style API

```python
client = OpenAI(
    api_key=API_KEY,
    base_url="https://openrouter.ai/api/v1"
)
```

📌 This line connects your code to **external AI infrastructure**.

---

# 🔷 4. API KEY — WHAT IT DOES

```python
API_KEY = "sk-or-v1-...."
```

### This key:

* Authenticates your request
* Identifies your account
* Tracks usage
* Enables billing & limits

⚠️ **Security note**:
Hardcoding keys is unsafe. In real deployments, use environment variables.

---

# 🔷 5. WHICH AI MODEL IS USED & WHY

```python
model="openai/gpt-4o-mini"
```

### GPT-4o-mini:

* A **Large Language Model**
* Trained on massive text datasets
* Optimized for:

  * Speed
  * Cost
  * Reasoning
  * Instruction following

### What the model DOES:

* Understands natural language
* Reasons about questions
* Generates structured text

### What it DOES NOT do:

* Browse internet
* Access Christ database
* Fetch live data

---

# 🔷 6. TYPE OF AI USED (IMPORTANT FOR EXAMS)

| Aspect       | Classification                     |
| ------------ | ---------------------------------- |
| AI Type      | **Generative AI**                  |
| Model Class  | **LLM (Large Language Model)**     |
| Learning     | **Pre-trained (not trained here)** |
| Interaction  | **Conversational AI**              |
| Intelligence | **Single Agent (Reactive)**        |

---

# 🔷 7. DATA USED — EXPLAINED CLEARLY

### ❌ No dataset is trained

### ❌ No CSV / database used

### ✅ Data Sources Used:

## 1️⃣ SYSTEM PROMPT (CONTROL DATA)

```python
"You are a professional academic AI assistant..."
```

This **controls behavior**, not knowledge.

📌 This is **prompt engineering**, not training.

---

## 2️⃣ OFFICIAL LINKS (GROUNDING DATA)

```python
LINKS = {...}
```

Purpose:

* Anchor responses
* Reduce hallucination
* Increase trust

---

## 3️⃣ CHAT HISTORY (TEMPORARY MEMORY)

```python
chat_history = []
```

Stored only in:

* RAM
* Runtime session

Deleted when:

* Kernel restarts
* Notebook closes

---

## 4️⃣ SUGGESTION POOL (UX DATA)

Used only to:

* Guide user interaction
* Improve experience

---

# 🔷 8. HOW A QUESTION BECOMES AN ANSWER (FULL PIPELINE)

## 🔁 COMPLETE FLOW

```
User types question
      ↓
Input validation
      ↓
UI updates (thinking animation)
      ↓
Prompt construction
      ↓
API request sent
      ↓
LLM reasoning
      ↓
Text generation
      ↓
Response displayed
```

---

# 🔷 9. PROMPT ENGINEERING (VERY IMPORTANT)

### Messages sent to API:

```python
messages = [
  {"role": "system", "content": system_prompt},
  {"role": "user", "content": "..."},
  {"role": "assistant", "content": "..."},
]
```

### Roles Explained:

| Role      | Purpose                      |
| --------- | ---------------------------- |
| system    | Controls personality & rules |
| user      | Human input                  |
| assistant | Previous AI replies          |

📌 This is **context replay**, not memory storage.

---

# 🔷 10. PARAMETERS USED IN API CALL

```python
temperature=0.2
max_tokens=800
```

### What they do:

| Parameter   | Effect                  |
| ----------- | ----------------------- |
| temperature | Controls randomness     |
| low (0.2)   | Factual, stable answers |
| max_tokens  | Max length of response  |

---

# 🔷 11. DOES THIS USE AI AGENTS?

### ❌ NOT A MULTI-AGENT SYSTEM

There is:

* No planner agent
* No tool-calling agent
* No autonomous loop

### ✅ SINGLE AI AGENT

The LLM:

* Observes
* Thinks
* Responds

This is a **reactive agent architecture**.

---

# 🔷 12. WHY “THINKING ANIMATION” IS USED

```html
🎓 CUB is analyzing your question…
```

### Purpose:

* Improves UX
* Masks latency
* Mimics human reasoning

This is **perceived intelligence design**.

---

# 🔷 13. HOW OUTPUT IS DISPLAYED

Rendered using:

* Markdown
* HTML
* CSS

```python
display(Markdown(...))
```

Chat is:

* Re-rendered every turn
* Scroll auto-adjusted

---

# 🔷 14. LIMITATIONS (YOU MUST KNOW THIS)

| Limitation      | Reason              |
| --------------- | ------------------- |
| No live data    | No browsing         |
| No verification | Model-generated     |
| No storage      | Memory resets       |
| API cost        | Token-based billing |

---

# 🔷 15. SECURITY & ETHICS

### Good Practices Used:

* Disclaimer shown
* Domain restriction
* Low temperature
* Source links

### Needs Improvement:

* API key security
* Rate limiting
* Input sanitization

---

# 🔷 16.  AI REALLY USED?

### BEST ANSWER:

> “Yes, the system uses a Large Language Model accessed via an external API. The AI is not trained locally but is prompted using system instructions and contextual memory to generate accurate, domain-specific responses.”

---

# 🔷 17. FINAL ONE-LINE SUMMARY

> “This project is a domain-restricted conversational AI system that uses the OpenRouter API to access a GPT-4o-mini large language model, combined with prompt engineering, UI orchestration, and in-memory conversational context to deliver structured academic responses.”

From,

Neeraj Ashish Goli.
---


