# AI Model Picker

A mobile-friendly web tool that helps users choose the best AI model for their specific needs. 

## About
The **AI Model Picker** is a decision assistant designed for professionals, small teams, and non-technical users. Instead of guessing which model to use (GPT-4, Claude 3.5, Gemini, Llama 3, or others), users answer 7 simple questions about their task, budget, and complexity.

The app uses a weighted scoring system to recommend the top models and also provides a quick **tailored prompt** to get them started immediately.

## Features
* **Scoring Engine:** Ranks models based on task type, reasoning capability, speed, and cost.
* **Conflict Detection:** Warns users if their budget constraints conflict with their task complexity (e.g., "Complex reasoning" vs "Must be free").
* **Web-Native Awareness:** Considers if a user needs live data and prioritizes models with deep internet access.
* **Prompt Generator:** Automatically generates a ready-to-use prompt based on the user's skill level (Beginner text vs. Advanced JSON).
* **Zero Dependencies:** Built entirely in HTML, CSS, and JavaScript. No build steps, no frameworks, no backend required.

## Why This Tool is Unique
While there are many **AI Model Leaderboards** and **Developer Benchmarks** out there, **AI Model Picker** fills a specific gap for the everyday user:

| Feature | Typical Leaderboards | Enterprise Cost Tools | AI Model Picker (This Tool) |
| :--- | :--- | :--- | :--- |
| **Target Audience** | Developers & Engineers | CTOs & Finance Teams | **Individuals, Freelancers, Students** |
| **Primary Metric** | Python Code / Benchmarks | Cloud API Spend | **Personal Monthly Budget** |
| **Goal** | Technical Performance | Corporate Cost Cutting | **Avoiding "Subscription Fatigue"** |

**The Core Problem Solved:**
Most users blindly pay for multiple monthly subscriptions (ChatGPT Plus, Claude Pro, etc.) without realizing that a free or cheaper model might handle their specific workflow/ task (e.g., "summarizing PDFs") even better. This tool uses a weighted algorithm to find that "Goldilocks" model for your specific needs.

## The "Goldilocks" Engine: Why This Tool Exists

Most AI tools fall into two traps:
1.  **The "Enterprise Sales" Trap:** Tools like *Wonderchat* are designed to sell you a chatbot builder for your business. They don't inherently care about your personal wallet.
2.  **The "Developer Benchmark" Trap:** Leaderboards like **HuggingFace** rank models by abstract Python scores that don't mean much to an everyday user writing an email.

**AI Model Picker** is different. It is the **Consumer Advocate** for AI.

### Comparison: Us vs. The Rest

| Feature | Corporate Lead Magnets | Developer Leaderboards | AI Model Picker (This Tool) |
| :--- | :--- | :--- | :--- |
| **Primary Goal** | Sell you a B2B subscription | Rank raw computing power | **Save you money** |
| **Cost Awareness** | Ignored | Ignored | **Core Feature** (Checks if you overpay) |
| **Input Logic** | Basic (Text only) | N/A | **Deep** (PDFs, Code, Images, Web) |
| **Web Capability** | Rarely checks | N/A | **Distinguishes Online vs. Offline models** |
| **Target User** | CTOs & Support Managers | ML Engineers | **Freelancers, Students, & You** |

### Core Philosophy: Fighting "Subscription Fatigue"
We believe you shouldn't pay monthly subscriptions for ChatGPT Plus if a free model (like Gemini Flash or GPT-4o mini) can handle your specific workload. This simple tool calculates the "Minimum Viable Model" for your task to keep your monthly recurring costs at 0.

## Why Model Selection Still Matters

Even as AI systems improve rapidly, two realities make model selection an essential skill for everyday users:

### **1. AI models are becoming more different, not more similar**

Although base training datasets overlap, every major AI lab is now integrating different forms of *specialized*, *exclusive*, or *partnership-driven* data:

- Some models emphasize **reasoning and mathematics**. 
- Some excel in **creativity and storytelling**.
- Some prioritize **low latency or cost efficiency**. 
- Some integrate **live web data** more deeply.  
- Some optimize for **privacy and self-hosting**. 
- Some receive **proprietary data partnerships** (forums, social platforms, etc.).

Because of this, capabilities, hallucination patterns, styles, and strengths will continue to diverge.

Even if overall intelligence improves, **specialization and bias profiles will remain**, making it helpful to match the right model to the right task.

### **2. The modern AI skill is “model routing”**

A growing number of people are shifting from relying on a single AI model to distributing work across multiple models depending on strengths:

- One model for **fast ideation**  
- One for **complex reasoning**  
- One for **creative writing**  
- One for **web-connected research**  
- One for **code generation or debugging**  
- One for **private, local workflows**

This mindset treats AI not as a single assistant, but as a *team of coworkers* — each with different talents.
The benefit: you get better results while reducing unnecessary subscriptions fatigue.

### **Why this matters for this tool**

This project is built on the belief that:

- No single AI model will ever be the best at everything.  
- Model diversity (and specialization) is increasing, not shrinking.  
- Everyday users need simple, friendly guidance — *without* reading dozens of reviews or benchmark charts.  
- A lightweight, transparent decision helper can save money, time, and cognitive load.

## How to Run Locally
Running it is incredibly easy:

1.  **Clone the repository:**
    ```bash
    git clone [https://github.com/yourusername/ai-model-picker.git](https://github.com/yourusername/ai-model-picker.git)
    ```
2.  **Open the file:**
    Double-click `index.html` to open it in your web browser.

## Configuration
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
