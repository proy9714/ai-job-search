---
framework_version: 1.1.1
---

# Candidate Profile

<!-- Populated by /setup Path A (documents/) on 2026-11-02. Sources: Resume.pdf, transcripts, reference letters, project reports. -->

## Identity
- **Name:** Priyadarshi Roy
- **Location:** Cölbe, Germany (near Marburg, Hesse)
- **Phone:** +49 1521-7847618
- **Email:** proy9714@gmail.com
- **LinkedIn:** https://www.linkedin.com/in/priyadarshi-roy/
- **GitHub:** https://github.com/proy9714
- **Status:** MSc Data Science student at Philipps-Universität Marburg, thesis submission November 2026. Available to start immediately.
- **Constraints:** Open to relocating anywhere; Europe first, India second. Full-time permanent roles only. German student residence permit expires March 2027, so Europe roles need permit/visa support (see 04-job-evaluation.md Eligibility Gate).

### Languages
<!-- Every language you can work in professionally, with your honest level. Used by the
Language Gate in 04-job-evaluation.md and by job-scraper/search-queries.md's query-language
generation. Omit any language you don't actually work in - an undeclared language is treated as
a hard no, not a gap to smooth over. -->

| Language | Level | Notes |
|----------|-------|-------|
| English | C2 | Working language; CEO reference praises spoken and written English |
| Bengali | Native | |
| Hindi | C2 | |
| Japanese | JLPT N3 | Intermediate |
| German | A2 | Elementary - postings requiring fluent/business German should FLAG or FAIL |

## Education

| Degree | Period | Institution | Key Topics |
|--------|--------|-------------|------------|
| MSc Data Science | 2024 - present (in progress, thesis submission November 2026) | Philipps-Universität Marburg, Germany | Computer Vision I, Natural Language Systems, Intro to NLP, Machine Learning with Graphs, Data Integration, Matrix Methods in Data Analysis, Numerical Methods, Implementation of Database Systems, Project Work Data Science (12 ECTS), Advanced Topics seminar |
| MSc Computer Science | 2019 - 2021 | St. Xavier's College (Autonomous), Kolkata, India (affiliated to University of Calcutta) | Algorithms, Advanced DBMS, Distributed OS, AI, Compiler Design, Cryptography and Network Security, Data Mining and Warehousing, Image Processing and Pattern Recognition |
| BSc Computer Science | 2016 - 2019 | St. Xavier's College (Autonomous), Kolkata, India (affiliated to University of Calcutta) | Data Structures, DBMS, Operating Systems, Computer Networks, Design and Analysis of Algorithms, Digital System Design |

**Grades:**
- MSc Data Science: current average 10.21 on the German 0-15 point scale (10-12 = above average), 81 ECTS as of 1 July 2026. Best modules: Data Integration 13, Machine Learning with Graphs 12, Natural Language Systems 12, Large Specialization Module CS 12, Matrix Methods in Data Analysis 11, Advanced Topics seminar 11. Degree not yet awarded.
- MSc Computer Science: CGPA 8.17/10, Grade A, Class I.
- BSc Computer Science: CGPA 7.99/10, Grade A, Class I.

**Master's thesis (in progress):** Computer Vision for Historical Art Analysis, Philipps-Universität Marburg (2026 - present).

## Professional Experience

### Machine Learning Engineer - Sprinriver Technology Private Limited (Aug 2021 - Aug 2024)
Kolkata, India
- Developed production NLP systems for automated document understanding, including multi-document summarisation and highlight extraction pipelines that replaced manual review of large document collections.
- Built enterprise Retrieval-Augmented Generation (RAG) applications using GPT-3.5 Turbo, embedding-based retrieval, LangChain, and vector search, enabling employees to query organisational knowledge in natural language.
- Designed modular LLM orchestration workflows and evaluation pipelines, improving the reliability, maintainability, and scalability of Generative AI applications.
- Developed and deployed Python REST APIs using Flask to serve machine learning models in production.
- Collaborated with engineering and product teams across the ML lifecycle, translating business requirements into deployed AI solutions.

