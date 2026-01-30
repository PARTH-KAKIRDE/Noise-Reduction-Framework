# Noise-Reduction-Framework

This repository presents a **Digital Signal Processing (DSP) project** focused on analyzing and comparing **Windowed FIR Filtering** and **Matched Filtering** for noise reduction and signal detection in noisy environments.

The project emphasizes **engineering realism**: understanding *why* complete noise removal is impossible in practice, and *how* different filtering approaches optimize Signal-to-Noise Ratio (SNR) under different assumptions.

---

## 📌 Project Motivation

In real-world systems, signals are often corrupted by:
- Additive White Gaussian Noise (AWGN)
- Impulsive noise
- Spectral overlap between signal and noise

This project was undertaken to:
- Study the **limitations of conventional FIR filters**
- Understand why **matched filters achieve superior SNR**
- Bridge the gap between **theoretical DSP concepts** and **practical implementation**

---

## 🧠 Core Concepts Explored

- Windowed FIR filter design
- Frequency-domain vs time-domain filtering
- Spectral overlap and in-band noise
- Impulse noise behavior
- Matched filter theory
- Correlation-based detection
- SNR calculation and interpretation
- Group delay vs distortion
- Practical limitations of “complete” noise removal

---

## 🔧 Methods Implemented

### 1️⃣ Windowed FIR Filtering
- Designed FIR filters using windowing techniques (Rectangular, Hamming, Hanning and Blackman)
- Studied:
  - Main-lobe width vs sidelobe attenuation
  - Effect on Gaussian and impulsive noise
- Observed that:
  - FIR filters remove **out-of-band noise only**
  - In-band noise cannot be eliminated without signal distortion

### 2️⃣ Matched Filtering
- Implemented a matched filter using:
  \[
  h[n] = s^*[N-1-n]
  \]
- Performed time-domain correlation for signal detection
- Demonstrated:
  - Coherent integration of signal energy
  - Incoherent averaging of noise
  - Significant SNR improvement

---

## 📊 Key Observations

| Aspect | FIR Windowed Filter | Matched Filter |
|------|--------------------|----------------|
| Domain | Frequency | Time |
| Signal knowledge | Not required | Required |
 Primary objective | Attenuation of out-of-band components | Maximization of output SNR |
| Noise removed | Out-of-band only | Uncorrelated noise |
| In-band noise | ❌ Not removable | ✅ Suppressed |
| SNR optimal | ❌ No | ✅ Yes |
| Output characteristic | Smoothed version of input signal | Sharp detection peak |
| Typical applications | Signal conditioning and smoothing | Detection and synchronization |

---

## ⚠️ Important Engineering Insights

- **No practical filter can completely remove noise** when signal and noise overlap in frequency or time.
- Windowing improves realism but does **not** create ideal filters.
- Matched filters **do not clean the signal** — they **concentrate signal energy** at a single detection peak.
- Large output amplitude does **not** imply better performance; **SNR is the true metric**.

> *“A windowed FIR filter removes frequencies.  
A matched filter recognizes patterns.”*

---

## 🧪 Normalization Study (Critical Result)

Two matched filter normalization approaches were tested:

| Case | Result | Verdict |
|----|------|--------|
| Sum normalization | High SNR, lower amplitude | ✅ Correct |
| Norm normalization | Large amplitude, poor SNR | ❌ Incorrect |

Matched filters are designed to **maximize SNR**, not amplitude.

---

## 🛠 Tools & Technologies

- MATLAB / Octave
- Digital Signal Processing Toolbox
- Git & GitHub for version control

---

## 🚀 Applications

The techniques studied here are directly applicable to:
- Communication systems
- Radar and sonar
- Biomedical signal processing
- Particle detectors
- Embedded DSP systems

---
