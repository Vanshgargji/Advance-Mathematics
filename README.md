# Assignment – Learning Probability Density Function Parameters

## Objective

The objective of this assignment is to learn and understand probability density functions by transforming a real-world dataset feature and estimating the parameters of a given non-linear probability model.

---

## Dataset

* **Dataset:** India Air Quality Dataset (Kaggle)
* **Feature Used:** NO₂ concentration (x)
* Missing values were removed before processing.

---

## Step 1: Data Transformation

Each value of NO₂ (x) is transformed into a new variable (z) using the following transformation:

z = x + aᵣ sin(bᵣ x)

Where:

* aᵣ = 0.05 × (r mod 7)
* bᵣ = 0.3 × (r mod 5 + 1)
* r is the university roll number

r = 102303137
This step introduces non-linearity into the dataset.

---

## Step 2: Learning the Probability Density Function

The transformed variable z is modeled using the following probability density function:

p̂(z) = c · e^(−λ(z − μ)²)

The parameters are estimated using statistical techniques:

* **μ (mean):** Estimated as the mean of z
* **λ (spread parameter):** Computed from the variance of z using λ = 1 / (2σ²)
* **c (normalization constant):** Computed as c = √(λ / π)

The estimation is based on the similarity of the given function to a Gaussian distribution.

---

## Final Output

The final learned parameters are:
 
* Value of μ    : 25.80132545300301
* Value of λ    : 0.0014587890256159974
* Value of c    : 0.021548711532478945

---

## Learning Outcome

* Understanding non-linear data transformation
* Estimation of probability distribution parameters
* Practical application of statistical concepts such as mean and variance
