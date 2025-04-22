# 🤖 Prompt Refining Chatbot

A Streamlit-based chatbot assistant that classifies, refines, and guides users through structured prompt suggestions for AI agents, especially targeting blockchain task modeling.

## 🧠 Features
- Interactive chat interface via `streamlit`.
- Uses LLM (LLaMA3-8B) to parse and refine natural language prompts.
- Converts user input into structured blockchain task JSON format.
- Dynamically adjusts UTC timestamps based on location.
- Single input field with confirmation flow.
- Outputs formatted JSON directly in the UI.

## 🚀 Getting Started

### 1. Clone the Repo
```bash
git clone https://github.com/plutus1234/assistant.git
cd assistant/timestamp
```

### 2. Install Requirements
```bash
pip install -r requirements.txt
```

### 3. Create `.env` File
```env
GROQ_API_KEY=your_groq_api_key_here
```

### 4. Run the App
```bash
streamlit run chatbot_prompt_refiner.py
```

## 📦 Requirements
```
streamlit
python-dotenv
requests
geopy
timezonefinder
pytz
```

## 📤 Output Format
Returns JSON in the following structure:
```json
{
  "agenda_specs": {"attributes": "..."},
  "cascade_schema": [
    {
      "type": "OPERATION_MATRIX",
      "contingency": "CERTAIN",
      "time": {
        "temporal_state": "FUTURE",
        "exec_time": 1714028400,
        "constraint": "EXACTLY",
        "timezone": "UTC"
      },
      "description": "Book a SUV ride from I-9/3 to F-8 on April 25, 2025 at 3:00 PM",
      "control_flow": [...],
      "fallback": {...}
    }
  ]
}


