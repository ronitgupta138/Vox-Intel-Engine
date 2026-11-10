# FFT Spectral Energy Distribution & Spectral Flux Specification

## 1. Short-Time Fourier Transform (STFT)
- **Windowing:** 512-point Hanning window with 50% overlap (256-sample hop size, 16ms frame duration).
- **Spectral Centroid:**
  $$\text{Centroid} = \frac{\sum_{k=0}^{K-1} f_k \cdot |X[k]|}{\sum_{k=0}^{K-1} |X[k]|}$$
  Measures vocal brightness and vocal tract tension under cognitive strain.

## 2. Spectral Flux
$$\text{Flux}_t = \sum_{k=0}^{K-1} (|X_t[k]| - |X_{t-1}[k]|)^2$$
Quantifies sudden articulatory changes and voice quality shifts between consecutive audio frames.
