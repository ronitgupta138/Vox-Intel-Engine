# Audio DSP Pipeline Energy Conservation Invariant Tests

## 1. Parseval's Theorem Verification
Asserts energy conservation between time-domain and frequency-domain representations:
$$\sum_{n=0}^{N-1} |x[n]|^2 = \frac{1}{N} \sum_{k=0}^{N-1} |X[k]|^2$$
Any energy loss $> 0.01\%$ flags invalid filter windowing or numerical underflow.
