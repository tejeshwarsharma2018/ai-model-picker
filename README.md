# AI Model Picker

A smart, mobile-friendly web tool that helps users choose the best AI model for their specific needs. 

[**Live Demo**](https://yourusername.github.io/model-picker) ## 🚀 About
The **AI Model Picker** is a single-file decision assistant designed for professionals, small teams, and non-technical users. Instead of guessing which model to use (GPT-4, Claude 3.5, Gemini, Llama 3, etc.), users answer 6 simple questions about their task, budget, and complexity.

The app uses a weighted scoring algorithm to recommend the top 2 models and provides a **tailored prompt** to get them started immediately.

## ✨ Features
* **Smart Scoring Engine:** Ranks models based on task type, reasoning capability, speed, and cost.
* **Conflict Detection:** Warns users if their budget constraints conflict with their task complexity (e.g., "Complex reasoning" vs "Must be free").
* **Web-Native Awareness:** Detects if a user needs live data and prioritizes models with internet access.
* **Prompt Generator:** Automatically generates a ready-to-use prompt based on the user's skill level (Beginner text vs. Advanced JSON).
* **Zero Dependencies:** Built entirely in vanilla HTML, CSS, and JavaScript. No build steps, no frameworks, no backend required.

## 🛠️ How to Run Locally
Since this project is a single file, running it is incredibly easy:

1.  **Clone the repository:**
    ```bash
    git clone [https://github.com/yourusername/ai-model-picker.git](https://github.com/yourusername/ai-model-picker.git)
    ```
2.  **Open the file:**
    Double-click `index.html` to open it in your web browser.

## ⚙️ Configuration
You can easily add new models or change scoring rules by editing the `index.html` file directly.

### Adding a New Model
Look for the `const MODELS` array in the JavaScript section:

```javascript
{
  id: "new-model-name",
  label: "New Model 1.0",
  tier: "free", // options: premium, low, free
  cost_desc: "Free Tier",
  trade_off: "Slower than paid models.",
  notes: "Great for writing.",
  capabilities: { 
      reasoning: 4, 
      speed: 3, 
      web_native: false, 
      multimodal: true, 
      coding: 3, 
      long_context: 4 
  },
  self_host: false
}
