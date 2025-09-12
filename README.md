# 📘 CS5710 Machine Learning — Homework 1

**University:** University of Central Missouri  
**Department:** Computer Science & Cybersecurity  
**Course:** CS5710 Machine Learning (Fall 2025)  

---

## 👩‍🎓 Student Information
- **Name:** Ashmitha Kumbham  
- **Student ID:** 700773518  
- **GitHub Repo:** [PASTE REPO URL HERE]  

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

Print model parameters from both Normal Equation and Gradient Descent.

Save the figures (fig_data_and_fits.png, fig_loss_curve.png) in the repo directory.

📝 Assignment Questions & Solutions
Q1 — Function Approximation by Hand
Dataset: (1,1), (2,2), (3,2), (4,5)
Model: 
𝑦
^
=
𝜃
0
+
𝜃
1
𝑥
y
^
​
 =θ 
0
​
 +θ 
1
​
 x

Trial (1,0) → MSE = 4.5

Trial (0.5,1) → MSE = 0.75

✅ Better fit: (0.5,1) due to lower error.

Q2 — Random Guessing Practice
Loss function:

𝐽
(
𝜃
0
,
𝜃
1
)
=
8
(
𝜃
0
−
0.3
)
2
+
4
(
𝜃
1
−
0.7
)
2
J(θ 
0
​
 ,θ 
1
​
 )=8(θ 
0
​
 −0.3) 
2
 +4(θ 
1
​
 −0.7) 
2
 
At (0.1,0.2): 
𝐽
=
1.32
J=1.32

At (0.5,0.9): 
𝐽
=
0.48
J=0.48

✅ Closer point: (0.5,0.9)

⚠️ Random guessing is inefficient → does not use gradient information.

Q3 — First Gradient Descent Iteration
Dataset: (1,3), (2,4), (3,6), (4,5)
Start: 
𝜃
(
0
)
=
(
0
,
0
)
θ 
(0)
 =(0,0), learning rate 
𝛼
=
0.01
α=0.01

Gradient: (-9.0, -24.5)

Update: 
𝜃
(
1
)
=
(
0.09
,
0.245
)
θ 
(1)
 =(0.09,0.245)

𝐽
(
𝜃
(
0
)
)
=
21.5
J(θ 
(0)
 )=21.5

𝐽
(
𝜃
(
1
)
)
≈
15.256
J(θ 
(1)
 )≈15.256

✅ Loss decreases → gradient descent works.

Q4 — Random Guessing vs Gradient Descent
Dataset: (1,2), (2,2), (3,4), (4,6)

Random guess (0.2,0.5) → 
𝐽
≈
5.515
J≈5.515

Random guess (0.9,0.1) → 
𝐽
≈
7.935
J≈7.935

GD (1 step, 
𝛼
=
0.01
α=0.01) → 
𝐽
≈
10.509
J≈10.509

⚠️ Random guess can be better at the start.
✅ GD improves systematically after many steps.

Q5 — Underfitting
Symptoms: High train error + high test error.

Cause: Model too simple.

Fixes: Add complexity, improve features, reduce regularization.

Q6 — Comparing Models
Model A (low train error, high test error): Overfitting

Fix: Regularization, more data, simplify model, early stopping

Model B (high train & test error): Underfitting

Fix: More complexity, better features, reduce regularization

Q7 — Linear Regression Programming
Task: Generate dataset from 
𝑦
=
3
+
4
𝑥
+
𝜖
y=3+4x+ϵ, fit using:

Closed-form solution (Normal Equation)

Gradient Descent

Parameters:

Learning rate: 0.05

Iterations: 1000

Loss: Mean Squared Error (MSE)

Sample Output:

csharp
Copy code
[Normal Equation] intercept = 2.97, slope = 4.01
[Gradient Descent] intercept = 2.96, slope = 4.00
Final MSE (GD): 1.01
✅ Both methods converge to nearly the same solution.

📊 Figures
fig_data_and_fits.png → Dataset + fitted lines

fig_loss_curve.png → GD loss vs iterations

✅ Notes
Implemented from scratch (no scikit-learn LinearRegression).

Both closed-form and gradient descent are coded manually.

Figures auto-generated when script runs.

👉 Would you like me to also include **your Q1–Q6 full written answers as a separate PDF file**
