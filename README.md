# Financial Plan Intelligence

## From Financial Data to Informed Decisions

### An Agentic AI Framework for Personal Finance, Portfolio Optimization & Integrated Risk Analysis

## Overview

Financial Plan Intelligence is an **agentic AI-powered analytical platform** designed to support personal financial management, investment planning, and forward-looking financial decisions within a unified framework.

The project originates from a fundamental principle: **effective personal financial management requires a comprehensive approach**, combining the monitoring of income and expenses, control of cash flows, identification of potential financial risks, and corrective actions to maintain liquidity and financial resilience. Equally important is the effective management of financial surpluses, ensuring that accumulated savings are not left idle but are strategically allocated to investments, taking into account liquidity needs, risk exposure, and long-term financial objectives.

The integrated analysis **builds on a 12-month monitoring period of personal income and expenses to assess cash flows and savings capacity, providing the basis for a balanced and prudent allocation of accumulated savings into an optimized investment portfolio with defensive characteristics**. The integration of personal financial planning and portfolio management brings together projections of personal finances, including potential financial shocks, with simulated portfolio performance to assess the evolution of liquidity and investments under different financial and market conditions. Specifically, it combines **five personal financial scenarios** (baseline conditions, a prolonged reduction in employment income, extraordinary expenses, and increased recurring expenses) with **three investment market scenarios** (unfavorable, central, and favorable). These market scenarios are intended as **illustrative proxies for potential portfolio gains and losses**, providing a broader perspective on how investment performance could interact with personal cash flows, liquidity needs, and potential financial shocks. They are estimated using **historical bootstrap simulations**, which resample observed stock returns to capture historical market fluctuations, volatility, and extreme movements. The purpose is to incorporate potential investment outcomes into the broader financial assessment, allowing personal budgeting, financial resilience, and investment risk to be evaluated together. The resulting **integrated combinations**, evaluated over rolling horizons from 1 to 24 months, allow the joint assessment of liquidity resilience, investment performance, and overall financial sustainability under alternative future conditions.

In conclusion, the platform goes beyond monitoring financial performance. It aims to **transform financial data into actionable insights**, enabling users to understand their current financial position, **identify recurring expenses** and opportunities for improvement, **allocate savings more efficiently**, and evaluate the **sustainability of financial decisions** under alternative future conditions.

---

## Key Features

Financial Plan Intelligence integrates three complementary analytical capabilities within a single decision-support framework.

### Personal Finance Intelligence

- Analysis of 12 months of historical household financial transactions.
- Classification and assessment of income and expenditure.
- Monthly cash-flow analysis and identification of financial imbalances.
- Evaluation of savings capacity and available liquidity.
- Identification of recurring expenses and potential financial vulnerabilities.
- Financial resilience analysis under adverse household conditions.
- Forward-looking liquidity projections over customizable monthly horizons.

### Investment Intelligence

- Quantitative analysis of 50 equities belonging to the STOXX Europe 50 universe.
- Risk-return ranking and selection of 25 securities.
- Statistical analysis of historical return distributions.
- Portfolio optimization using Monte Carlo simulations.
- Maximum Sharpe Ratio portfolio selection with diversification constraints.
- Historical bootstrap simulations of potential future investment outcomes.
- Assessment of unfavorable, central, and favorable market scenarios.

### Integrated Financial Decision Support

- Combined assessment of personal finance and investment performance.
- Initial allocation of positive accumulated savings between liquidity and investments.
- Five household financial scenarios and three investment market scenarios.
- Fifteen integrated financial scenario combinations.
- Rolling financial projections from 1 to 24 months.
- Assessment of financial sustainability, liquidity resilience, and potential funding gaps.
- Natural-language interaction through specialized AI agents.

---

## Financial & Investment Methodology

### 1. Personal Finance Analysis

The analysis begins with 12 months of historical financial transactions, covering household income, expenses, and cash flows.

