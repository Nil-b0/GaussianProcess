# 🌌 Gaussian Processes: A Gateway to Uncertainty

![GP Banner](https://upload.wikimedia.org/wikipedia/commons/thumb/5/5e/Gaussian_process_sample_functions.svg/1200px-Gaussian_process_sample_functions.svg.png)

---

> “A Gaussian Process is not just a method — it’s a **philosophy of inference**.”  
> *— Every Bayesian Ever*

---

## 🧠 What is a Gaussian Process?

A **Gaussian Process (GP)** is a non-parametric Bayesian model used to predict distributions over functions. Think of it as:

- A **distribution over functions** instead of points
- A way to model **uncertainty and correlation**
- Incredibly useful for **interpolation, regression, and scientific inference**

---

## 📌 Why It Matters in Cosmology

- 🌌 Fits sparse or noisy astronomical data  
- 📈 Encodes prior structure like smoothness or periodicity  
- 🔮 Gives **error bars** on function predictions (not just numbers)

---

## 🔗 References & Resources

- [📘 My Jupyter Notebook on GPs](notebooks/gaussian-processes.ipynb)
- [📚 Rasmussen & Williams (2006) — *The GP Bible*](http://www.gaussianprocess.org/gpml/)
- [🛠️ sklearn GaussianProcessRegressor Docs](https://scikit-learn.org/stable/modules/gaussian_process.html)
- [🎥 Gaussian Processes Explained Visually (YouTube)](https://www.youtube.com/watch?v=4vGiHC35j9s)
- [🌐 My GitHub Repository on GPs](https://github.com/Nil-b0/gaussian-process-site)

---

## 🔍 Peek Preview

```python
from sklearn.gaussian_process import GaussianProcessRegressor
from sklearn.gaussian_process.kernels import RBF

gp = GaussianProcessRegressor(kernel=RBF(length_scale=1.0))
gp.fit(X_train, y_train)
y_pred, y_std = gp.predict(X_test, return_std=True)
