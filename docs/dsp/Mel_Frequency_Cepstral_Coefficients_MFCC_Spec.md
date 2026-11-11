# Mel-Frequency Cepstral Coefficients (MFCC) Extraction Specification

## 1. Processing Chain
1. Pre-emphasis filter: $y[t] = x[t] - \alpha \cdot x[t-1]$ (with $\alpha = 0.97$).
2. STFT framing with Hanning window.
3. 26-channel triangular Mel filterbank spanning $300\text{Hz} - 8000\text{Hz}$.
4. Discrete Cosine Transform (DCT-II) yielding 13 static MFCC cepstral coefficients plus delta and delta-delta acceleration features.
