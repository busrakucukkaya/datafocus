
Some content here about the existing page.

## Docker Compose Diagram

graph TD;
    A[Grafana] -->|depends on| B[Prometheus];
    A -->|depends on| C[Loki];
    D[Promtail] -->|logs from| E[Docker Socket];
    F[cAdvisor] -->|monitors| E;

    A -->|uses network| G[datatouch-network];
    B -->|uses network| G;
    C -->|uses network| G;
    D -->|uses network| G;
    F -->|uses network| G;

    E[Docker Socket] -->|provides logs| D;
    E -->|provides metrics| F;