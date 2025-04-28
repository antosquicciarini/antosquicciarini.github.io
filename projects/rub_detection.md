
# 🔧 Rub Detection in Aeroderivative Gas Turbines

**Rotor–stator rub** is a common but critical malfunction in turbomachinery, particularly in aero-derivative gas turbines where design constraints limit sensor placement. Due to compact geometries and the use of ball bearings instead of hydrodynamic ones, **proximity sensors are impractical**, and vibration must be monitored indirectly via **accelerometers on the casing**.

These signals are affected by high levels of noise, making **rub detection in early stages difficult** with traditional frequency-domain techniques such as Fourier analysis.

---

## 🧠 Our Deep Learning-Based Solution

In our work, we present a novel **Intelligent Fault Detection (IFD)** system using **deep neural networks (DNNs)** trained with **synthetic vibration data** from a calibrated **finite element (FE) model** of a rotating machine.

This data-driven approach avoids the need to collect dangerous real-world fault data and opens the door to safe, scalable training of deep models. The key features of our methodology include:

- **Synthetic Dataset Creation**: An FE model simulates rub events of varying intensity and frequency (e.g., light rub: 1×; heavy rub: ½×).
- **Transfer Learning**: The DNN trained on simulated data generalizes well to **real experimental signals**, achieving up to **91% G-Mean** and **~86% accuracy**.
- **Data Preprocessing**: Accelerometer signals are resampled, windowed, and transformed via **FFT** to emphasize relevant harmonic content.
- **Regularization & Optimization**: Grid search was used to identify optimal architectures with **L1/L2 regularization**, improving generalization.

---

## 🖼️ Simulation and Experimental Setup

## 🧩 Finite Element Model Simulation
Here are two visualizations from the FE model used to generate synthetic training data for rub scenarios:

![FE model example 1](./assets/img/FE_model_1.png)  
*Finite Element model simulating single-point rub in high-speed shaft.*

![FE model example 2](./assets/img/FE_model_2.png)  
*FE mesh used to simulate both light and heavy rub events.*

## 🧪 Real Experimental Setup

![Real experimental rig](./assets/img/Real_exp.png)  
*Experimental test bench with mounted accelerometers and proximity sensors used to validate model predictions.*

---

## 📊 Results and Transfer Learning Performance

We tested multiple DNN architectures with different regularization techniques (L1, L2, ElasticNet) to study how they affect generalization from synthetic to real-world signals.

## 📋 Result Summary

![Result Table](./assets/img/Result_table.png)  
*Performance of different DNN models on real test signals after training on synthetic data.*

## 📈 AUC/ROC Curves Comparison

![AUC ROC Curves](./assets/img/AUC_ROC_curves.png)  
*Comparison of AUC-ROC performance across models with varying regularization. Shows impact of regularization on robustness and transfer learning accuracy.*

---

## 📄 Related Publication

**Squicciarini, A., Zarzo, A., González-Guillén, C.E., Muñoz-Guijosa, J.M.**  
*Application of Deep Neural Networks for Automatic Rub Detection in Aero-Derivative Gas Turbines*,  
Advanced Engineering Informatics, vol. 62, 2024, Art. no. 102607.  
📎 [DOI: 10.1016/j.aei.2024.102607](https://doi.org/10.1016/j.aei.2024.102607)
