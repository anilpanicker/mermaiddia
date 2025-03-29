```mermaid
graph TD
    A[Raw Data (Bronze)] --> B{Landing Zone};
    B --> C[Raw Tables (Bronze)];
    C --> D{Data Validation & Cleaning};
    D --> E[Cleaned Tables (Silver)];
    E --> F{Data Transformation & Aggregation};
    F --> G[Curated Tables (Gold)];
    G --> H[Data Marts/Analytics];
    H --> I[Reporting & BI];

    subgraph Bronze Layer
        B;
        C;
    end

    subgraph Silver Layer
        E;
    end

    subgraph Gold Layer
        G;
    end

    style A fill:#f9f,stroke:#333,stroke-width:2px
    style B fill:#eef,stroke:#333,stroke-width:2px
    style C fill:#eef,stroke:#333,stroke-width:2px
    style D fill:#f9f,stroke:#333,stroke-width:2px
    style E fill:#efe,stroke:#333,stroke-width:2px
    style F fill:#f9f,stroke:#333,stroke-width:2px
    style G fill:#ffffe0,stroke:#333,stroke-width:2px
    style H fill:#e0ffff,stroke:#333,stroke-width:2px
    style I fill:#f0f8ff,stroke:#333,stroke-width:2px
