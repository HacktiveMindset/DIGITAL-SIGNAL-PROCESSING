
# Unit III: z-Transform and Analysis of LTI Systems

## Introduction to z-Transform
The z-transform is a powerful mathematical tool used in digital signal processing (DSP) for analyzing discrete-time signals and systems. It transforms discrete-time signals into a complex frequency domain representation.

### Definition of z-Transform
The z-transform of a discrete-time signal \( x[n] \) is defined as:

\[
X(z) = \sum_{n=-\infty}^{\infty} x[n] z^{-n}
\]

Where:
- \( X(z) \) is the z-transform of the signal.
- \( z \) is a complex variable, \( z = re^{j\omega} \), where \( r \) is the radius and \( \omega \) is the angular frequency.

### Region of Convergence (ROC)
The region of convergence for the z-transform is the range of \( z \) values for which the z-transform converges. The ROC is crucial for determining the stability and causality of the system.

## Properties of z-Transform
1. **Linearity**: If \( x_1[n] \) and \( x_2[n] \) are two discrete-time signals with z-transforms \( X_1(z) \) and \( X_2(z) \), then:
   \[
   a_1 x_1[n] + a_2 x_2[n] \rightarrow a_1 X_1(z) + a_2 X_2(z)
   \]

2. **Time Shifting**: If \( x[n] \) has a z-transform \( X(z) \), then:
   - Right shift: \( x[n-k] \rightarrow z^{-k} X(z) \)
   - Left shift: \( x[n+k] \rightarrow z^{k} X(z) \)

3. **Scaling in z-domain**: If \( x[n] \) has a z-transform \( X(z) \), then:
   \[
   a^n x[n] \rightarrow X(az)
   \]

4. **Convolution**: If \( x[n] \) and \( h[n] \) have z-transforms \( X(z) \) and \( H(z) \), then the convolution \( y[n] = x[n] * h[n] \) has a z-transform given by:
   \[
   Y(z) = X(z) H(z)
   \]

5. **Initial and Final Value Theorems**:
   - Initial value theorem: \( x[0] = \lim_{z \to \infty} X(z) \)
   - Final value theorem: \( x[\infty] = \lim_{z \to 1} (z-1) X(z) \)

## Inverse z-Transform
The inverse z-transform is used to recover the original discrete-time signal from its z-transform. Several methods can be used, including:
1. **Power Series Expansion**: Expanding \( X(z) \) in a power series and collecting terms.
2. **Partial Fraction Expansion**: For rational z-transforms, decompose \( X(z) \) into simpler fractions and apply known inverse z-transforms.

## Analysis of Linear Time-Invariant (LTI) Systems in z-Domain
### System Function
The system function \( H(z) \) of an LTI system relates the input signal to the output signal in the z-domain. It is defined as:
\[
H(z) = \frac{Y(z)}{X(z)}
\]

### Stability
A discrete-time LTI system is stable if the ROC of its z-transform includes the unit circle \( |z| = 1 \). For stability, all poles of \( H(z) \) must lie inside the unit circle.

### Causality
A system is causal if its output at any time depends only on current and past input values. For a causal system, the ROC extends outward from the outermost pole.

### Pole-Zero Representation
The pole-zero plot is a graphical representation of the poles and zeros of the system function \( H(z) \). It provides insight into the system's stability and frequency response.

## Transient and Steady-State Responses
The total response of an LTI system can be decomposed into transient and steady-state responses:
- **Transient Response**: The system's response to initial conditions and inputs, typically decaying over time.
- **Steady-State Response**: The system's behavior after transients have died out, determined by the input signal and system characteristics.

## Causality and Stability Conditions
1. **Causality**: For a system to be causal, its impulse response must be zero for all \( n < 0 \).
2. **Stability**: The system is stable if all poles of the system function \( H(z) \) lie within the unit circle.

### Pole-Zero Cancellation
Pole-zero cancellation occurs when a pole of the system function \( H(z) \) coincides with a zero. While it can simplify the analysis, it may lead to instability if not handled properly.

## The Schur-Cohn Stability Test
The Schur-Cohn stability test is a criterion to determine the stability of a discrete-time system based on the locations of its poles. It states that if the magnitudes of the poles are less than one, the system is stable.

## Conclusion
Understanding the z-transform and its properties is essential for analyzing discrete-time LTI systems. The stability and causality of these systems play a critical role in designing effective digital signal processing applications.

---