This initial observation period establishes the financial baseline and provides the information required to evaluate savings capacity, spending patterns, and financial stability.

The framework then examines how available financial resources may evolve under alternative household conditions, including income reductions, extraordinary expenses, and increased recurring expenditure.

### 2. Investment Selection & Portfolio Optimization

The investment methodology follows a **structured, sequential process**, in which each analytical stage informs subsequent modelling decisions.

**I. Historical market data analysis**

Five years of daily price and return series are analyzed for 50 equities belonging to the STOXX Europe 50 universe.

**II. Risk-return assessment and selection**

Annualized returns and volatility are calculated, followed by a combined ranking assigning equal weight to both measures to select the top 25 securities.

**III. Return distribution analysis**

The Jarque-Bera normality test and excess kurtosis analysis identify non-normal return distributions with heavy tails, indicating the presence of extreme market movements.

These findings motivate the use of historical bootstrap simulations to better capture the distinctive risk characteristics of individual stocks.

**IV. Portfolio construction and optimization**

Covariance analysis and Monte Carlo simulation of **5,000 candidate portfolios** are used to select the maximum Sharpe Ratio portfolio, subject to diversification constraints, including a maximum of four securities per sector.

**V. Historical bootstrap simulation**

Non-parametric resampling of observed returns over the preceding five years generates **1,000 potential portfolio trajectories over the subsequent 24 months**.

The methodology incorporates historical peaks, downturns, and extreme fluctuations while preserving contemporaneous cross-asset relationships.

**VI. Forward-looking scenario analysis**

Three potential portfolio outcomes are calculated from the simulated performance distribution:

| Market scenario | Percentile | Interpretation |
|---|---|---|
| Unfavorable | P5 | Downside portfolio outcome |
| Central | P50 | Median portfolio outcome |
| Favorable | P95 | Upside portfolio outcome |

These scenarios represent possible investment outcomes, not guaranteed future performance.

### 3. Integrated Financial Assessment

Following the initial 12-month observation period, **50% of accumulated positive net savings is invested and 50% retained as liquidity**.

Over the subsequent 24 months:

- Personal liquidity evolves according to household cash flows and financial shocks.
- Investment capital follows simulated market performance.
- The combined evolution is assessed to identify financial vulnerabilities and potential funding requirements.

Five personal finance scenarios are considered:

| Scenario | Financial condition |
|---|---|
| Baseline | Historical household financial conditions |
| Income reduction | 30% reduction in employment income |
| Extraordinary expense 1 | €10,000 unexpected expenditure |
| Extraordinary expense 2 | €20,000 unexpected expenditure |
| Recurring expenses | 15% increase in recurring expenditure |

Each financial condition is combined with the three investment scenarios, generating **15 integrated combinations**.

The system evaluates these combinations over rolling horizons from 1 to 24 months, supporting comparisons between alternative financial and market conditions.

### From Analysis to Financial Decisions

The integrated framework helps address practical questions such as:

- *How much of my accumulated savings can I allocate to investments while maintaining adequate liquidity?*
- *What happens to my financial position if my income falls for an extended period?*
- *Can I cover an unexpected expense without compromising my investment strategy or having to sell assets?*
- *How would unfavorable market performance affect my overall financial position under a simultaneous household financial shock?*
- *What additional funding might be required to maintain financial sustainability?*

Through this integrated quantitative approach, Financial Plan Intelligence **translates financial analysis into practical decision support**, helping users understand the potential consequences of their choices before making them.

---

## Agentic AI Architecture

Financial Plan Intelligence is developed in Python using a **modular, tool-based architecture orchestrated through LangGraph**.

The system separates quantitative calculations from agentic reasoning, allowing specialized components to execute financial analyses based on user-defined parameters and time horizons.

### Main Components

