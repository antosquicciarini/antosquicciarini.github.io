
# ⏱️ Multiscale Time-Series Feature Extraction Using Entropic & Informational Functionals

This project proposes a general-purpose methodology to transform time series into interpretable sequences of **entropic and information-theoretic features**. The method is designed for **anomaly detection** and **time-series characterization** in domains such as fault monitoring, EEG seizure detection, and more.

The approach combines:
- **Multiscale overlapping windows**
- **Non-parametric Kernel Density Estimation (KDE)**
- **Adaptive bandwidth optimization using Jensen–Shannon Divergence (JSD)**
- **A library of continuous entropic and informational measures** (e.g., Shannon, Tsallis, Rényi, Fisher Information)

---

## 🧠 Why This Matters

Entropy and information measures provide a **rich, continuous description of signal complexity**, uncertainty, and structure — essential for detecting subtle or time-localized anomalies. Our method optimizes the transformation parameters and builds a **scale-adaptive, windowed representation** of the signal.

---

## 📐 Method Overview

The methodology applies **KDE** to windowed segments of the time series at multiple scales, producing a sequence of PDFs. Then, various **entropy-based features** are computed for each PDF. The bandwidth is optimized offline using **JSD**, ensuring minimal bias and variance.

![Method diagram](./assets/img/fig_1_art_1.png)  
*A modular pipeline applying KDE, JSD-based optimization, and entropic feature extraction over multiscale overlapping windows.*

---

## 🔬 Experimental Results

## 🧪 Synthetic Signal with Contextual Anomaly

We generate a synthetic signal that transitions from a normal to an anomalous regime using added frequency components. The anomaly is detected by shifts in entropy and information content.

![Synthetic anomaly signal](./assets/img/fig_2_art_1.png)  
*A designed synthetic signal where harmonic content shifts during the anomaly window.*

## 🎯 Multiscale Feature Plots

We visualize the extracted features across different window sizes and time indices.

![Entropic time-series curves](./assets/img/fig_3_art_1.png)  
*Multiscale entropy and Fisher information curves over time. Anomalies manifest as sudden drops in information and spikes in entropy.*

---

## 🧠 Real Application: EEG Seizure Detection

The methodology was applied to **scalp EEG signals** from the CHB-MIT database. The results show that seizures trigger consistent, multi-scale changes in the extracted features.

![EEG preictal signals](./assets/img/fig_4_art_1.png)  
*EEG signal before seizure: healthy baseline.*

![EEG entropy behavior](./assets/img/fig_6_art_1.png)  
*Entropy and information functionals capturing the seizure onset across scales.*

---

## 📈 Final Validation

To ensure interpretability, we also plotted the PDFs generated at different scales and bandwidths to visualize how KDE transforms signal windows before entropy evaluation.

![PDF Grid by scale and h](./assets/img/fig_9_art_1.png)  
*Grid of PDFs for anomaly and normal signals across scales and bandwidths, showing clear contrast.*

---

## 📄 Related Publication

**Squicciarini, A., Valero Toranzo, E., Zarzo, A.**  
*A Time-Series Feature-Extraction Methodology Based on Multiscale Overlapping Windows, Adaptive KDE, and Continuous Entropic and Information Functionals*,  
Mathematics, vol. 12, 2396, 2024.  
📎 [https://doi.org/10.3390/math12152396](https://doi.org/10.3390/math12152396)  
🔬 [Project Code on GitHub](https://github.com/antosquicciarini/Information_Measurement)
