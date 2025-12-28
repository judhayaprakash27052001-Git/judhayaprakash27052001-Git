graph TB
    A[Developer Push] --> B{GitHub/GitLab}
    B --> C[Jenkins Controller]
    C --> D[Shared Agent Pool]
    D --> E[Dynamic Environment]
    E --> F[Security Scanning]
    F --> G{Quality Gates}
    G --> H[Approval Automation]
    H --> I[Production Deployment]
    
    subgraph "Observability Layer"
        O1[Prometheus Metrics]
        O2[ELK Logs]
        O3[Cost Dashboard]
    end
    
    subgraph "Security Layer"
        S1[SAST/DAST]
        S2[Container Scanning]
        S3[Secret Detection]
    end
    
    C -.-> O1
    C -.-> O2
    C -.-> O3
    F -.-> S1
    F -.-> S2
    F -.-> S3
