# Time-Domain Autocorrelation Pitch Extraction ($F_0$ Tracking)

## 1. Algorithmic Formulation
Vox-Intel-Engine extracts vocal fundamental frequency ($F_0$) directly from raw 16kHz PCM audio buffers using normalized autocorrelation:
- **Autocorrelation Function:**
  $$R(\tau) = \sum_{n=0}^{N-\tau-1} x[n] \cdot x[n+\tau]$$
- **Pitch Search Range:**
  Bounded between $50\text{Hz}$ and $400\text{Hz}$ (lag $\tau \in [40, 320]$ samples at 16kHz sample rate).

## 2. Center Clipping Pre-Processing
Before correlation, signal samples pass through a 3-level non-linear center clipper to suppress higher formant harmonics:
$$y[n] = \begin{cases} x[n] - C_L, & x[n] > C_L \\ 0, & |x[n]| \le C_L \\ x[n] + C_L, & x[n] < -C_L \end{cases}$$
where $C_L = 0.3 \times \max(|x[n]|)$.
