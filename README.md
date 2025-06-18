# Architecture Overview

The AI agents leverage Large Language Models (LLMs) for their language understanding and generation capabilities. The system incorporates various frameworks and tools to empower users to build domain knowledge through meta-analyses and identify relevant datasets during the **business understanding** phase. Subsequently, in the **data understanding** phase, users can intuitively perform exploratory analyses on datasets using natural language. The AI agents facilitate the steps of **data extraction** and **processing** of datasets, including the **training** and **evaluation** of machine learning models to allow predictive analysis at scale. A human-in-the-loop approach is employed, requiring code review before execution.

---

![Image](https://github.com/user-attachments/assets/b3345c0e-5af8-482e-b8d3-6b5da801d1ab)

* **N8N** for workflow automation in domain exploration and dataset discovery.
* **AG2 (Autogen)**: Agentic framework to automate the data mining process.
* **Streamlit**: User interface that allows for interaction with the agents.
* **Supabase**: Cloud data storage, agent memory and encrypted user authentication.

### Agent Functionality Across CRISP-DM Phases

Autocrisp is built following the principles of a foundational framework for data mining. The Cross-industry standard process for data mining, known as CRISP-DM, is an open standard process model that describes common approaches used by data mining experts. It is the most widely-used analytics model.

---

![Image](https://github.com/user-attachments/assets/808576cc-c009-4d05-8818-796b1358fc1e)
![Image](https://github.com/user-attachments/assets/6ca75997-8db6-4b87-bb40-71685817d802)

### Integration of Technologies

Autocrisp is utilizing N8N for its business understanding capabilities by connecting the user in foremost with an orchestration agent that can answer direct questions or brainstorm ideas. The orchestration agent may delegate research tasks towards a set of agents capable of automating comprehensive literature research, identifying relevant datasets through targeted web searches and querying datasets using natural language to SQL.

---

![Image](https://github.com/user-attachments/assets/a7f5bae7-9175-4c41-b90c-17dd8c3edb20)
![Image](https://github.com/user-attachments/assets/83e0f309-842a-4049-9f0a-ab07d3928c2c)

The remaining phases data understanding, data preparation, modeling, and evaluation are supported by agents built on the Autogen (AG2) framework. These agents handle tasks such as:

* Exploratory data analysis
* Data cleaning
* Model training
* Model evaluation

All components are integrated into a Streamlit-based application, providing users with an interactive way to engage with the agents.
