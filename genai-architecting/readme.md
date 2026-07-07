# Functional Requirements

Loqua is an existing online language learning platform with approximately 100 active students located in Europe and North America learning French.

The company wants to integrate Generative AI into the platform to make learning language judgment-free, student own pace and  available 24/7.

To protect learner privacy and reduce operational costs, Loqua has decided to self-host its AI infrastructure instead of relying entirely on commercial hosted LLM providers.

The target infrastructure budget is **5000** for an on-premises AI server capable of serving the expected student workload.

---

# Assumptions

The following assumptions are made for this case study:

- Loqua currently has approximately **100 active students**.
- Student usage is spread throughout the day rather than occurring simultaneously.
- An open-source LLM can provide sufficient quality for B1/B2 French tutoring.
- The selected model can run efficiently on hardware within the allocated infrastructure budget.
- AI inference will be hosted on a single on-premises server with a public API exposed securely over the internet.
- Additional compute resources can be added later if the user base grows.

---

# Data Strategy

The AI assistant should provide accurate and pedagogically sound responses while respecting copyright and learner privacy.

Rather than relying solely on the LLM's internal knowledge, the application will retrieve relevant learning content using Retrieval-Augmented Generation (RAG) before generating responses.

Student conversations should be stored securely to enable personalization while complying with applicable data protection regulations (e.g., GDPR).

---

# Technical Considerations

Candidate open-source models include:

- IBM Granite
- Llama
- Mistral
- Qwen

IBM Granite is considered because it is an open-source model with training data that is traceable so we can avoid any copyright issues and we are able to know what is going on in the model.

https://huggingface.co/ibm-granite

