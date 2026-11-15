
# Financial Plan Intelligence

### Agentic AI for Integrated Personal Finance and Investment Planning

**Financial Plan Intelligence** is an agentic AI project designed to support informed financial decisions by connecting personal finance management, savings allocation, investment portfolio optimization, and forward-looking financial risk assessment within a unified analytical framework.

Rather than treating household budgeting and investment management as separate activities, the project integrates both dimensions to evaluate how income, expenses, savings, liquidity, and investment performance interact over time.

The objective is not to maximize investment returns in isolation, but to support financially sustainable decisions by balancing investment opportunities with liquidity requirements, exposure to risk, and the ability to withstand adverse financial conditions.

The system combines quantitative financial models, scenario simulations, and a multi-agent architecture to translate complex financial information into integrated, evidence-based assessments.

## Project Overview

The project addresses three interconnected dimensions of financial decision-making:

**1. Personal Finance Management**

Analyzes historical income and expenses to evaluate spending patterns, savings capacity, available liquidity, and the sustainability of personal financial conditions.

**2. Investment Portfolio Planning**

Selects and optimizes an equity investment portfolio using historical market data, risk-return analysis, diversification constraints, and probabilistic projections of future performance.

**3. Integrated Financial Planning**

Combines personal finance projections with investment scenarios to assess total financial wealth, liquidity requirements, potential funding shortfalls, and financial resilience under different future conditions.

The distinctive value of the project lies in the interaction between these components: investment decisions are evaluated in relation to personal financial needs, while financial planning incorporates the potential evolution and risks of invested savings.

## 1. Personal Finance Analysis

The Personal Finance component uses 12 months of historical financial transactions to establish an initial financial position.

The analysis includes:

- Historical income and expense analysis.
- Identification of recurring expenditure patterns.
- Assessment of savings capacity and accumulated savings.
- Initial allocation of available savings between liquidity and investments.
- Forward-looking cash-flow and liquidity projections.
- Evaluation of adverse financial conditions through stress testing.

The initial allocation divides accumulated savings into two components: 50% retained as personal liquidity and 50% allocated to investments.

Both components subsequently evolve according to their respective financial dynamics.

### Financial Stress Testing

The system evaluates five personal finance conditions:

1. Baseline financial conditions.
2. A 30% reduction in income.
3. An extraordinary expense of €10,000.
4. An extraordinary expense of €20,000.
5. A 15% increase in recurring expenses.

These conditions make it possible to examine how unexpected events or deteriorating financial circumstances affect future liquidity and financial sustainability.

## 2. Investment Portfolio Analysis and Optimization

The Investment component applies quantitative financial analysis to an initial universe of 50 equities belonging to the STOXX Europe 50 index.

Historical price series covering five years are used to construct a ranking and select 25 equities for the subsequent portfolio optimization process.

The analysis includes:

- Historical return and volatility calculations.
- Risk-return-based equity ranking.
- Selection of 25 equities from the initial investment universe.
- Portfolio construction and optimization.
- Monte Carlo evaluation of alternative portfolio allocations.
- Diversification constraints, including a maximum of four equities per sector.
- Historical bootstrap simulations to estimate potential future portfolio outcomes.

The portfolio optimization evaluates 5,000 candidate allocations.

The subsequent investment risk analysis uses 1,000 simulated trajectories to assess possible portfolio developments over a 24-month horizon.

### Investment Risk Scenarios

Portfolio outcomes are represented through three probabilistic scenarios:

- **Unfavorable market (P5):** downside portfolio outcome.
- **Central market (P50):** median portfolio outcome.
- **Favorable market (P95):** upside portfolio outcome.

These scenarios provide a framework for evaluating investment uncertainty rather than relying on a single deterministic forecast.

## 3. Integrated Financial Planning and Resilience

The integrated financial assessment combines five personal finance conditions with three investment scenarios, producing **15 financial scenario combinations**.

Each combination is evaluated across a rolling time horizon of 1 to 24 months.

The analysis connects:

- Future income and expenditure.
- Personal liquidity evolution.
- Investment portfolio performance.
- Total financial wealth.
- Potential liquidity deficits and funding requirements.
- Financial sustainability under adverse conditions.

