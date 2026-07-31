flowchart LR
    U[👤 User]

    subgraph Frontend
        F[Web / Mobile Application]
    end

    subgraph Backend
        API[REST API]
        Logic[Business Logic]
    end

    subgraph AI
        Model[AI / ML Model]
    end

    subgraph Database
        DB[(MySQL / MongoDB)]
    end

    U --> F
    F --> API
    API --> Logic
    Logic --> DB
    Logic --> Model
    DB --> Logic
    Model --> Logic
    Logic --> API
    API --> F
    F --> U