| Component | Responsibility |
|---|---|
| Financial Orchestrator | Interprets requests, manages analytical parameters, and coordinates specialized tools and agents |
| Personal Finance Agent | Processes household financial information, cash flows, savings, and liquidity conditions |
| Investment Risk Agent | Evaluates portfolio risk, simulated performance, and alternative market scenarios |
| Financial Assessment Agent | Integrates personal finance and investment outcomes into comprehensive financial assessments |
| Shared Analytical State | Maintains the information required for coordinated analysis and response generation |

### Analytical Workflow

```text
Natural-language financial question
                 |
                 v
        Financial Orchestrator
                 |
       +---------+---------+
       |                   |
       v                   v
Personal Finance      Investment Risk
     Agent                 Agent
       |                   |
       +---------+---------+
                 |
                 v
       Financial Assessment
              Agent
                 |
                 v
     Integrated financial analysis
                 |
                 v
     Evidence-based explanation
```

The multi-agent architecture supports questions involving individual analytical domains as well as requests requiring the integration of personal financial conditions, investment performance, and financial resilience.

---

## Technology Stack

The project combines financial modelling, statistical analysis, agentic AI, and interactive analytical visualization.

### Programming & Data Analysis

| Technology | Application |
|---|---|
| Python | Core development and financial modelling |
| Pandas | Financial transaction processing and time-series analysis |
| NumPy | Numerical calculations, arrays, and simulations |
| SciPy | Statistical analysis, including Jarque-Bera and kurtosis |
| yfinance | Historical equity market data retrieval |
| Math | Mathematical operations and numerical utilities |

### Quantitative Methods

- Annualized return and volatility calculations.
- Risk-return ranking.
- Covariance and portfolio risk analysis.
- Sharpe Ratio optimization.
- Monte Carlo portfolio simulations.
- Jarque-Bera normality testing.
- Excess kurtosis analysis.
- Historical bootstrap resampling.
- Percentile-based investment scenarios.
- Deterministic household financial stress testing.
- Rolling liquidity and investment projections.

### Agentic AI & Orchestration

| Library | Application |
|---|---|
| LangGraph | Multi-agent workflow orchestration and shared state |
| LangChain Core | Agent tools, prompts, messages, and runnable components |
| LangGraph MemorySaver | In-memory workflow checkpointing |

### Visualization & Interactive Demo

| Library | Application |
|---|---|
| Gradio | Interactive analytical interface and live demonstration |
| Matplotlib | Financial charts and statistical visualizations |
| Plotly | Interactive charts and financial data exploration |
| Seaborn | Statistical data visualization |
| IPython.display | Notebook visualizations and embedded outputs |

The implementation also uses Python standard libraries for date handling, data structures, text processing, and execution utilities.

---

## Repository Structure

The repository is organized around the main Jupyter Notebook and its supporting financial data.

```text
financial-plan-intelligence/
|
|-- Financial_Plan_Intelligence.ipynb
|
|-- data/
|   |-- personal_finance_transactions_12_months_Nov2025_Oct2026.csv
|
|-- README.md
```

### Main Notebook

**Financial_Plan_Intelligence.ipynb**

The principal project deliverable, containing the quantitative analyses, financial models, portfolio optimization methodology, agentic architecture, and interactive demonstrations.

The notebook documents the development process and integrates analytical outputs with explanations of the underlying methodology.