This integrated approach makes it possible to assess whether available financial resources remain sufficient when personal financial shocks and unfavorable market developments occur simultaneously.

It also supports the identification of situations in which investment capital may need to be considered in relation to personal liquidity requirements.

The resulting assessments provide a more comprehensive perspective than analyzing savings, investment returns, or household expenses independently.

## 4. Agentic AI Architecture

Financial Plan Intelligence incorporates a multi-agent architecture designed to coordinate personal finance analysis, investment risk evaluation, and integrated financial assessments.

The architecture includes specialized analytical and orchestration components:

**Financial Orchestrator**

Coordinates the analytical workflow and directs financial questions toward the relevant components.

**Personal Finance Agent**

Interprets personal finance conditions, liquidity projections, and the effects of financial shocks.

**Investment Risk Agent**

Analyzes investment portfolio outcomes and the implications of alternative market scenarios.

**Financial Assessment Agent**

Integrates personal finance and investment risk information to evaluate financial resilience and sustainability.

**Response Generation Agent**

Interprets natural-language questions and generates contextualized financial explanations based on the integrated analysis.

The response generation process supports flexible monthly horizons from 1 to 24 months and different combinations of financial conditions and investment scenarios.

### Analytical Workflow

1. Historical personal finance and market data are processed.
2. Personal financial conditions and savings capacity are assessed.
3. Investment securities are selected and portfolio weights are optimized.
4. Future portfolio outcomes are estimated through quantitative simulations.
5. Personal finance stress tests and investment scenarios are integrated.
6. Specialized agents interpret the requested financial conditions and time horizon.
7. The system generates evidence-based financial assessments.

## 5. Methodology

The project combines deterministic financial planning, quantitative investment analysis, probabilistic risk estimation, and agentic interpretation.

### Personal Finance Methodology

Historical financial transactions establish the initial position, while projected income, expenses, and liquidity movements provide a basis for evaluating future financial conditions.

Stress testing introduces alternative assumptions to examine the consequences of adverse financial events.

### Investment Methodology

Historical equity data support security selection and portfolio optimization.

Monte Carlo optimization evaluates alternative portfolio allocations, while historical bootstrap simulations estimate the distribution of potential investment outcomes.

### Integrated Assessment Methodology

Personal finance trajectories and portfolio scenarios are combined over corresponding time horizons.

The integrated assessment examines liquidity, investment capital, total financial wealth, and possible funding requirements across the 15 scenario combinations.

### Agentic Interpretation

The multi-agent layer connects the analytical results to natural-language financial questions, allowing users to explore alternative conditions, compare outcomes, and understand the implications of financial decisions.

## 6. Technologies

The project uses:

- **Python** for financial analysis and quantitative modeling.
- **Pandas and NumPy** for data processing and numerical calculations.
- **Monte Carlo simulation** for portfolio optimization.
- **Historical bootstrap simulation** for investment risk projections.
- **LangGraph** for multi-agent orchestration.
- **Generative AI** for financial interpretation and contextualized response generation.
- **Jupyter Notebook** for implementation, documentation, and reproducibility.

## 7. Project Files

**Main Notebook**

[Financial_Plan_Intelligence.ipynb](Financial_Plan_Intelligence.ipynb)

Contains the financial analysis, quantitative models, scenario simulations, agentic architecture, and project demonstrations.

**Data**

The `data/` directory contains the financial transaction dataset used in the Personal Finance analysis.

**Repository**

[Financial Plan Intelligence — GitHub](https://github.com/Valeria-Raele/financial-plan-intelligence)

## 8. Project Scope

Financial Plan Intelligence is a research and development project demonstrating how quantitative financial analysis and agentic AI can be combined to support integrated financial planning.

Its primary contribution is the connection between personal financial management and investment planning within a coherent decision-support framework.

The project demonstrates how financial decisions can be evaluated not only in terms of expected investment performance, but also in relation to future liquidity, financial vulnerability, and the sustainability of personal financial resources.

It is intended as an analytical and decision-support framework, not as a personalized investment advisory service or a guarantee of future financial outcomes.
