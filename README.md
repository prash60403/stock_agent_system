# 📊 Multi-Agent Stock Market Analysis System

## 🚀 Project Overview
This project is a **multi-agent stock market analysis system** where an Analyst Agent studies stock data and a Trader Agent makes trading decisions based on that analysis. The system uses a sequential workflow built with CrewAI and real-time stock data from yfinance.

---

## 🛠️ Features
- Real-time stock data fetching using yfinance  
- Multi-agent collaboration (Analyst + Trader)  
- Structured task-based workflow  
- Automated trading decision (Buy / Sell / Hold)  
- Clean modular architecture  

---

## ⚙️ Tech Stack
- Python  
- CrewAI (Multi-Agent Framework)  
- yfinance (Stock Data API)  
- LLM (for reasoning and decision-making)  

---

## 📌 Project Architecture

### 1. Stock Research Tool
- Fetches real-time stock data:
  - Current Price  
  - Price Change  
  - Percentage Change  
  - Currency  
- Acts as the data source for the Analyst Agent  

---

### 2. LLM Initialization
- Initializes a language model  
- Enables reasoning, analysis, and decision-making for agents  

---

### 3. Analyst Agent
- **Role:** Stock Market Analyst  
- **Goal:** Analyze stock performance and trends  
- **Backstory:** Experienced financial analyst  
- **Tools:** Stock research tool  
- **Responsibility:** Generate insights from stock data  

---

### 4. Analyst Task
- **Description:** Analyze stock using real-time data  
- **Expected Output:**  
  - Trend analysis  
  - Risk evaluation  
  - Recommendation  

---

### 5. Trader Agent
- **Role:** Stock Trader  
- **Goal:** Decide whether to Buy, Sell, or Hold  
- **Backstory:** Profit-focused trader  
- **Context:** Uses Analyst Agent output  

---

### 6. Trader Task
- **Description:** Make trading decision based on analysis  
- **Expected Output:**  
  - Final decision (Buy / Sell / Hold)  
  - Reasoning behind decision  

---

### 7. CrewAI Workflow
- Combines both agents and tasks  
- Executes sequentially:
  1. Analyst Agent performs analysis  
  2. Trader Agent makes decision  

---

### 8. Main Execution (`main.py`)
- Initializes CrewAI  
- Runs the workflow  
- Outputs:
  - Stock analysis  
  - Trading decision  

---

## 📈 Example Output

**Analysis:**  
The stock shows upward momentum with moderate volatility.  

**Decision:**  
Buy with caution for short-term gains.  

---

## ▶️ How to Run

```bash
# Clone the repository
git clone https://github.com/your-username/stock_agent_system.git

# Navigate to project
cd stock_agent_system

# Install dependencies
pip install -r requirements.txt

# Run the project
python main.py
