# Contributing to Vox Intel Engine

Thank you for your interest in contributing to **Vox Intel Engine**! We welcome contributions to audio digital signal processing (DSP), Fourier spectral analysis, voice acoustic feature extraction, and real-time streaming REST/WebSocket endpoints.

---

## 🛠️ Development Workflow

1. **Clone the Repository**:
   ```bash
   git clone https://github.com/ronitgupta138/vox-intel-engine.git
   cd vox-intel-engine
   ```

2. **Branching Conventions**:
   - `feat/<feature-name>`: New audio DSP transforms, feature extractors, or FastAPI routes
   - `fix/<bug-name>`: Sampling rate, buffer boundary, or audio codec bug fixes
   - `perf/<optimization>`: NumPy/SciPy vectorized audio processing optimizations
   - `docs/<doc-topic>`: Audio pipeline documentation and API schemas
   - `test/<test-suite>`: Synthetic waveform and audio fixture additions

3. **Running Builds & Tests**:
   Ensure virtual environment is active and pytest passes:
   ```bash
   pytest tests/
   ```

---

## 📝 Pull Request Guidelines

- **Commit Message Format**: Follow conventional commits (`feat:`, `fix:`, `perf:`, `docs:`, `test:`).
- **Vectorized Math**: Audio DSP transforms (FFT, Mel spectrograms, MFCC) must utilize vectorized NumPy/SciPy routines rather than Python for-loops to preserve real-time streaming latency.
- **Clean Typing**: Maintain Python 3.11+ type hints across function signatures.

---

## ⚖️ License
By contributing, you agree that your contributions will be licensed under the project's [MIT License](LICENSE).
