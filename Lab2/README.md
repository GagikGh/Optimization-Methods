# Dichotomy Method (Bisection Search for Optimization)

This implementation demonstrates the **Dichotomy Method** for finding the minimum of a unimodal function on a closed interval.

---

## Theoretical Breakdown

The Dichotomy Method is an interval reduction technique that iteratively narrows the search range.

- **Objective:** Find the minimum of \( f(x) \) on \([a, b]\)

- At each step, two symmetric points around the center are evaluated:

\[
x_1 = \frac{a + b}{2} - \delta
\]
\[
x_2 = \frac{a + b}{2} + \delta
\]

- **Decision rule:**

\[
\text{If } f(x_1) < f(x_2) \Rightarrow b = x_2
\]
\[
\text{Else } a = x_1
\]

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
- **Delta:** \( \delta = 0.125 \)

---

## Sample Iteration Table

| Step | a | b | b-a | x₁ | x₂ |
|------|----|----|------|------|------|
| 1 | 0.5000 | 3.0000 | 2.5000 | ... | ... |
| 2 | ... | ... | ... | ... | ... |
| ... | ... | ... | ... | ... | ... |

---

## Result

After iterations, the algorithm converges to:

\[
x^* \approx 1.41
\]

This is the approximate point where the function reaches its minimum.

---

## Implementation Details

- Uses two test points \(x_1, x_2\) at each iteration
- Reduces the interval size step-by-step
- Stores evaluated points for visualization
- Prints a detailed step-by-step table

---

## Visualization

The script generates a plot showing:

- Function curve
- Evaluated points (blue)
- Final minimum (red star)
- Initial interval boundaries

---

## How to Run

```bash
python your_script.py
