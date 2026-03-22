
# 📊 Financial Research Agent (CrewAI)
**Multi-Agent AI System for Automated Company Research & Analysis**

---

## 📌 Overview

This project implements a **multi-agent financial research system** that automates:

- Company-level **data collection from web sources**
- Structured **research synthesis**
- Professional **analyst-style reporting**

The system separates responsibilities between **research and analysis**, mimicking how real financial teams operate.

---

## 🧠 Architecture

```mermaid
flowchart TD
    A[User Input: Company] --> B[Researcher Agent]

    B --> C[Raw Research Data]

    C --> D[Analyst Agent]
    D --> E[Structured Financial Report]

    subgraph Workflow
        B
        D
    end
````

---

## ⚙️ How It Works

### 1. Researcher Agent

* Performs deep research on a company using web search
* Focus areas:

  * Company health
  * Historical performance
  * News & events
  * Opportunities & risks

📄 Defined in: 

---

### 2. Analyst Agent

* Transforms research into a **structured report**
* Adds:

  * Executive summary
  * Trend analysis
  * Market insights
  * Future outlook

📄 Defined in: 

---

## 🔄 Task Pipeline

The system follows a **sequential pipeline**:

1. **Research Task**

   * Collects structured company data
2. **Analysis Task**

   * Converts research into a professional report

📄 Task definitions: 

---

## 🏗️ Orchestration

* Managed using CrewAI
* Sequential execution ensures:

  * Research is completed before analysis
* Output is saved automatically

📄 Implementation: 

---

## 🛠️ Tech Stack

* Python
* CrewAI
* OpenAI / Groq / DeepSeek LLMs
* Serper API (web search)
* Pydantic
* YAML-based configuration

---

## 📂 Project Structure

```bash
financial-research-agent/
│
├── src/financial_researcher/
│   ├── crew.py              # Agent orchestration
│   ├── main.py              # Entry point
│   └── config/
│       ├── agents.yaml      # Agent definitions
│       └── tasks.yaml       # Task pipeline
│
├── output/
│   └── report.md            # Generated report
│
├── README.md
```

---

## ▶️ Setup & Run

### 1. Install dependencies

```bash
pip install uv
crewai install
```

---

### 2. Configure environment variables

Create `.env` file:

```env
OPENAI_API_KEY=your_key
SERPER_API_KEY=your_key
```

---

### 3. Run the system

```bash
crewai run
```

---

## 📊 Example Use Case

**Input**

```text
Company: Apple
```

**Output**

* Comprehensive research summary
* Structured financial report
* Executive-level insights
* Saved to: `output/report.md`

---

## 🧩 Key Features

* Multi-agent system (Research + Analysis separation)
* Web-enabled real-time research
* Structured report generation
* Modular YAML-based configuration
* Clean pipeline for extensibility

---

## 🔮 Future Improvements

* Add valuation models (DCF, ratios)
* Integrate real-time financial APIs
* Add comparison across multiple companies
* Build dashboard UI (Streamlit)
* Add memory for historical tracking

---

## ⚠️ Note

This project is based on a CrewAI template and has been extended with:

* Structured research pipeline
* Multi-agent separation of concerns
* Production-style output generation

---

## ⭐ Summary

This project demonstrates:

* Multi-agent AI system design
* Automated research workflows
* LLM orchestration for structured outputs
* Scalable and modular architecture

- Or write **resume bullets that actually get shortlisted**
```
