# 🚢 AutoClearance: AI-Powered Logistics Compliance Team

![Python](https://img.shields.io/badge/Python-3.10%2B-blue)
![CrewAI](https://img.shields.io/badge/Framework-CrewAI-orange)
![Status](https://img.shields.io/badge/Status-Building%20in%20Public-green)

> **From "Manual Entry" to "AI Automation".**
> A Multi-Agent System designed to streamline cross-border customs clearance data processing.

---

## 📖 The Backstory 

**"Why does it take 30 minutes to process one invoice?"**

During my time as a **Logistics Data Analyst Intern** at *Shenzhen Qianhai Wanbang Supply Chain*, I analyzed the daily workflow of customs brokers. I discovered a critical bottleneck:

* **70% of operational time** was wasted on manual data entry from non-standardized invoices (PDF/Images/Excel).
* **Human Error:** Fatigue led to typos in HS Codes and weight discrepancies (e.g., Gross Weight < Net Weight), causing compliance risks.

Combining my academic background in **Economics & Statistics (UCSC)** with my industry insights, I built **AutoClearance**: a virtual team of AI agents to solve this data mess.

---

## 🤖 How It Works 

I utilize **CrewAI** to orchestrate a team of autonomous agents, simulating a real-world "Compliance Department":

### The Agent Crew
1.  **📄 The Ingest Agent (Data Cleaning):**
    * **Role:** Extracts structured data (Description, Qty, Price) from messy raw text/files using LLM capabilities.
    * **Task:** Standardizes unit measurements and corrects OCR typos (e.g., "plstic" -> "Plastic").
2.  **🔍 The Auditor Agent (Stat & Logic Check):**
    * **Role:** Applies statistical logic to ensure data integrity.
    * **Logic:** Verifies that `Total Value = Unit Price * Qty` and `Gross Weight > Net Weight`. It flags anomalies just like a senior broker would.
3.  **📦 The Delivery Agent (System Integration):**
    * **Role:** Formats the verified data into a standard **JSON/CSV** object, ready for import into ERP systems (e.g., CargoWise).

---

## 🛠️ Tech Stack 

* **Core Framework:** [CrewAI](https://github.com/joaomdmoura/crewAI) (Agent Orchestration)
* **Language:** Python 3.10+
* **LLM:** OpenAI GPT-4 (via API)
* **Tools:** Pandas (Data Analysis), LangChain

---

## 🚀 Getting Started 

### Prerequisites
* Python 3.10 or higher
* An OpenAI API Key

### Installation

1.  **Clone the repository**
    ```bash
    git clone [https://github.com/wenlujiao/AutoClearance.git](https://github.com/wenlujiao/AutoClearance.git)
    cd AutoClearance
    ```

2.  **Install dependencies**
    ```bash
    pip install crewai crewai-tools
    ```

3.  **Set up environment variables**
    * Create a `.env` file in the root directory.
    * Add your API key (**Important:** Do NOT upload this file to GitHub):
    ```text
    OPENAI_API_KEY=sk-your_key_here
    ```

4.  **Run the Agents**
    ```bash
    python main.py
    ```

---

## 📊 Roadmap 

I am building this project in public based on "Human-in-the-loop" principles.

* [x] **Phase 1:** Build the "Data Cleaning Agent" to standardize messy text.
* [ ] **Phase 2:** Integrate "Auditor Agent" for weight and value logic checks.
* [ ] **Phase 3:** Connect to an external HS Code lookup tool (RAG implementation).
* [ ] **Phase 4:** Build a Streamlit UI for drag-and-drop usage.

---

## 👤 About Me

**Wenlu Jiao**
* 🎓 **UCSC** Undergraduate in Economics & Statistics.
* 💼 Former **Logistics Data Analyst Intern** (Shenzhen Qianhai Wanbang).
* Passionate about leveraging AI agents to solve vertical industry problems.

[Connect on LinkedIn](https://www.linkedin.com/in/wenlu-jiao)

---

*This project is for educational and portfolio purposes.*
