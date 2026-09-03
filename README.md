# ONLY FOR YOUR EYES 😍
### *ARE YOU AUTHORISED TO ACCESS SUPER SECRET INFORMATION?*

A cybersecurity-themed, multimodal human-verification desktop system engineered for hackathons. Masquerading as an ultra-classified defense intelligence terminal, the application subjects the user to four increasingly sophisticated biological and cognitive authentication protocols before granting clearance to "classified" intelligence.

---

## Table of Contents
1. [Problem Statement](#problem-statement)
2. [Core Concept & The Joke](#core-concept--the-joke)
3. [System Architecture](#system-architecture)
4. [Verification Protocols](#verification-protocols)
   - [Protocol 01: Human Cognition Verification](#protocol-01-human-cognition-verification)
   - [Protocol 02: Behavioural Typing Analysis](#protocol-02-behavioural-typing-analysis)
   - [Protocol 03: Multimodal Expression + Gesture Verification](#protocol-03-multimodal-expression--gesture-verification)
   - [Protocol 04: Voice Response Verification](#protocol-04-voice-response-verification)
5. [Final Clearance Assessment & Transmission](#final-clearance-assessment--transmission)
6. [Strict Gate Failure Behavior](#strict-gate-failure-behavior)
7. [AI / ML & Computer Vision Techniques](#ai--ml--computer-vision-techniques)
8. [Installation & Execution](#installation--execution)
9. [Asset Extensibility](#asset-extensibility)
10. [Privacy, Ethical Disclosures & Limitations](#privacy-ethical-disclosures--limitations)
11. [Team Contributions](#team-contributions)

---

## Problem Statement
Standard CAPTCHAs and single-factor authenticators are vulnerable to automated bot scripts, browser macros, and synthetic injection attacks. As generative AI makes trivial work of optical character recognition and multi-choice challenges, verifying authentic human presence requires multidimensional evaluation spanning semantic cognition, temporal keystroke cadence, spatial facial expressions, physical hand gestures, and acoustic vocal features.

---

## Core Concept & The Joke
The interface adopts an uncompromising, serious dark-theme defense terminal aesthetic (`RESTRICTED ACCESS // LEVEL-4 CLASSIFIED // DIRECTIVE 94-B`). 

The humor does **not** stem from silly meme styling, but emerges organically from the dramatic contrast:
1. The user must pass multi-factor AI evaluations (smiling while flashing peace signs, reciting movie/TV quotes, matching cognitive riddles).
2. Upon passing all four grueling protocols, the dramatic security clearance sequence reveals the "SUPeR SECret COde":
   ```python
   print("Hello world!")
   ```
3. The classified final transmission button directs the user to the classic Rickroll.

---

## System Architecture

```
Useless_Projects/
│
├── main.py                     # Entry point & system integrity checks
├── config.py                   # Central settings, thresholds, weights, styling, secret text
├── ui.py                       # Polished cyber/terminal GUI (Tkinter + Canvas + PIL)
├── cognition.py                # Protocol 01: Semantic free-response NLP evaluator
├── typing_analysis.py          # Protocol 02: Keystroke dynamics & behavioural telemetry
├── multimodal.py               # Protocol 03: Vision pipeline (Face, Hands, Pose similarity)
├── voice.py                    # Protocol 04: Speech-to-text & acoustic feature analysis
├── scoring.py                  # Gate verification engine & composite assessment
├── generate_starter_assets.py  # Local offline asset generator
├── assets/                     # Auto-discovered asset pools
│   ├── cognition/              # Jokes, riddles, semantic equivalence rules (.json)
│   ├── typing/                 # Long sentences & dialogue scripts (.txt)
│   ├── gestures/               # Target pose/expression images (.png, .jpg)
│   └── voice/                  # Reference audio recordings (.wav) & metadata (.json)
├── models/                     # Cached local model bundles (MediaPipe Tasks)
├── requirements.txt            # Python dependencies
└── README.md                   # System documentation & defense presentation
```

---

## Verification Protocols

### Protocol 01: Human Cognition Verification
- **Mechanism**: Free-response text input to jokes, riddles, and cultural prompts (no multiple-choice answers).
- **Evaluation Engine**:
  1. Concept group coverage (requires semantic keyword groups such as "cross" + "road" / "get across" for chicken joke).
  2. Character & word n-gram TF-IDF cosine similarity via `scikit-learn`.
  3. Token Jaccard overlap.
  4. Instant offline deterministic fallback.

### Protocol 02: Behavioural Typing Analysis
- **Mechanism**: Prompt requires exact reproduction of longer movie/TV dialogue quotes (e.g. Modern Family, Harry Potter, Avengers).
- **Telemetry Monitored**:
  - Inter-key intervals (IKI / flight time in ms)
  - Key hold duration (dwell time in ms)
  - Speed (WPM and Characters Per Second)
  - Cognitive pauses (> 380ms)
  - Error correction / backspace frequency
- **Bot Countermeasures**: Instant paste (<0.35s), uniform robotic timing ($\sigma < 6$ms), or zero-variance macros are immediately flagged.

### Protocol 03: Multimodal Expression + Gesture Verification
- **Mechanism**: Side-by-side display of tactical target specification card and live webcam feed with cyber HUD scanning reticles.
- **Vision Models**:
  - `FaceLandmarker`: Analyzes 52 facial blendshapes (mouth smile curvature, jaw openness, eyebrow elevation).
  - `HandLandmarker`: Evaluates 21 3D finger kinematics (peace/V-sign, thumbs-up, open palm, chin touch).
  - `PoseLandmarker`: Evaluates head/shoulder alignment and hand elevation.
- **Score Matrix**:
  - Face Compatibility %
  - Hand Compatibility %
  - Pose Compatibility %
  - Multimodal Response %

### Protocol 04: Voice Response Verification
- **Mechanism**: User plays a reference speech audio clip, then records their microphone response.
- **Acoustic Analysis**:
  - Speech-to-Text: Automated transcription via `SpeechRecognition`.
  - Semantic similarity: Compares transcription against reference phrase.
  - Pitch ($F_0$) Compatibility: Fundamental frequency estimation via autocorrelation (`scipy.signal`).
  - Duration/Timing Compatibility: Energy envelope speech segment matching.

---

## Final Clearance Assessment & Transmission
When all protocols independently pass, the system computes the weighted clearance score:
$$\text{Clearance Score} = (0.10 \times \text{Cognition}) + (0.20 \times \text{Typing}) + (0.30 \times \text{Multimodal}) + (0.20 \times \text{Voice}) + (0.20 \times \text{Behavioural})$$

- Displays Threat Level (`LOW`, `MODERATE`, `SUSPICIOUS`, `CRITICAL`).
- Reveals the classified intelligence:
  ```
  The SUPeR SECret COde is:

  print("Hello world!")
  ```
- Presents `[ ACCESS FINAL TRANSMISSION ]` which opens `https://www.youtube.com/watch?v=dQw4w9WgXcQ`.

---

## Strict Gate Failure Behavior
In strict accordance with the defense security model:
- **Independent Gates**: Protocols are evaluated sequentially. A failure in Protocol 01 stops execution immediately—Protocols 02, 03, and 04 are never executed.
- **No Score Leakage**: If any protocol fails, the user is immediately shown the dramatic failure screen:
  ```
  --------------------------------------------------
                ⚠ BOT DETECTED ⚠

        Unauthorized non-human entity detected.

               ACCESS TERMINATED
  --------------------------------------------------
  [ TERMINATE SESSION ]
  ```
- No hint, score percentage, or model identifier is revealed to prevent bot reverse-engineering.

---

## AI / ML & Computer Vision Techniques
- **MediaPipe Tasks (TFLite CPU)**: Real-time landmarker pipelines for face mesh, hands, and pose running at ~30 FPS on standard laptop hardware.
- **Scikit-Learn NLP**: Character & word n-gram TF-IDF vectorization with cosine similarity for semantic paraphrase tolerance.
- **Acoustic Signal Processing (`scipy`)**: Autocorrelation for harmonic pitch contour ($F_0$) tracking and RMS envelope extraction.
- **Keystroke Dynamics**: Temporal Gaussian variance anomaly scoring for biometric cadence validation.

---

## Installation & Execution

### 1. Prerequisites
- Windows 10/11
- Python 3.10+ (tested on Python 3.12)
- Working webcam and microphone (built-in laptop sensors supported)

### 2. Setup
Clone or navigate to the project directory and install dependencies:
```powershell
pip install -r requirements.txt
```

### 3. Run Application
```powershell
python main.py
```

---

## Asset Extensibility
Real user assets are automatically discovered and loaded from `assets/` and the project root:
- **Cognition**: `Jokes.txt` is automatically loaded and parsed into free-response challenges.
- **Typing**: `Dialouges.txt` is automatically parsed into behavioural typing quotes.
- **Gestures**: Real user reference images (`.jpeg`, `.jpg`, `.png`) are loaded via `gesture_targets.json` or auto-discovered.
- **Voice**: Real audio clips (`.mpeg`, `.mp3`, `.wav`, `.mp4`, `.m4a`, `.ogg`) are discovered automatically. `prompts.json` is optional.

---

## Privacy, Ethical Disclosures & Limitations
1. **Zero Persistent Storage**: All camera frames, microphone recordings, and keystrokes are processed strictly in volatile RAM and deleted immediately upon evaluation.
2. **No Identity Authentication**: The system evaluates *response congruence* (poses, cadence, phrases), never individual human identity or facial recognition databases.
3. **Prototype Limitations**: This software is engineered for educational demonstration and hackathon competition. It does not provide certified defense-grade authentication and should not be deployed in real-world critical infrastructure.

---

## Team Contributions
- **Multimodal Computer Vision**: MediaPipe Tasks integration, real-time tactical HUD reticle rendering, and hand/pose vector matching.
- **Audio & Speech Engineering**: Microphone streaming via `sounddevice`, autocorrelation pitch estimation, and STT transcript verification.
- **Cognitive NLP & Keystroke Dynamics**: Free-response semantic similarity engine, flight/dwell time telemetry tracking, and bot anomaly filters.
- **Cybersecurity Terminal UI**: Custom dark-mode Tkinter design, gate enforcement logic, and classified reveal sequence.
