# Lexical Cadence Metrics & Speech-to-Pause Ratio Analysis

## 1. Cadence & Pace Computation
- **Words Per Minute (WPM):**
  $$\text{WPM} = \frac{\text{Total Words Recognized}}{\text{Duration in Minutes}}$$
  Target conversational baseline: 130–160 WPM.
- **Speech-to-Pause Ratio:**
  $$\text{Ratio} = \frac{T_{\text{voiced}}}{T_{\text{silence}}}$$
  Identifies unnatural hesitations, cognitive stalls, or manic pacing.

## 2. Disfluency Filler Detection
Automated regex and phonetic phoneme scoring detects common fillers ("um", "uh", "like", "you know") and measures filler density per 100 words.
