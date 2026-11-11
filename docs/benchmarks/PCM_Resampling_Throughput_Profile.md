# Polyphase Sinc Audio Resampling Throughput Benchmark

## 1. Throughput Findings
- Converts 48kHz / 44.1kHz browser microphone inputs down to 16kHz model sample rate.
- Polyphase FIR filterbank processes 1,000,000 audio samples in $< 12\text{ms}$ on CPU, utilizing $< 1.5\%$ of available core budget.
