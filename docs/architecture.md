## 🧭 Architecture Diagram

```mermaid
flowchart LR
    subgraph Ingestion
        A[NASA PDFs] --> B[PDF Parser]
        B --> C[Semantic Chunker]
        C --> D["Embedder\ntext-embedding-3-large"]
        D --> E[(Qdrant)]
        C --> F[(BM25 Index)]
    end

    subgraph Query
        Q[User Query] --> R[FastAPI]
        R --> HR["Hybrid Retriever\nDense + BM25 + RRF"]
        HR --> E
        HR --> F
        HR --> RR["Cross-Encoder\nReranker"]
        RR --> G["LLM Generator\nGPT-4o-mini"]
        G --> A1[Answer + Citations]
    end

    subgraph Observability
        OT[OpenTelemetry] -.-> HR
        OT -.-> RR
        OT -.-> G
    end

    subgraph Evaluation
        EV[RAGAS Harness] --> Gold[Gold Set]
        EV --> Metrics["Faithfulness\nRelevancy\nPrecision"]
    end
```