**Named projects (from CEO reference letter, Dec 2023):**
- **Texplicit:** AI-based analytics tool that reads, digests and curates information from multiple internet sites and intranet documents. Role: backend developer and ML engineer, building the API endpoints and owning all ML-related work.
- **Mental-health support platform:** support-focused social media platform. Role: full-stack developer (Angular frontend, Python/Flask backend).
- **E-books Junction:** online e-book store. Role: backend developer (Node.js/Express API endpoints).
- The CEO also credits "a track record of successfully implementing multiple generative AI solutions."

**Note:** the reference letter (dated 04-Dec-2023, written while employed) states the title as "Software Engineer". The candidate's title of record on the CV is Machine Learning Engineer. See the prepared answer in `07-interview-prep.md`.

## Research Experience

### Master's Thesis: Computer Vision for Historical Art Analysis (2026 - present)
Philipps-Universität Marburg. Technologies: PyTorch, Vision Transformers, Vision-Language Models, Human Pose Estimation, Image Retrieval.
- Researching computer vision foundation models for semantic understanding of human figures, interactions, and visual structures in historical artworks.
- Developing multimodal pipelines combining human pose estimation, object detection, image embeddings, and geometric verification for structured analysis of paintings.
- Investigating domain shift and representation learning when transferring vision models from natural images to non-photographic artistic media, including scene graph generation and knowledge-based retrieval.

### Independent Scientific Project: "Noli Me Tangere: Pose-Grounded Human-Human Interaction Scene Graphs for the Computational Analysis of Paintings" (2026)
Philipps-Universität Marburg, sole author.
- Literature review of computer vision for art history (about 80 references), covering CNN, transformer and vision-language-model approaches, and identifying gaps such as the absence of human-human interaction modelling and artwork-specific scene graph generation.
- **Proposed and designed** a four-stage pipeline: open-vocabulary human detection (Grounding DINO), pose estimation, pose features and learned pose embeddings, then VLM reasoning that produces structured interaction triplets (e.g. <Mary Magdalene, reaches_toward, Christ>). Argued for grounding VLMs in measurable geometry rather than prompting them directly, citing their hallucination rates on art-historical relations.
- Collected a corpus of about 1,000 artworks from ART Research Network, JSTOR Art & Art History, and the Prometheus image archive. Designed a deduplication stage that combines deep image embeddings with geometric verification, with manual review of borderline cases (copies vs. reproductions).
- Proposed applications: narrative-based artwork retrieval, computational study of artistic evolution, and art-historical knowledge graphs.
- *Framing note: this report is a proposal and design. Describe the pipeline as proposed or under development, not as built and evaluated, unless the thesis has since delivered results.*

## Independent Projects
- **Study Advisor (RAG-based chatbot, 2025):** Multi-stage RAG pipeline for academic advising at Philipps-Universität Marburg, with intent classification, chat-history integration, query decomposition, Text-to-SQL, semantic retrieval, context summarisation, and LLM response generation. Hybrid retrieval inside PostgreSQL using pgvector (semantic search) and pg_trgm (fuzzy matching), so no separate vector database is needed. FastAPI backend, Vue.js frontend over WebSocket. Built from university XML data (Marvin portal) mapped to a relational schema. Benchmarked Llama 3.1-70B against Gemini 2.5-Flash with RAGAS over 75 questions: Gemini led on faithfulness (0.65 vs 0.44) and answer correctness (0.57 vs 0.47). Two-person university project; Priyadarshi owned the system architecture. Tech: Python, FastAPI, LangChain, PostgreSQL, pgvector, Vue.js.
- **NLS Voice Assistant (2026):** Task-oriented voice assistant for weather queries and multi-turn calendar management, integrating speech recognition (Faster-Whisper), local LLM orchestration (Ollama), and text-to-speech in a containerised Docker Compose pipeline. Built a scenario-based evaluation framework (intent accuracy, slot accuracy, temporal resolution, task completion rate), reaching 100% intent accuracy across evaluated scenarios. Analysed failure modes such as ASR errors and ambiguous time expressions.
- **Multi-Label Emotion Classification (2025):** Binary Relevance logistic regression over 768-dimensional BERT embeddings with balanced class weighting. Applied MLSMOTE in embedding space to address severe label imbalance (training samples 2,768 to 4,724 across 28 label combinations). Weighted F1 0.81, best per-class F1 0.85 (fear), minority-class recall 0.92 (anger). Tech: Python, PyTorch, Hugging Face Transformers, Scikit-Learn.
- **Distributed Discovery of Inclusion Dependencies (2024):** Fault-tolerant distributed system for discovering inclusion dependencies in datasets larger than single-node memory, built with the Akka actor framework and ported to Apache Spark. Tech: Java, Akka, Apache Spark.
- **Comparative Study of NLP Models for Text Classification (fake news detection) (2021):** MSc final-year project evaluating classical ML and deep learning approaches across multiple algorithms and feature representations. Tech: Python, TensorFlow, Keras, NLTK, Scikit-Learn.
- **HandGX - Hand Gesture / ASL Recognition (2019):** BSc final-year project. CNN-based recognition of American Sign Language gestures, covering preprocessing, feature extraction and mobile deployment. Tech: Python, OpenCV, TensorFlow, Keras, Kivy.
- **Genetic Algorithms term paper (MSc, 2019-2021).**

