# Real-Time Audio Frame DSP Pipeline Latency Benchmarks

## 1. Performance Profile
- **Input Chunk:** 32ms audio buffer (512 samples at 16kHz).
- **Processing Breakdown:**
  - Hanning Windowing & FFT: 0.18ms
  - Autocorrelation $F_0$ Pitch Estimation: 0.82ms
  - Spectral Feature Extraction (Centroid, Flux): 0.14ms
  - **Total Pipeline Latency:** 1.14ms (< 4% of the 32ms real-time budget).
