# EcoRAG: Multi-Hop Economic QA Benchmark for RAG  

*EcoRAG: A Multi-Hop Economic QA Benchmark for Retrieval-Augmented Generation Using Knowledge Graphs*  

---

**Overview**  
EcoRAG is a benchmark for testing multi-hop retrieval-augmented generation (RAG) with economic knowledge graphs.  
Unlike prior datasets (limited to 2–4 hops, shallow answers), EcoRAG:  
- Supports 4–7 hop reasoning  
- Includes linear, converging, and divergent subgraphs  
- Provides descriptive, context-rich answers  
- Uses domain-specific data (World Bank, IMF, ECB, etc.)  

---

**Features**  
- 3,114 QA pairs from 62 economic sources  
- Degree-balanced node sampling for diversity  
- Reusable pipeline for building new benchmarks  
- Evaluated on Hybrid RAG, ReRank RAG, and KG-RAG  

---

**Pipeline**  
Steps:  
1. Build KG from economic reports  
2. Sample nodes by degree  
3. Extract multi-hop paths  
4. Validate with LLM  
5. Generate Q&A pairs  
6. Evaluate with RAG methods  

Pipeline figure:  

![EcoRAG Benchmark Pipeline](EcoRAG%20Pipeline.png)  

---

**Results**  
- ReRank RAG performs best on converging paths (MRR up to 0.75 at 5 hops)  
- Hybrid RAG is consistent on divergent paths  
- KG-RAG struggles with deep reasoning  

---

**Resources**  
- Dataset & code: [EcoRAG Repository](https://github.com/haniehkh18/EcoRAG)  
- Paper (PDF): included in this repo  

---

**Citation**  
```bibtex
@InProceedings{10.1007/978-3-031-97144-0_15,
author="Khorashadizadeh, Hanieh
and Tiwari, Sanju
and Benamara, Farah
and Mihindukulasooriya, Nandana
and Groppe, Jinghua
and Sahri, Soror
and Ezzabady, Morteza
and Ieng, Fr{\'e}d{\'e}ric
and Groppe, Sven",
editor="Ichise, Ryutaro",
title="EcoRAG: A Multi-hop Economic QA Benchmark for Retrieval Augmented Generation Using Knowledge Graphs",
booktitle="Natural Language Processing and Information Systems",
year="2026",
publisher="Springer Nature Switzerland",
address="Cham",
pages="163--173",
abstract="Retrieval-Augmented Generation (RAG) enhances large language models (LLMs) by integrating external knowledge retrieval. However, existing multi-hop RAG benchmarks are limited by shallow reasoning depth, simple retrieval structures, and non-descriptive answers. We introduce EcoRAG, a novel multi-hop economic QA benchmark built on knowledge graphs (KGs). EcoRAG extends retrieval depth to seven-hop reasoning, incorporates complex subgraph structures, and leverages domain-specific economic knowledge. It enables a more realistic evaluation of retrieval and reasoning by bridging the gap between structured knowledge sources and generative models, while also providing a reusable benchmark to advance multi-hop RAG research.",
isbn="978-3-031-97144-0"
}

