## Azure Architecture with Custom Icons

```mermaid
graph TD
  A[Azure Function] -->|Process| B[Azure Database];
  B -->|Store| C[Azure Storage];
  C -->|Return| D[API];
```