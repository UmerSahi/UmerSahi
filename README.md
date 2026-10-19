<div align="center">

<picture>
  <source media="(prefers-color-scheme: dark)" srcset="assets/banner-dark.svg">
  <source media="(prefers-color-scheme: light)" srcset="assets/banner-light.svg">
  <img src="assets/banner-light.svg" alt="Umer Sahi, AI / ML engineer: computer vision, medical image analysis, trustworthy AI" width="100%">
</picture>

**I build AI systems that are evaluated honestly, explainable by design, and shipped end to end.**
<br>
Computer science graduate (ranked 1st in cohort, CGPA 3.76/4.00) working across computer vision, medical imaging and LLM agents.

[Portfolio](https://umer-sahi.vercel.app/) · [LinkedIn](https://www.linkedin.com/in/umer-sahi-b3bb19348/) · [Email](mailto:umersahi5p@gmail.com)

</div>

---

## About

I graduated with a B.S. in Computer Science from Khwaja Fareed University of Engineering & IT (2021 to 2025) as the gold medalist, ranked first in my cohort. My thesis, **Deep Spud**, took a transfer-learning classifier all the way to a deployed Flask API and Next.js frontend.

Since then I have focused on a question I find more interesting than raw accuracy: *can we trust what a model tells us, and can we show why?* My recent work pairs strong baselines and confidence intervals with explainability audits, safety evaluation and clear documentation of limitations.

I currently work as an AI / Data Science Intern at Netixsol, supporting ML workflows from data cleaning to model benchmarking. I am looking for research-based graduate positions and AI/ML engineering roles, and I am open to opportunities worldwide.

## Selected work

> Some of these projects are not yet in public repositories. Links appear only where a public repository exists, and every figure below is taken from my CV.

<table>
<tr>
<td width="50%" valign="top">

### Explainable Fracture Detection
**Medical imaging · Explainable AI**

Binary fracture classification on the FracAtlas radiograph dataset (4,085 images, 719 fractured). Fine-tuned ResNet-50 and DenseNet-121 with a stratified 70/15/15 split and a weighted loss for class imbalance.

- DenseNet-121 on the held-out test set (N = 583): AUROC **0.933**, AUPRC **0.852**, calibration error 0.044
- ResNet-50 AUROC **0.935**; both beat a frozen-feature logistic regression baseline (0.884)
- 95% bootstrap confidence intervals on every metric
- Grad-CAM with an automated saliency audit that flagged shortcut-learning risk (55.41% of activation mass in the image border), reported openly
- FastAPI backend with a heatmap viewer; documented as a research prototype with a model card

`PyTorch` `Grad-CAM` `FastAPI`

Code: not yet public

</td>
<td width="50%" valign="top">

### Multi-Agent AI Clinic Assistant
**Agentic systems · Safety and evaluation**

A multi-agent clinical assistant for a simulated outpatient clinic network (5 branches, 30 doctors, 520 synthetic patients) with bilingual Urdu and English intake. A human review gate sits on every recommendation, and all data is synthetic.

- LangGraph supervisor with 7 specialist agents and 4 MCP servers
- Two-tier triage: deterministic red flags plus an LLM urgency classifier, 100% emergency recall on 50 benchmark scenarios
- 65 test conversations across 9 categories; 14/14 red-team attacks defended with 0 leaked patient records
- Multimodal lab-report extraction at 99.4% parameter accuracy on 30 reports

`LangGraph` `MCP` `RAG` `Python`

Code: not yet public

</td>
</tr>
<tr>
<td width="50%" valign="top">

### RealEstate Hub: Voice and Chat Agent
**Full-stack AI · Interpretable ML**

A stateful, bilingual (English and Roman Urdu) LangGraph agent with 10 nodes covering search, booking, rescheduling, RAG, email and valuation, backed by a 750+ property knowledge base.

- LightGBM valuation model: R² **0.891**, MAPE 5.4% (5,778 listings)
- LightGBM lead scoring: ROC AUC **0.912** (3,496 leads)
- SHAP attributions translated into plain-language explanations of each price
- Real-time voice via Vapi and Deepgram, Google Calendar integration, invariants against double bookings and hallucinated listings
- Deployed with a React/Vite frontend and Docker on Render

`LangGraph` `LightGBM` `SHAP` `React`

Code: not yet public

</td>
<td width="50%" valign="top">

### AFL AI Assistant
**Sports analytics · Tool-using agent**

Netixsol internship capstone. A LangGraph assistant with explicit intent routing and Gemini-powered tool use over 7,904 matches and 217,568 player-game rows.

- 8 trained models; match-winner classifier at ROC AUC 0.71 and 66% accuracy against a 57 to 58% naive baseline
- 100% (34/34) router accuracy; 28/28 on the combined evaluation suite
- Prompt-injection guard blocking 6/6 tested styles
- Fixed a multi-turn bug where stale entities leaked into unrelated follow-ups

`LangGraph` `FastAPI` `scikit-learn` `pandas`

Code: not yet public

</td>
</tr>
<tr>
<td width="50%" valign="top">

### Deep Spud: Potato Disease Classification
**Undergraduate thesis · Computer vision**

InceptionV3 transfer learning for multi-class potato leaf disease classification, with augmentation for a limited dataset. **94%** test accuracy, evaluated with precision, recall and confusion matrices, and deployed through a Flask REST API with a Next.js frontend.

`TensorFlow` `Flask` `Next.js`

[Training notebooks](https://github.com/UmerSahi/potato-disease-Classification-notebook-only)

</td>
<td width="50%" valign="top">

### Brain Tumor MRI Classifier
**Medical imaging · Desktop app**

CNN classifier for glioma, meningioma, pituitary tumor and no tumor, with a Tkinter interface showing predicted class, confidence and per-class probabilities. For education and research only, not for diagnosis.

`TensorFlow` `Keras` `Tkinter`

[Repository](https://github.com/UmerSahi/Brain-Tumor-Detection-Desktop-App)

</td>
</tr>
</table>

**Also on GitHub:** [Laptop Price Predictor](https://github.com/UmerSahi/Laptop-Price-Predictor) (regression model behind a web interface) · [StoreFlow dashboard](https://github.com/UmerSahi/Admin_Dashboard_Frontend_typescript) (Next.js analytics) · [Crypto Price Watcher](https://github.com/UmerSahi/Cryptopricewatcher) (TypeScript) · [Netixsol internship work](https://github.com/UmerSahi/Netixsol)

## Research interests

I treat these as directions I am building toward, not as published expertise.

| Direction | Where it shows up in my work |
|---|---|
| Computer vision and medical image analysis | Fracture detection on radiographs; brain tumor MRI classification |
| Explainable and trustworthy AI | Grad-CAM saliency audit, model card, SHAP explanations |
| Safety evaluation of AI systems | Clinic assistant triage recall, red-team audit, prompt-injection guards |
| Multimodal and generative AI | Lab-report extraction, voice and chat agents, RAG |

## Engineering practice

- **Evaluate before claiming.** Held-out test sets, baselines, bootstrap confidence intervals and calibration, not a single accuracy number.
- **Report failure modes.** The saliency audit that exposed border-activation shortcuts is in the write-up, not hidden from it.
- **Ship the whole system.** Data processing, training, APIs, interfaces, containers and deployment.
- **Design for safety.** Deterministic guards next to LLM components, human review gates, and tested attack scenarios.

## Skills

| | |
|---|---|
| **Languages** | Python · JavaScript (ES6+) · TypeScript · SQL |
| **ML and vision** | PyTorch · TensorFlow · Keras · scikit-learn · OpenCV · LightGBM · SHAP · transfer learning |
| **LLMs and agents** | LangGraph · RAG · Model Context Protocol · LLM integration |
| **Backend and web** | FastAPI · Flask · Node.js · REST APIs · React · Next.js · Docker |
| **Data** | pandas · PostgreSQL (Supabase) · MySQL · ChromaDB |
| **Tools** | Git · Jupyter · Google Colab · Figma |

## Recognition

Gold Medalist, B.S. Computer Science (rank 1 in cohort) · Top Performer, HEC Pakistan Generative AI Training Program, Cohort 3 (2026) · IELTS Academic 7.5

## Contact

I am interested in research assistantships, graduate research positions and AI/ML engineering roles anywhere in the world.

[umersahi5p@gmail.com](mailto:umersahi5p@gmail.com) · [LinkedIn](https://www.linkedin.com/in/umer-sahi-b3bb19348/) · [Portfolio](https://umer-sahi.vercel.app/)
