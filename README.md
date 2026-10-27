# The AI Minister: Ethical and Engineering Implications of Automating the Ministry of Territory and Housing

> What happens when a Random Forest with confidence *p* > 0.95 issues an eviction order? When a multi-objective optimizer decides between 5,000 homes now and 2,000 carbon-neutral homes later? This project analyses, from a data engineering perspective, the limits of automating a public administration.

Academic project for **TAED1** (Technology, Ethics and Data), Bachelor's Degree in Data Science and Engineering, **Universitat Politècnica de Catalunya (UPC)**, academic year 2025–26.

**Authors:** Ander Miranda, Pablo Fernández, Oriol Parent and Pau González.

> ⚠️ The "Conseller-IA" is a **hypothetical system** built for academic analysis. It is not endorsed by the Generalitat de Catalunya or by the UPC.

---

## 📌 Overview

The project imagines a "Conseller-IA": an AI system that manages the Catalan Ministry of Territory and Housing (urban planning, housing and mobility). Instead of asking *can it be done?*, it asks **where must the line be drawn?**

**Central thesis:** algorithmic governance is excellent at processing large volumes of structured data, but it perpetuates historical biases and cannot make moral exceptions in cases of extreme vulnerability. No metric (AUC, F1, NDCG) solves what the authors call the *moral exception problem*. The answer is a **human-in-the-loop** architecture, understood as an engineering requirement and not as a political preference.

## 🧱 What the project covers

### 1. Technical framework
The system is designed as a hybrid socio-technical system with four sub-systems, each with its own models and data:

| Sub-system | Main models | Example data |
|---|---|---|
| Territorial planning | Transformers (LLM), CNN, XGBoost | ICGC maps, IDESCAT indicators, cadastre |
| Urban planning & building control | Random Forest, GNN, BERT | Inspection records, POUM zoning, LiDAR |
| Housing allocation & emergencies | NSGA-II (Pareto front), Cox survival models | Housing applicants registry, CO₂ factors |
| Mobility & licensing | Reinforcement Learning, multi-agent systems | Traffic IoT sensors, public transport data |

Data sovereignty is a prerequisite: sensitive data stays on the Generalitat's own infrastructure (GDPR Art. 44–49, EU AI Act Annex III).

### 2. Materiality as an ethical variable
The environmental cost of the AI itself is quantified:

- **~3,600 MWh/year** of energy consumption.
- **2.9–4.3 million litres of water per year** for cooling (WUE 0.8–1.2 L/kWh), a real constraint in a territory with drought protocols.
- **Carbon footprint** (using the Catalan electricity mix, 0.283 kg CO₂eq/kWh): about 1.01 million kg CO₂eq for the initial deployment and about 1.30 million kg CO₂eq per year of operation.
- Hardware lifecycle and geopolitical dependencies (cobalt, lithium, rare earths), with procurement conditions.

### 3. Explicability and accountability
Explainability methods per sub-system (SHAP, GNNExplainer, Pareto-front visualisation, saliency maps), the *Problem of Many Hands*, and accountability tools: Model Cards, Data Statements, Algorithmic Impact Assessments and an audit log.

### 4. Delegation matrix
A three-tier taxonomy of what can be automated:

1. **AI as decision-maker:** only for reversible logistics with no impact on individual rights.
2. **AI as assistant:** urbanism and housing; the AI detects and proposes, the human decides.
3. **Human-only decision:** anything that changes a person's legal status (evictions, demolitions, refusals).

### 5. Ethical framework
Four lenses (teleological, deontological, virtue ethics, care ethics), Begoña Román's ten ethical values applied as a conflict/mitigation matrix, and a micro / meso / macro impact hierarchy. Philosophical references include Aristotle (*phronesis*), Kant, Rawls, Jonas, Tronto, Véliz, the Frankfurt School, Leopold, Næss, Bentham and Mill.

### 6. Empirical validation
A blinded survey where respondents solved 10 urban, social and environmental dilemmas acting as the "Conseller-IA". Each answer corresponded to one of four stakeholder archetypes (ecological, economic, social, property rights). Key finding: **social protection dominates in acute emergencies and ecological prevention dominates against catastrophic future risk**, so the system cannot rely on a single static objective function.

### 7. Case studies

| Case | Dilemma | Proposed engineering response |
|---|---|---|
| **1.1 The uninhabitable premises** | Formal justice vs. material justice (Decree 141/2012) | Hard rule at the decision layer: no eviction if a vulnerability flag is active and there is no confirmed alternative housing |
| **1.2 The irregular community centre** | Universal rules vs. community capital and the interest of the minor | 30-day suspension and notification to Social Services; the algorithm reports, a human decides |
| **1.3 The green corridor** | Intergenerational responsibility vs. present displacement | Publish the full objective space and halt; the weighting is a democratic decision |
| **2 Emergency housing** | Housing First (5,000 units) vs. Sustainability First (2,000 units) | Present the full Pareto front and delegate the choice of weights to an accountable human body |
| **3 Biomass plant** | Landscape protection vs. aggregate utility | The system flags the conflict; exceptions are human, documented decisions |

### 8. Regulatory guidelines
Four proposals: transparency and democratic validation, system control and fallback mechanisms (72-hour delay, kill-switch), protection of human dignity, and material and environmental governance.

---

## 📁 Repository contents

| File | Description |
|---|---|
| `Html.html` | Interactive academic web platform (in Catalan) that presents the whole project: theory, case studies, charts and references |
| Article (PDF) | The full paper, *The AI Minister: Ethical and Engineering Implications of Automating the Ministry of Territory and Housing* (in English, IEEE-style format) |
| Presentation (PDF) | Slides summarising the main arguments (in Catalan) |

## 🚀 How to view the project

Open `Html.html` in a modern browser. An internet connection is needed because the page loads fonts, Chart.js and D3 from CDNs, and some images from external hosts.

## 🛠️ Technologies

HTML, CSS and vanilla JavaScript, [Chart.js](https://www.chartjs.org/) (charts) and [D3.js](https://d3js.org/) (radar chart).

## 🤖 Use of AI tools

- **Google Gemini:** research support, concept clarification and language improvement of the article.
- **Anthropic Claude:** web design and front-end programming of the platform.

The authors reviewed all content and take full responsibility for it. The theses, arguments and case analyses are human-authored.

## 📚 Key references

Begoña Román (ethical values framework), Virginia Eubanks (*Automating Inequality*), Carissa Véliz (*Privacy is Power*), Hans Jonas (*The Imperative of Responsibility*), Joan Tronto (*Moral Boundaries*), John Rawls (*A Theory of Justice*), Deb et al. (NSGA-II), Lundberg & Lee (SHAP), EU AI Act (Regulation 2024/1689) and GDPR.

---

*Universitat Politècnica de Catalunya · Barcelona · 2025–26*
