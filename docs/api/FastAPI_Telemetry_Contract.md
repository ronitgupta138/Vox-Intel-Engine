# FastAPI Async Streaming Audio Telemetry API Specifications

## 1. WebSocket Protocol
- `WS /ws/telemetry/audio-stream`:
  - Client streams raw 16-bit linear PCM chunks (512 samples per frame).
  - Server returns real-time JSON frames containing:
    ```json
    {
      "timestamp_ms": 1280,
      "pitch_f0_hz": 142.5,
      "spectral_centroid_hz": 2180.4,
      "energy_db": -18.2,
      "is_voiced": true
    }
    ```
