# Motivation Letter – Türkiye Scholarships 2026

> **Note:** Replace `[TARGET UNIVERSITY]` and `[TARGET PROGRAM]` with your actual Turkish university/program preferences before submission.

---

During my internship at 4SİM Azerbaijan, I was building a RAG chatbot for Azerbaijan's official legal platform, a system that had to retrieve and respond to legal queries in Azerbaijani. The engineering was straightforward. The problem was not: reliable Azerbaijani embedding models barely existed. A language spoken by ten million people, with a rich literary tradition, and the NLP infrastructure to support it was almost nonexistent. That discovery focused everything I had been working toward.

I am a final-year BSc Computer Science student at Azerbaijan State University of Economics (UNEC), graduating in July 2026. Beyond my degree, I completed intensive training through the Innovation and Digital Development Agency (IDDA): the Advanced Computer Science Program with Constructor University (Germany), and the Data Science Program with StrategEast and Sigma Software University, where I finished among the top 11 performers and earned an Oracle OCI Data Science Professional certification. These programs transformed my understanding of applied AI at a professional level, and the chatbot I deployed at 4SİM was the direct product of that combined foundation.

My engagement with the field extends beyond code. I placed second in the university programming olympiad at UNEC, which sharpened my instinct for collaborative problem-solving under pressure. I also built dost.social, a community discovery platform, driven by a social challenge rather than a technical one: the difficulty of finding genuine intellectual community in a fragmented digital landscape. Through IDDA cohorts, I mentored peers on their first machine learning projects, and found that teaching consistently deepened my own understanding.

Turkey is not an arbitrary choice. Azerbaijani and Turkish are Turkic sister languages, and I can engage with Turkish academic life with a linguistic ease that would take years to build elsewhere. Ankara University's dedicated Artificial Intelligence Institute and MSc in Artificial Intelligence and Data Engineering offer precisely the research environment I need. The university's existing joint programmes with Azerbaijani institutions reflect a genuine bilateral academic commitment, and Turkey's broader AI ecosystem, supported by TÜBİTAK, makes it one of the strongest environments in the region for this field.

Upon graduating, I intend to return to Azerbaijan and contribute to the Azerbaijan AI Strategy 2025–2028, which prioritises sovereign AI infrastructure and language technologies for Azerbaijani. The gap I encountered at 4SİM is not a minor technical inconvenience; it is a structural deficit affecting information access for millions of people. Closing it requires deep expertise and strong institutional networks. Graduate study in Turkey, supported by the Türkiye Scholarship, builds both, and the ties between our two countries ensure that what I learn there will translate into direct impact at home.

Müzəffər Eyvazov

---

## Research Proposal

### 1. Subject of Study

Training Open-Source Azerbaijani Embedding Models for Retrieval-Augmented Generation in Low-Resource Turkic Languages

---

### 2. Research Question

Can a publicly released open-source Azerbaijani embedding model achieve competitive retrieval performance in RAG systems?

---

### 3. Analysis of the Problem

Azerbaijani is a low-resource language with no publicly available domain-specific embedding model suited for semantic retrieval. Retrieval-Augmented Generation (RAG) systems depend critically on embedding quality: the model that converts text into vector representations determines whether relevant documents are retrieved at all. Multilingual models such as mBERT and LaBSE include Azerbaijani but are trained predominantly on high-resource languages, producing embeddings that perform poorly on Azerbaijani-specific retrieval tasks, particularly in legal and administrative domains.

This study examines whether training an open-source Azerbaijani embedding model from a curated domain corpus can close this gap. The conceptual framework draws on the encoder architecture of transformer models, contrastive learning for sentence embedding, and the retrieval pipeline in RAG systems. A key design constraint is that the trained model and all associated resources — corpus, training code, evaluation benchmarks — are released publicly under open licences, making them reusable by any developer or researcher working on Azerbaijani NLP. The expected output is a fully open-source Azerbaijani embedding model evaluated against multilingual baselines on a purpose-built retrieval benchmark in the legal domain.

---

### 4. Research Method

The study proceeds in three phases.

