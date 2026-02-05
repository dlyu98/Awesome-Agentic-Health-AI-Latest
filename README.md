# Awesome Agentic Health AI

This repository is a curated and regularly updated collection of the **latest projects, products, papers and breakthroughs** in **agentic artificial‑intelligence (AI) for healthcare**.  It draws inspiration from the original [Awesome‑AI‑Agents‑for‑Healthcare](https://github.com/AgenticHealthAI/Awesome-AI-Agents-for-Healthcare) repository, but focuses on the most recent work (through early 2026) and highlights real‑world deployments alongside academic advances.  The goal is to provide an accessible starting point for clinicians, researchers and developers exploring how multi‑agent systems and agentic AI can improve patient care, medical workflow and health‑equity.

## What is agentic AI?

Traditional healthcare AI tools are largely reactive: they produce predictions or summaries when prompted but leave control of the workflow to a clinician.  **Agentic AI** takes a different approach.  Multiple large‑language‑model (LLM)–based agents are orchestrated to **plan tasks, retrieve relevant information, cross‑validate one another’s outputs and adapt over time**.  In radiology, for example, a recent review notes that multi‑agent, retrieval‑augmented and uncertainty‑aware systems can reduce hallucination rates and improve diagnostic accuracy, though current implementations remain computationally demanding and require rigorous clinical validation【611328004656680†L182-L197】.  Adoption of LLMs for imaging has grown from ~30 % of departments in 2020 to over 75 % by 2024【611328004656680†L205-L217】, yet hallucination rates of 8–15 % persist【611328004656680†L205-L217】.  **Agentic AI aims to address this by distributing tasks across specialized agents and introducing checkpoints where errors are caught before they reach clinicians**【611328004656680†L182-L197】.

Other commentaries point out that agentic AI shifts radiology and other medical systems from passive, user‑triggered tools to **autonomous assistants** capable of **dynamic triaging, context‑aware reasoning and workflow management**; however, limited clinical validation and evolving regulatory frameworks remain key challenges【718437852469727†L138-L151】【718437852469727†L225-L256】.

## Ecosystem overview

The diagram below provides a high‑level view of the agentic health AI ecosystem.  It captures eight major categories of agentic systems described in this repository.

![Agentic Health AI ecosystem](images/agentic_health_ai_ecosystem.png)

## Latest projects and breakthroughs (2025‑2026)

The tables below summarize notable projects and papers from 2024–2026, organized by category.  Each entry lists the project or system, the year, a succinct description and the source.

### Multi‑modal clinical agents

| Project/Agent | Year | Key contributions | Sources |
|---|---|---|---|
| **M³Builder** | 2025 | Four specialized agents automate machine‑learning workflows for medical imaging—from data processing and environment configuration to auto‑debugging and model training.  The system introduces the **M3Bench** benchmark covering 14 datasets across five anatomies and three modalities.  When evaluated using Claude‑3.7‑Sonnet as the agent core, M³Builder achieved a **94.29 % task‑completion success rate**, outperforming prior ML‑agent designs【888183404684677†L53-L69】. | arXiv preprint【888183404684677†L53-L69】 |
| **AURA** | 2025 | A **multi‑modal medical agent** for understanding, reasoning and annotation.  AURA provides dynamic interactions and contextual explanations for medical images via a modular toolbox: (i) a segmentation suite for phase grounding, pathology and anatomy; (ii) a counterfactual image‑generation module to support hypothesis testing; and (iii) evaluation tools to assess diagnostic relevance and visual interpretability【875702780077740†L49-L67】.  It highlights a shift from static predictions to interactive decision support. | arXiv preprint【875702780077740†L49-L67】 |

### Radiology & imaging agents

| Project/Agent | Year | Key contributions | Sources |
|---|---|---|---|
| **RadFabric** | 2025 | A multi‑agent, multimodal reasoning framework for chest‑x‑ray interpretation.  Specialized agents detect pathologies, map findings to anatomical structures and synthesize visual, anatomical and clinical data.  **RadFabric achieves near‑perfect detection of challenging pathologies (accuracy 1.000) and an overall diagnostic accuracy of 0.799 compared with 0.229–0.527 for traditional systems**【169502549588149†L52-L66】.  It showcases modularity and interoperability via the Model Context Protocol. | arXiv preprint【169502549588149†L52-L66】 |
| **Diagnostic co‑pilot (AMIE)** | 2024‑2025 | In a Nature study on differential diagnosis, the **Articulate Medical Intelligence Explorer (AMIE)** demonstrated a **top‑10 diagnostic accuracy of 59.1 %**, outperforming unassisted clinicians (33.6 %) and improving clinicians’ performance when used as an assistant (51.7 % vs 36.1 %)【41675009081567†L372-L390】. | Nature article【41675009081567†L372-L390】 |

### Disease‑management & workflow agents

| Project/Agent | Year | Key contributions | Sources |
|---|---|---|---|
| **AMIE for disease management** | 2025 | AMIE was extended beyond diagnosis to **longitudinal disease management**.  A two‑agent architecture pairs a **Dialogue Agent** (patient‑facing) with a **Management Reasoning Agent** (plans investigations and treatments using clinical guidelines).  In a randomized virtual OSCE with 100 multi‑visit scenarios, specialist physicians rated AMIE’s management plans **non‑inferior to those of primary‑care physicians** and observed **significant improvements in treatment precision** (p < 0.05)【700379143592045†L343-L370】.  The system leverages guidelines from sources like the UK NICE and BMJ Best Practice and produces structured management plans【700379143592045†L221-L255】【700379143592045†L295-L303】. | Google Research blog【700379143592045†L221-L255】【700379143592045†L343-L370】 |

### Patient‑facing voice agents

| Project/Agent | Year | Key contributions | Sources |
|---|---|---|---|
| **Hippocratic AI voice agents (UHS deployment)** | 2025 | Universal Health Services partnered with Hippocratic AI to deploy **generative AI voice agents** that make post‑discharge phone calls.  These agents follow up with patients, review medication instructions and probe for new symptoms.  Thousands of patients have been contacted since launch, and the average patient satisfaction rating is **9.0 out of 10**.  Positive results have led to expansion across additional hospitals【212509038993599†L224-L251】. | Press release【212509038993599†L224-L251】 |

### Mental‑health & CBT agents

| Project/Agent | Year | Key contributions | Sources |
|---|---|---|---|
| **AutoCBT** | 2025 | An autonomous multi‑agent framework for cognitive behavioral therapy (CBT).  Starting from single‑turn consultation models, the authors introduce **dynamic routing and supervisory mechanisms** inspired by real counseling to produce high‑quality responses.  Experiments on bilingual datasets show that AutoCBT provides more helpful and contextually appropriate counselling responses than prior LLM‑based CBT systems【310586166793977†L53-L70】. | arXiv preprint【310586166793977†L53-L70】 |

### Personal‑health & navigation agents

| Project/Agent | Year | Key contributions | Sources |
|---|---|---|---|
| **Personal Health Agent (PHA)** | 2025 | A research prototype that analyzes wearable data, questionnaires and blood biomarkers to deliver personalized health insights.  The PHA decomposes tasks into three agents—a **data‑science agent**, a **domain‑expert agent** and a **health‑coach agent**—which reason collaboratively.  In evaluations with a real dataset of ~1,200 users and over 7,000 expert annotations, the data‑science agent improved analysis‑plan quality (75.6 % vs 53.7 % for the base model), and the domain‑expert agent produced more clinically relevant and personalized responses【623711362828657†L246-L260】【623711362828657†L306-L354】. | Google Research blog【623711362828657†L246-L260】【623711362828657†L306-L354】 |
| **Wayfinding AI** | 2025 | An early‑stage agent that helps users navigate online health information.  Wayfinding AI proactively asks clarifying questions to understand the user’s goals and provides deferred answers.  A randomized user study with 130 participants found that users preferred the agent over a baseline model across dimensions such as helpfulness, relevance, goal understanding and tailoring; conversations were also longer and more engaging【475443089103642†L326-L365】. | Google Research blog【475443089103642†L326-L365】 |

### Inclusive & accessibility agents

| Project/Agent | Year | Key contributions | Sources |
|---|---|---|---|
| **Agentic AI for disabilities and neurodivergence** | 2025 | A framework that assists individuals with disabilities and neurodivergence through four integrated agents: a **meal‑planner**, **reminder**, **food‑guidance** and **monitoring** agent.  These agents are coordinated via a hybrid reasoning engine to provide adaptive nutrition guidance, scheduling and real‑time monitoring.  Evaluation on synthetic data demonstrated improved nutritional adherence, higher reminder responsiveness, increased user satisfaction and fewer caregiver interventions【539836909864261†L831-L857】. | arXiv preprint【539836909864261†L831-L857】 |

### Training & benchmark environments

| Project/Agent | Year | Key contributions | Sources |
|---|---|---|---|
| **MedAgentGym** | 2025 | A **scalable interactive training environment** for code‑centric biomedical reasoning.  It includes **72,413 task instances across 129 categories** derived from 12 biomedical scenarios.  MedAgentGym offers interactive feedback, verifiable ground truth and a benchmark for 29 LLMs.  Reinforcement‑learning experiments show that training with MedAgentGym improves model performance and provides a cost‑effective alternative to proprietary models like GPT‑4o【404970063240360†L54-L69】. | arXiv preprint【404970063240360†L54-L69】 |

### Future & ongoing research

| Study/Initiative | Year | Description | Sources |
|---|---|---|---|
| **Nationwide randomized study of AI in virtual care** | 2026 | Google Research and Included Health announced a **nationwide randomized controlled trial** to evaluate conversational AI in real‑world virtual care.  The study will assess AI‑driven clinical reasoning, personalized health insights and navigation support at scale.  It builds on earlier work with AMIE, PHA and Wayfinding AI, and aims to generate robust prospective evidence for the safety and utility of these systems【891254307725479†L219-L257】【891254307725479†L281-L287】. | Google Research blog【891254307725479†L219-L257】【891254307725479†L281-L287】 |

## Contributing

Contributions that add **new papers, products or deployments (from 2024 onward)** or improve the summaries are welcome!  Please open a pull request with a clear description and provide a reliable source (peer‑reviewed paper, company announcement or reputable news article).  This project follows the all‑contributors specification – contributions of any kind are welcome.

## License

This repository is distributed under the **CC‑BY‑SA 4.0** license unless otherwise noted.  Individual papers and products linked here retain their original licenses; please refer to the source for details.

## Disclaimer

This list is maintained for research and educational purposes.  Inclusion does not imply endorsement or clinical readiness.  Many of the systems described here are research prototypes or early deployments.  Always refer to regulatory guidance and consult qualified professionals before applying AI systems in clinical practice.
