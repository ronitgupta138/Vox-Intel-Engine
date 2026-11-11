# FastAPI Health and Kubernetes Readiness Probe Endpoints

## 1. Specifications
- `GET /healthz`: Liveness probe asserting process loop responsiveness (returns HTTP 200 `{"status": "healthy"}`).
- `GET /readyz`: Readiness probe asserting DSP audio circular buffers and model weights are initialized in memory.
