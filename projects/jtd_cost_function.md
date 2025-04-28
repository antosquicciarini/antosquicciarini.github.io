
# 📉 Jensen-Tsallis Divergence for Supervised Classification under Data Imbalance

In many real-world classification problems—such as in healthcare, fraud detection, or predictive maintenance—data imbalance is a major challenge. Conventional loss functions like **Categorical Cross Entropy (CE)** can lead to models that overfit to majority classes and produce **overconfident predictions** that fail to generalize.

In this work, we propose the **Jensen-Tsallis Divergence (JTD)** as a **new loss function** for deep learning models trained on imbalanced datasets. It generalizes the well-known **Jensen-Shannon Divergence (JSD)** by incorporating **Tsallis entropy**, introducing a tunable parameter `q` that directly influences regularization strength.

---

## 🧠 Why Jensen-Tsallis?

- **Built-in regularization**: JTD discourages overconfident output distributions, leading to better generalization.
- **Tunable flexibility**: The `q` parameter controls how strongly the model penalizes high-confidence predictions.
- **Superior performance**: JTD consistently outperforms CE, JSD, and focal loss in tests with artificially imbalanced datasets (MNIST, CIFAR-10, SVHN, Fashion-MNIST).

---

## 🔍 Theoretical Insight

We demonstrate that JTD introduces an intrinsic **confidence penalty** on output predictions. By adjusting `q`, we control how conservative the model becomes, thus reducing overfitting.

---

## 🔬 Results: Accuracy & Regularization Effect

## 🔄 Learning Curve Comparison

![Accuracy Learning Curves](/assets/img/fig_1.png)  
*Test vs train accuracy using CE, JSD, and JTD with various `q`. JTD improves generalization without overfitting.*

## 🎯 Regularization Term Behavior

![Regularization Effect](/assets/img/fig_3.png)  
*Behavior of the JTD's regularization term as a function of model confidence. Larger `q` values shift the regularization curve and enhance robustness.*

---

## 📄 Related Preprint

**Squicciarini, A., Trigano, T., Luengo, D.**  
*Jensen-Tsallis Divergence for Supervised Classification under Data Imbalance*, submitted to Springer - Machine Learning (ECLM 2025).  
🔗 [Project Repository](https://github.com/antosquicciarini/Jensen_Tsallis_Divergence_for_Supervised_Classification_under_Data_Imbalance)

---

[⬅️ Back to Projects](/projects)
