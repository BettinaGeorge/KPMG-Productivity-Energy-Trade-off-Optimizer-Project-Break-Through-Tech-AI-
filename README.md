# ⚡ KPMG Productivity–Energy Tradeoff Optimizer  
**AI Studio x KPMG | Break Through Tech Fall 2025**

> *Exploring how AI can balance productivity gains and energy efficiency for sustainable enterprise performance.*

---

## 🌍 Overview
This project was developed as part of **Break Through Tech’s AI Studio** in collaboration with **KPMG US (Trusted AI Team — Sustainability Pillar)**.  
Our goal was to build an intelligent optimizer that measures and balances the **trade-off between energy consumption and employee productivity** when using generative AI tools in the workplace.

---

## 🧠 Problem Statement
AI adoption has drastically increased productivity but also **amplified energy consumption**.  
Organizations need a data-driven approach to evaluate:
- How much productivity AI actually delivers per energy unit consumed  
- Whether energy performance can be optimized without reducing workflow efficiency  

> **Core Question:**  
> *Can we optimize the trade-off between energy usage and employee productivity using AI?*

---

## 🎯 Objectives
- **Optimize Efficiency:** Reduce unnecessary energy usage while maintaining current AI productivity levels.  
- **Quantify Workforce AI Use:** Assess which job roles and industries rely most on AI in daily workflows.  
- **Measure Productivity Value:** Estimate the time saved per worker through generative AI adoption.  

---

## 💼 Business Impact
- 💰 **Cut Costs & Boost Efficiency:** Balance energy performance with sustainability to lower operational expenses.  
- 🧩 **Establish Smarter Workflows:** Use AI insights to enhance collaboration and task management.  
- 🌱 **Scale Responsible AI:** Drive sustainable AI adoption aligned with ESG and corporate responsibility goals.

---

## 🧩 Data Pipeline
| Dataset | Source | Description | Size |
|----------|---------|-------------|------|
| **Claude AI Workplace Usage** | [Anthropic Research](https://arxiv.org/html/2503.04761v1#S3) | 2.8M Claude AI conversations analyzing work task distributions | 23 × 8 |
| **AI Energy & Carbon Footprint** | [How Hungry is AI? (arXiv)](https://arxiv.org/html/2505.09598v1#S4.SS3.SSS1) | Benchmark of energy consumption for 28 AI models | 29 × 6 |
| **AI Productivity (Time Saved)** | [Federal Reserve Report](https://www.stlouisfed.org/on-the-economy/2025/feb/impact-generative-ai-work-productivity) | Estimates average minutes saved per task using AI | 92,927 × 2 |

### 🧼 Data Preparation
- Cleaned and merged datasets; standardized energy units (Wh)  
- Removed outliers >300 Wh and imputed missing medium-tier values  
- Engineered new features: `energy_per_task`, `minutes_per_task`, `intensity_share`, `occ_weight`  

---

## 📊 Modeling & Optimization
### 🔹 Models Used
- **Linear Regression 1** → Predicts *energy consumption (Wh/hr)*  
- **Linear Regression 2** → Predicts *AI productivity (minutes saved)*  
- **NSGA-II Multi-Objective Algorithm** → Optimizes *Pareto frontier* between energy efficiency and productivity  

### 🧮 Methodology
1. Normalized AI model & occupation data  
2. Calculated weighted task distributions across 1,000+ simulated work tasks  
3. Trained dual regression models for energy and productivity prediction  
4. Applied **NSGA-II** to generate Pareto-optimal trade-off curve  

---

## 🧾 Results
- Identified **optimal balance points** where productivity gain and energy efficiency intersect.  
- Achieved **>75% productivity prediction accuracy** and **energy cost modeling within 25% margin**.  
- Claude AI identified as a **top eco-efficient model** under medium computational load.  

---

## 🚀 Future Directions
- Integrate Bayesian Linear Regression with MCMC for more robust uncertainty modeling  
- Expand datasets to include real-time enterprise AI workloads  
- Visualize Pareto front dynamically with interactive dashboards  

---

## 🧰 Tech Stack
- **Languages:** Python (Pandas, NumPy, Matplotlib, Scikit-learn)  
- **Optimization:** NSGA-II (via DEAP), Linear Regression  
- **Visualization:** Plotly, Seaborn  
- **Documentation:** Jupyter, Markdown, Google Colab  

---

## 👥 Team
**Bettina George** – University of North Carolina at Chapel Hill  
**Ryan Vaseem** – Stevens Institute of Technology  
**Kimberly Hernandez** – University of Maryland  
**Jasper Li** – Williams College  
**Diana**, **Shreya**, **Ei Pai** – Collaborators  

Mentored by **Dr. Uohna June Thiessen** (AI Studio Coach)  
and **KPMG Advisors**: Kathi Ray, Sharad Nagariya, Ryan Tuggle, Nainika Narayanan, Brooke Bernstein  

---

## 🏁 Timeline
| Phase | Duration | Focus |
|--------|-----------|--------|
| **Project Planning** | August | Define hypothesis & project scope |
| **Data Collection & EDA** | September | Clean, merge, visualize trends |
| **Model Development** | October–November | Train regression models & NSGA-II |
| **Final Presentation** | December | Visualizations & GitHub release |

---

## 📫 Contact
**Bettina George**  
📍 UNC Chapel Hill | Computer & Information Science  
🔗 [LinkedIn](https://www.linkedin.com/in/bettinageorge) • [GitHub](https://github.com/bettinageorge)
