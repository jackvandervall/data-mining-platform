# AutoCrisp: Agentic Data Mining Platform

> **Note:** This repository serves as a technical showcase for a proprietary application. Due to NDA and IP restrictions, the source code is not public.

## Description

**AutoCrisp** is a low-code, agentic orchestration platform designed to democratize the data science lifecycle. It enables domain experts to execute end-to-end data mining workflows—from hypothesis generation to predictive modeling—without writing raw code.

AutoCrisp strictly adheres to the **CRISP-DM** (Cross-Industry Standard Process for Data Mining) methodology. It utilizes a multi-agent architecture to enforce rigor in the **Business Understanding** and **Data Preparation** phases, preventing the common "garbage-in, garbage-out" failure mode of autonomous AI.

![Image](https://github.com/user-attachments/assets/6ca75997-8db6-4b87-bb40-71685817d802)


## Key Features

* **Automated Domain Research:** Leverages N8N workflows to perform meta-analyses and identify relevant external datasets before modeling begins.
* **Semantic Data Exploration:** Allows users to query complex datasets using natural language, translating intent into executable SQL/Pandas operations.
* **Human-in-the-Loop (HITL) Governance:** Critical code execution steps (cleaning, training) require user review, mitigating LLM hallucination risks.
* **Stateful Memory:** Agents retain context across the entire project lifecycle via encrypted cloud storage.

## Technical Architecture

The system integrates a hybrid stack of deterministic workflows and agents:

* **AG2 (AutoGen):** The core agentic framework handling the "heavy lifting" of code generation, error correction, and iterative reasoning.
* **N8N:** Handles orchestration of deterministic tasks (web search, API connectors) during the *Business Understanding* phase.
* **Streamlit:** Provides the interactive frontend, rendering agent dialogues and data visualizations.
* **Supabase:** Serves as the backend for vector memory, dataset storage, and encrypted user authentication.

## The CRISP-DM Workflow Implementation

AutoCrisp maps specific AI agents to the phases of the industry-standard data mining lifecycle:

### 1. Phase: Business Understanding (N8N Orchestration)

The system initiates with an Orchestration Agent that scopes the problem. It delegates tasks to research agents capable of literature review and dataset discovery.

**Orchestration Agent**
![Image](https://github.com/user-attachments/assets/a7f5bae7-9175-4c41-b90c-17dd8c3edb20)

**Research Agents**
![Image](https://github.com/user-attachments/assets/83e0f309-842a-4049-9f0a-ab07d3928c2c)


### 2. Phase: Data Operations & Modeling (AG2 Agents)

Once data is ingested, specialized Autogen agents take over. These agents operate in a conversable loop to execute:

* **Sanitization:** Detecting missing values and anomalies.
* **Feature Engineering:** Proposing and creating new variables based on domain context.
* **Training & Evaluation:** Running scikit-learn/PyTorch models and interpreting confusion matrices for the user.

**Agentic CRISP-DM Diagram**
![Image](https://github.com/user-attachments/assets/6ca75997-8db6-4b87-bb40-71685817d802)

## Installation & Setup

```bash
# Clone the repository
git clone https://github.com/jackvandervall/autocrisp.git

# Install dependencies (Recommend using a virtual environment)
pip install -r requirements.txt

# Configure Environment Variables
# Create a .env file containing your LLM provider keys and Supabase credentials
cp .env.example .env

# Launch the Application
streamlit run app.py

```


## Credits

Developed by Jack van der Vall in collaboration with a leading European academic research center for data science and AI based in Rotterdam. 
