# 📘 CS5710 Machine Learning — Homework 1

**University:** University of Central Missouri  
**Department:** Computer Science & Cybersecurity  
**Course:** CS5710 Machine Learning (Fall 2025)  

---

## 👩‍🎓 Student Information
- **Name:** Ashmitha Kumbham  
- **Student ID:** 700773518  

---

## 📂 Repository Structure

- `gradient_descent_linear_regression.py` — Source code for **Q7** (Normal Equation vs. Gradient Descent)  
- `fig_data_and_fits.png` — Plot of dataset with fitted regression lines  
- `fig_loss_curve.png` — Gradient Descent loss curve visualization  
- `requirements.txt` — Python dependencies  

---

## ⚙️ Setup & Execution

### 1. Install dependencies
```bash
pip install -r requirements.txt
2. Run the program
bash
Copy code
python gradient_descent_linear_regression.py
This will:

Print model parameters from both Normal Equation and Gradient Descent

Save the figures (fig_data_and_fits.png, fig_loss_curve.png) in the repo directory

📝 Assignment Questions & Solutions
Q1 — Function Approximation by Hand
Dataset: (1,1), (2,2), (3,2), (4,5)
Model: ŷ = θ₀ + θ₁x

Trial (θ₀, θ₁) = (1, 0) → MSE = 4.5

Trial (θ₀, θ₁) = (0.5, 1) → MSE = 0.75

✅ Better fit: (0.5, 1) due to lower error

Q2 — Random Guessing Practice
Loss function:

J(θ₀, θ₁) = 8(θ₀ − 0.3)² + 4(θ₁ − 0.7)²

At (0.1, 0.2): J = 1.32

At (0.5, 0.9): J = 0.48

✅ Closer point: (0.5, 0.9)

⚠️ Random guessing is inefficient → does not use slope/gradient information

Q3 — First Gradient Descent Iteration
Dataset: (1,3), (2,4), (3,6), (4,5)
Start: θ⁽⁰⁾ = (0, 0), learning rate α = 0.01

Residual sum = 18, weighted residual sum = 49

Gradient = (−9.0, −24.5)

Update: θ⁽¹⁾ = (0.09, 0.245)

Loss values:

J(θ⁽⁰⁾) = 21.5

J(θ⁽¹⁾) ≈ 15.256

✅ Loss decreases → gradient descent is working

Q4 — Random Guessing vs Gradient Descent
Dataset: (1,2), (2,2), (3,4), (4,6)

Random guess (0.2, 0.5) → J ≈ 5.515

Random guess (0.9, 0.1) → J ≈ 7.935

GD (1 step, α = 0.01) → J ≈ 10.509

⚠️ Random guess can be better at the very start
✅ GD improves systematically with more steps

Q5 — Underfitting
Symptoms: High training error + high test error

Cause: Model too simple

Fixes: Increase complexity, add features, reduce regularization

Q6 — Comparing Models
Model A (low training error, high test error): Overfitting

Fix: Regularization, more data, simplify model, early stopping

Model B (high training & test error): Underfitting

Fix: Add complexity, improve features, reduce regularization

Q7 — Linear Regression Programming
Task: Generate dataset from y = 3 + 4x + ε, fit using:

Closed-form solution (Normal Equation)

Gradient Descent

Parameters:

Learning rate: α = 0.05

Iterations: 1000

Loss: Mean Squared Error (MSE)

Sample Output:

csharp
Copy code
[Normal Equation] intercept = 2.97, slope = 4.01
[Gradient Descent] intercept = 2.96, slope = 4.00
Final MSE (GD): 1.01
✅ Both methods converge to nearly the same solution

📊 Figures
fig_data_and_fits.png → Dataset + fitted regression lines

fig_loss_curve.png → Loss vs iterations (GD)

✅ Notes
Implemented from scratch (no scikit-learn LinearRegression)

Both closed-form and gradient descent are coded manually

Figures auto-generated when script runs

yaml
Copy code

---
