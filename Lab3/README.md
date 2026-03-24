# Golden Section Search Method

This implementation demonstrates the **Golden Section Search Method** for finding the minimum of a unimodal function on a closed interval.

---

## Theoretical Breakdown

The Golden Section Method is an efficient interval reduction technique that minimizes function evaluations by reusing previously computed points.

- **Objective:** Find the minimum of \( f(x) \) on \([a, b]\)

- **Golden ratio constant:**
\[
t \approx 0.618
\]

- **Internal points:**
\[
x_1 = b - t(b - a)
\]
\[
x_2 = a + t(b - a)
\]

- **Decision rule:**

\[
\text{If } f(x_1) \leq f(x_2) \Rightarrow b = x_2
\]
\[
\text{Else } a = x_1
\]

- One of the points is reused at each iteration, reducing computations.

- **Stopping condition:**
\[
b - a < \varepsilon
\]

- **Final approximation:**
\[
x^* = \frac{a + b}{2}
\]

---

## Numerical Example

- **Function:**  
\[
f(x) = x^2 - 4\ln(x) - 2
\]

- **Interval:** \([0.5, 3]\)  
- **Precision:** \( \varepsilon = 0.5 \)  
- **Constant:** \( t = 0.618 \)

---

## Sample Iteration Table

| Step | a | b | b-a | x₁ | x₂ |
|------|----|----|------|------|------|
| 1 | 0.5000 | 3.0000 | 2.5000 | ... | ... |
| 2 | ... | ... | ... | ... | ... |
| ... | ... | ... | ... | ... | ... |

---

## Result

After convergence, the approximate minimum is:

\[
x^* \approx 1.41
\]

\[
f(x^*) \approx -0.62
\]

---

## Implementation Details

- Reuses one function evaluation per iteration
- Reduces interval using golden ratio proportions
- Stores evaluated points for visualization
- Prints step-by-step progress table

---

## Visualization

The script generates a plot showing:

- Function curve
- Evaluated points (blue)
- Final minimum (red star)

---

## How to Run

```bash
python your_script.py