[Open the Jupyter Notebook](https://github.com/Valeria-Raele/financial-plan-intelligence/blob/main/Financial_Plan_Intelligence.ipynb)

### Financial Dataset

**data/personal_finance_transactions_12_months_Nov2025_Oct2026.csv**

Contains the 12-month personal finance transaction dataset used to establish the initial household financial position and support subsequent analysis.

### Market Data

Historical equity data are retrieved using yfinance and processed within the quantitative investment workflow.

---

## Getting Started

### Requirements

- Python 3
- Jupyter Notebook or Google Colab
- Internet access for retrieving historical market data
- The required Python libraries
- Access to the financial transaction dataset

### Installation

Clone the repository:

```bash
git clone https://github.com/Valeria-Raele/financial-plan-intelligence.git
cd financial-plan-intelligence
```

Install the principal dependencies:

```bash
pip install numpy pandas scipy yfinance matplotlib seaborn plotly gradio langgraph langchain-core
```

The installation command covers the principal third-party libraries identified in the notebook. Additional dependencies or environment configuration may be required depending on the selected execution environment and agent model configuration.

### Running the Notebook

1. Open `Financial_Plan_Intelligence.ipynb` in Jupyter Notebook or Google Colab.
2. Install the required dependencies.
3. Configure the data paths and any model-access credentials required by the execution environment.
4. Run the notebook cells in sequence.
5. Explore the quantitative analyses, financial projections, and interactive demonstration.

The notebook should be executed in the intended environment with its required data and external services available.

---

## Interactive Live Demo

### Explore Financial Plan Intelligence

The **main Jupyter Notebook includes an interactive Gradio demonstration** designed to make the project's analytical capabilities accessible through natural-language questions.

The demonstration allows users to interact with the underlying quantitative and agentic system rather than simply reviewing static financial results.

It covers four complementary areas:

**Personal Finance Analysis**

Explore historical income, expenses, cash flows, savings, and financial conditions.

**Investment Analysis**

Examine equity selection, portfolio optimization, investment risk, and potential portfolio outcomes.

**Financial Stability & Resilience**

Assess the impact of income reductions, unexpected expenses, and other financial shocks on household liquidity and financial sustainability.

**Integrated Financial Assessment**

Combine personal financial scenarios with alternative investment outcomes to examine their joint impact on liquidity, investments, and overall financial resilience.

Users can formulate their own questions, explore predefined examples, and specify analytical parameters, including rolling time horizons from 1 to 24 months.

The interactive demonstration is provided **within the notebook** and illustrates the implemented analytical capabilities. It is not presented as a separately deployed, production-ready financial application.

---

## Validation & Analytical Scope

The project includes analytical validation and testing of the quantitative and agentic components.

Validation covers:

- Historical financial data processing.
- Portfolio selection and optimization outputs.
- Investment scenario calculations.
- Personal finance stress testing.
- Rolling monthly projections.
- Integrated financial assessments.
- Agentic interpretation of financial questions.

The integrated testing framework examines combinations of household financial conditions, investment scenarios, and monthly time horizons.

The project is designed to demonstrate reproducible quantitative analysis and coherent integration between specialized analytical components.

---

## Limitations

The project is intended for analytical research and financial decision support.

Several methodological limitations should be considered:

**Historical data dependence**

Investment simulations rely on observed historical market returns. Historical bootstrap techniques preserve characteristics of the sample but cannot anticipate previously unobserved market conditions.

**Scenario uncertainty**

The unfavorable, central, and favorable market scenarios represent conditional simulated outcomes rather than predictions of actual future returns.

**Portfolio optimization**

The maximum Sharpe Ratio portfolio is selected according to the specified quantitative methodology and constraints. This does not guarantee future outperformance.

**Financial projections**

Household financial scenarios are based on defined assumptions and should not be interpreted as forecasts of actual future income, expenses, or financial needs.

**Analytical scope**

The project demonstrates a quantitative and agentic financial decision-support framework. It does not constitute personalized financial advice or a production-ready financial advisory service.

---

## Project Purpose

Financial Plan Intelligence demonstrates how **personal financial management, quantitative investment analysis, and agentic AI** can be combined within a coherent financial decision-support framework.

Its distinctive contribution lies in integrating household financial conditions and investment outcomes to assess how available resources can be allocated, managed, and preserved under alternative future scenarios.

The project reflects an end-to-end approach to financial product development, combining **product vision, financial methodology, quantitative modelling, agentic architecture, and analytical validation**.

**From financial data to informed decisions.**