### Open Source
- **GPT Researcher (GitHub contributor, 2024)** - github.com/assafelovic/gpt-researcher: contributed feature implementations, bug fixes and code improvements to an open-source autonomous research agent (LLM orchestration, web retrieval, RAG components), delivered through reviewed pull requests.

## Technical Skills

### Programming & ML
- **Python** (primary): PyTorch, TensorFlow, Keras, Scikit-Learn, Hugging Face Transformers, Pandas
- **Other languages:** Java, C++, JavaScript, SQL
- **Machine Learning:** deep learning, neural networks, model evaluation, feature engineering, ML lifecycle
- **Generative AI:** LLMs, RAG, LangChain, prompt engineering, semantic search, RAGAS evaluation, agentic workflows, Text-to-SQL
- **Computer Vision:** OpenCV, Vision Transformers, human pose estimation, object detection, image retrieval, multimodal AI, vision-language models
- **Speech:** ASR (Faster-Whisper), TTS

### Domain Expertise
- NLP and document understanding (summarisation, highlight extraction, classification)
- Retrieval-Augmented Generation and LLM application engineering
- Computer vision for cultural heritage and digital art history (pose, scene graphs, domain shift)
- Data integration and databases

### Software & Tools
- Backend and MLOps: FastAPI, Flask, REST APIs, Docker, Docker Compose, Git, Linux, Ollama
- Data: PostgreSQL, pgvector, pg_trgm, MongoDB, MySQL, Apache Spark, Akka
- Web: Angular, Node.js/Express, Vue.js

## Certifications
- LangChain for LLM Application Development - DeepLearning.AI
- LangChain: Chat with Your Data - DeepLearning.AI
- Natural Language Processing with Classification and Vector Spaces - Coursera
- Build Basic Generative Adversarial Networks (GANs) - Coursera
- Python and Computer Vision Bootcamp - ShapeAI

## Publications
None yet.

## Awards
None listed.

## Extracurricular
- Leadership role in the annual Computer Science departmental festival "Exabyte", St. Xavier's College.
- National Service Scheme (NSS) volunteer, helping underprivileged school children in rural areas.

## References
- Dr. Romit Beed, Head of the Department of Computer Science, St. Xavier's College (Autonomous), Kolkata (rbeed@sxccal.edu). Taught the candidate across BSc and MSc for five years.
  Quote: "demonstrated exceptional proficiency in programming" / "communicates eloquently with both professors and peers, which can be attributed to his clarity of thought."
- Dr. Prabir Kumar Aditya, Chief Executive Officer, Sprinriver Technology Private Limited (contact details not on file; letter dated 04-Dec-2023). Direct employer, 2021-2024.
  Quote: "exceptional aptitude in swiftly comprehending new domains and delving deeply into the respective subjects" / "his structured approach to formulating problem statements and executing plans meticulously."

More references available upon request.
