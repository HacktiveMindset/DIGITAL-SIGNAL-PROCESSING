# Unit IV: Fourier Transforms, the DFT, and FFT

## 1. Introduction to Fourier Transform
- The Fourier Transform (FT) is a mathematical transformation used to analyze the frequencies contained in a signal.
- It converts a time-domain signal into its frequency-domain representation.

### Definition
- For a continuous time signal \( x(t) \), the Fourier Transform \( X(f) \) is defined as:
  \[
  X(f) = \int_{-\infty}^{\infty} x(t) e^{-j2\pi ft} dt
  \]

### Inverse Fourier Transform
- The inverse transform is given by:
  \[
  x(t) = \int_{-\infty}^{\infty} X(f) e^{j2\pi ft} df
  \]

### Properties of Fourier Transform
1. **Linearity**: \( a x_1(t) + b x_2(t) \) transforms to \( a X_1(f) + b X_2(f) \)
2. **Time Shifting**: \( x(t - t_0) \) transforms to \( X(f) e^{-j2\pi f t_0} \)
3. **Frequency Shifting**: \( e^{j2\pi f_0 t} x(t) \) transforms to \( X(f - f_0) \)
4. **Conjugate Symmetry**: If \( x(t) \) is real, then \( X(f) \) is conjugate symmetric.
5. **Parseval’s Theorem**: Energy in time domain equals energy in frequency domain.

## 2. Relation with z-Transform
- The z-transform is a generalization of the Fourier Transform, which is useful for discrete-time signals.
- The z-transform is defined as:
  \[
  X(z) = \sum_{n=-\infty}^{\infty} x[n] z^{-n}
  \]
- When \( z = e^{j\omega} \), the z-transform reduces to the discrete-time Fourier Transform (DTFT).

## 3. Discrete Fourier Transform (DFT)
- The DFT is used for finite-duration sequences and is defined for a sequence of \( N \) samples \( x[n] \):
  \[
  X[k] = \sum_{n=0}^{N-1} x[n] e^{-j\frac{2\pi}{N}kn}
  \]
  for \( k = 0, 1, \ldots, N-1 \).

### Properties of DFT
1. **Periodicity**: \( X[k] \) is periodic with period \( N \).
2. **Linearity**: \( a x_1[n] + b x_2[n] \) transforms to \( a X_1[k] + b X_2[k] \).
3. **Conjugate Symmetry**: If \( x[n] \) is real, then \( X[N-k] = \overline{X[k]} \).
4. **Circular Convolution**: \( y[n] = x[n] * h[n] \) corresponds to multiplication in the DFT domain: \( Y[k] = X[k] H[k] \).

## 4. Fast Fourier Transform (FFT)
- The FFT is an efficient algorithm to compute the DFT, reducing the computational complexity from \( O(N^2) \) to \( O(N \log N) \).
- Two common algorithms for FFT are:
  - **Radix-2 FFT**: Assumes \( N \) is a power of 2 and uses divide-and-conquer approach.
  - **Radix-4 FFT**: Similar to Radix-2 but processes 4 points at a time.

### FFT Algorithms
1. **Radix-2 FFT Algorithm**:
   - Breaks the DFT into smaller DFTs, recursively, until reaching the base case of 2-point DFT.
   - Efficiently computes the FFT by reusing calculations.

2. **Radix-4 FFT Algorithm**:
   - Operates on groups of 4 points, resulting in further reduced computations.
   - Reduces the number of multiplications compared to the Radix-2 approach.

## 5. Circular Convolution
- Circular convolution can be performed using the DFT and its inverse.
- If \( x[n] \) and \( h[n] \) are sequences of length \( N \):
  \[
  y[n] = x[n] \circledast h[n] = \text{IDFT}(\text{DFT}(x[n]) \cdot \text{DFT}(h[n]))
  \]

## Summary
- Fourier Transform provides frequency domain representation for signals.
- The DFT is a discrete version of the Fourier Transform for sampled signals.
- FFT algorithms greatly enhance computational efficiency for DFT calculations.
