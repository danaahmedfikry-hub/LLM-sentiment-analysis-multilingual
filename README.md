🧠 Multilingual Sentiment Analysis using Gemini LLM
📌 Overview

This project is an AI-powered sentiment analysis system that classifies text into Positive, Negative, or Neutral using Google Gemini. It also generates structured reasoning for classification in Arabic and provides a second deterministic output for validation.

The system demonstrates prompt engineering, multilingual reasoning, and dual-output LLM evaluation.

🚀 Features
Sentiment classification (Positive / Negative / Neutral)
Multilingual reasoning (Arabic explanations)
Dual-prompt strategy (reasoning + strict label output)
Temperature-controlled LLM responses
Batch processing of multiple texts
JSON export of results for analysis
🧠 Sentiment Logic

The model uses the following definitions:

Positive: Satisfaction, praise, approval, or enjoyment
Negative: Criticism, dissatisfaction, or disappointment
Neutral: Mixed, weak, or indifferent sentiment
⚙️ Model Strategy

The system uses two parallel LLM prompts:

1. Reasoning Prompt
Produces step-by-step explanation in Arabic
Helps interpret how the sentiment is derived
2. Reliable Prompt
Outputs only the final label
Uses temperature = 0 for deterministic results
🧰 Tech Stack
Python
Google Gemini (via LangChain)
dotenv
JSON handling
📂 Project Structure
sentiment-analysis-gemini/
│
├── main.py
├── .env
├── sentiment_results.json
└── README.md
▶️ How It Works
Load API key from environment variables
Initialize Gemini LLM
Send each review to the model using two prompts
Generate:
Arabic reasoning explanation
Final sentiment label
Store results in JSON file
💡 Example Inputs
"الموبايل ممتاز والبطارية بتقعد وقت طويل جدًا."
"الفيلم كان ممل وطويل زيادة عن اللزوم."
"عادي، مش وحش بس مش أحسن حاجة."
📤 Output Format

Each result contains:

{
  "text": "input review",
  "reasoning_output": "Arabic explanation from LLM",
  "reliable_output": "Positive / Negative / Neutral"
}
📌 Key Highlights
Prompt engineering for structured reasoning
Multilingual output control (Arabic reasoning constraint)
Dual-model output strategy for reliability comparison
Batch inference pipeline
JSON-based structured result storage
📈 Future Improvements
Add Streamlit UI for live sentiment analysis
Fine-tune prompts for better Arabic consistency
Add confidence scoring
Extend to multi-class emotion detection (anger, joy, etc.)
Support real-time streaming inputs
👩‍💻 Author

Dana Ahmed
Computer Science Graduate
AI Engineer focused on NLP, LLM systems, and intelligent text analysis systems
