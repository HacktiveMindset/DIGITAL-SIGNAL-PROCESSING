
# Unit II: Analysis of Discrete-Time LTI Systems

## Overview
This unit focuses on the analysis of discrete-time linear time-invariant (LTI) systems, including the convolution sum, properties of convolution, and stability analysis.

### Key Concepts
1. **Convolution Sum**: The convolution sum is a fundamental operation in LTI systems that determines the output signal from the input signal and the system's impulse response.
   - The convolution of two sequences \( x[n] \) and \( h[n] \) is defined as:
   \[
   y[n] = (x * h)[n] = \sum_{k=-\infty}^{\infty} x[k] h[n - k]
   \]

2. **Properties of Convolution**:
   - **Commutative Property**: \( x * h = h * x \)
   - **Associative Property**: \( x * (h * g) = (x * h) * g \)
   - **Distributive Property**: \( x * (h + g) = x * h + x * g \)

3. **Analysis of Causal LTI Systems**:
   - A causal system's output depends only on current and past inputs.
   - The impulse response \( h[n] \) of a causal LTI system is zero for \( n < 0 \).
   - The stability of an LTI system can be analyzed by examining its impulse response.

4. **Stability of LTI Systems**:
   - An LTI system is stable if its output is bounded for any bounded input (BIBO Stability).
   - For a causal LTI system, the impulse response must be absolutely summable:
   \[
   \sum_{n=-\infty}^{\infty} |h[n]| < \infty
   \]

5. **Step Response of LTI Systems**:
   - The step response \( s[n] \) is the output of the system when the input is a unit step function \( u[n] \).
   - The step response can be derived from the impulse response:
   \[
   s[n] = (h * u)[n] = \sum_{k=-\infty}^{n} h[k]
   \]

6. **Difference Equation**:
   - Discrete-time systems can be described by difference equations. For example:
   \[
   a_0 y[n] + a_1 y[n-1] + \ldots + a_m y[n-m] = b_0 x[n] + b_1 x[n-1] + \ldots + b_n x[n-n]
   \]
   - Recursive and non-recursive systems can be analyzed using these equations.

7. **Impulse Response of LTI Recursive Systems**:
   - Recursive systems use past outputs in their current output calculation.
   - The impulse response of such systems can be derived using difference equations.

8. **Correlation of Discrete-Time Signals**:
   - Correlation measures the similarity between two signals as a function of time-lag.
   - The cross-correlation of signals \( x[n] \) and \( y[n] \) is given by:
   \[
   R_{xy}[m] = \sum_{n=-\infty}^{\infty} x[n] y[n+m]
   \]

## Summary
- This unit covers the essential concepts of LTI systems, focusing on convolution, stability, and difference equations.
- Understanding these principles is crucial for further analysis and design of digital systems.

## References
- Proakis, J. G., & Manolakis, D. G. (2007). *Digital Signal Processing: Principles, Algorithms, and Applications*. Pearson Education.
- Mitra, S. K. (2006). *Digital Signal Processing: A Computer-Based Approach*. McGraw Hill.