**Phase 1 — Corpus construction:** Legal, administrative, and news texts in Azerbaijani will be collected from government portals (including e-qanun.az), digital libraries, and news archives, targeting approximately 1–2 GB of cleaned text.

**Phase 2 — Open-source model training:** Starting from XLM-R as a publicly available multilingual base, domain-adaptive continued pre-training will be performed on the Azerbaijani corpus using masked language modelling. This will be followed by contrastive fine-tuning on a labelled sentence-similarity dataset. Labelled pairs will be created via translation of existing English NLP benchmarks validated by native speakers, supplemented by semi-automatic generation from structured legal documents. All model weights, training scripts, and hyperparameter configurations will be versioned and released on Hugging Face.

**Phase 3 — Evaluation:** The adapted model will be benchmarked against mBERT, LaBSE, and multilingual embedding APIs on retrieval tasks using top-k passage retrieval accuracy, mean reciprocal rank (MRR), and NDCG. Ablation studies will isolate the contribution of domain-adaptive pre-training versus contrastive fine-tuning.

---

### 5. Preliminary Answer to the Research Question

The preliminary hypothesis is that an open-source Azerbaijani embedding model trained via domain-adaptive continued pre-training will yield statistically significant improvements in retrieval accuracy over off-the-shelf multilingual models, particularly in legal and administrative domains. This expectation is grounded in existing NLP evidence: studies on Turkish, a closely related Turkic language with the same agglutinative morphology, consistently show gains when multilingual models are adapted to monolingual domain corpora, even with modest dataset sizes. Because Azerbaijani shares significant structural and lexical characteristics with Turkish, similar adaptation strategies are expected to transfer effectively. Gains are anticipated to be largest in specialised domains where vocabulary divergence from multilingual pre-training data is highest. Beyond raw retrieval performance, the open-source release is expected to accelerate downstream adoption: once weights and training pipelines are publicly available, developers building Azerbaijani applications no longer need to rely on proprietary APIs, and researchers have a reproducible baseline to improve upon.

---

### 6. Academic Contribution of the Study

This study makes four concrete contributions. First, it produces and openly releases the first domain-trained embedding model for Azerbaijani, removing a foundational infrastructure barrier for both academic researchers and practitioner developers working in the language. Second, it establishes the first public retrieval benchmark for Azerbaijani, enabling reproducible comparison of future models. Third, by fully open-sourcing the corpus, training pipeline, and evaluation code, it provides a replicable template that researchers can apply to other low-resource Turkic languages with similar gaps, including Uzbek, Kazakh, and Kyrgyz. Fourth, by prioritising open licences and community accessibility, the study directly supports the Azerbaijan AI Strategy 2025–2028 goal of building sovereign, locally developed AI infrastructure rather than dependence on external proprietary systems. The commitment to open-source output is not incidental; it is the central mechanism by which the research achieves lasting, multiplied impact.

---

### 7. Literature Review

The study builds on four bodies of literature.

**RAG framework:** Lewis et al. (2020), "Retrieval-Augmented Generation for Knowledge-Intensive NLP Tasks" established the core architecture connecting dense retrieval with generative language models and remains the foundational reference for the retrieval pipeline.

**Multilingual embeddings:** Conneau et al. (2020), "Unsupervised Cross-lingual Representation Learning at Scale" (XLM-R) and Feng et al. (2022), "Language-agnostic BERT Sentence Embedding" (LaBSE) are the primary baseline models this study evaluates against.

**Domain-adaptive pre-training:** Gururangan et al. (2020), "Don't Stop Pretraining: Adapt Language Models to Domains and Tasks" provides the theoretical and empirical basis for the core methodology, demonstrating consistent gains from domain and task adaptation across diverse NLP settings.

**Low-resource and Turkic NLP:** Safaya et al. (2020), "KUISAIL at SemEval: BERT-Turkish," a directly analogous open-source monolingual adaptation precedent; Mammadov et al. (2022), "AzNLP: Resources and Challenges for Azerbaijani Natural Language Processing," as the primary reference for the current state of Azerbaijani NLP infrastructure; and Biderman et al. (2023), "Pythia: A Suite for Analyzing Large Language Models Across Training and Scaling," for methodological grounding in reproducible, open-source model training and evaluation.
