# Method of Alternatives (Uniform Search)

This implementation demonstrates the **Uniform Search Method (Method of Alternatives)** for finding the minimum of a unimodal function using a fixed step.

---

## Theoretical Breakdown

The method evaluates the function at equally spaced points over a given interval.

- **Objective:** Find the minimum of \( f(x) \)

- **Step size:**
  \[
  \delta = \text{given step}
  \]

- **Points generation:**
  \[
  x_k = a + k \cdot \delta
  \]

- **Selection rule:**
  \[
  f(x^*) = \min f(x_k)
  \]

- **Stopping condition:**
  \[
  x_k \leq b
  \]

- **Error estimate:**
  \[
  \varepsilon \approx \delta
  \]

---

## Numerical Example

- **Function:**  
  \[
  f(x) = x^2 - 4\ln(x) - 2
  \]

- **Interval:** \([0.5, 3]\)  
- **Step size:** \( \delta = 0.125 \)

### Sample Output

| Step | x | f(x) |
|------|----|------|
| 0 | 0.5000 | 2.7726 |
| 1 | 0.6250 | 1.6620 |
| 2 | 0.7500 | 0.9001 |
| ... | ... | ... |

**Result:**  
The approximate minimum is found at:

\[
x^* \approx 1.41
\]

\[
f(x^*) \approx -0.62
\]

*(Exact values may slightly vary depending on step size)*

---

## Implementation Details

- Iterates from **a to b** with fixed step \( \delta \)
- Stores all computed values for visualization
- Tracks minimum dynamically
- Prints step-by-step table of values

---

## Visualization

The script generates a plot showing:

- The function curve
- Sampled points (red)
- Estimated minimum (green)

---

## How to Run

```bash
python your_script.py
