# Unit V: Design of Digital Filters

## 1. Introduction to Digital Filters
- Digital filters are systems that process discrete-time signals to achieve a desired output.
- They can be classified into two main categories:
  - **Finite Impulse Response (FIR) Filters**: Have a finite duration response to an impulse input.
  - **Infinite Impulse Response (IIR) Filters**: Have an infinite duration response due to feedback.

## 2. Classification of Filters
### 2.1 Low-Pass Filters (LPF)
- Allow signals with a frequency lower than a certain cutoff frequency to pass through.
- Reject frequencies higher than the cutoff.

### 2.2 High-Pass Filters (HPF)
- Allow signals with frequencies higher than a certain cutoff frequency to pass through.
- Reject frequencies lower than the cutoff.

### 2.3 Band-Pass Filters (BPF)
- Allow a specific range of frequencies to pass through while attenuating frequencies outside this range.

### 2.4 Band-Stop Filters (BSF)
- Reject a specific range of frequencies while allowing other frequencies to pass.

## 3. Filter Specifications
- Key specifications for digital filters include:
  - **Cutoff Frequency**: The frequency at which the filter begins to attenuate signals.
  - **Passband Ripple**: Variation in the gain within the passband.
  - **Stopband Attenuation**: The minimum attenuation in the stopband.
  - **Transition Width**: The width of the frequency band between the passband and stopband.

## 4. Design of FIR Filters
### 4.1 Window Method
- Involves multiplying an ideal impulse response by a window function to reduce ripples.
- Common window functions include:
  - **Rectangular Window**: Simple but leads to significant ripples.
  - **Hamming Window**: Provides a smoother response.
  - **Hanning Window**: Reduces side lobes compared to rectangular.

### 4.2 Frequency Sampling Method
- Uses samples of the desired frequency response to construct the filter.
- The frequency response is expressed in terms of its discrete frequency components.

### 4.3 Design Steps
1. Specify the filter requirements (cutoff frequency, ripple, etc.).
2. Select the appropriate design method (window or frequency sampling).
3. Calculate the impulse response or filter coefficients.
4. Implement the filter in a discrete-time system.

## 5. Design of IIR Filters
### 5.1 From Analog Filters
- IIR filters can be derived from analog filter prototypes using transformation methods.

### 5.2 Approximation of Derivatives
- Techniques like the Bilinear Transformation can be used to convert analog filter specifications into digital filters.

### 5.3 Impulse Invariant Transformation
- Ensures that the impulse response of the digital filter matches that of the analog filter at discrete time intervals.

### 5.4 Bilinear Transformation
- Maps the s-plane of the analog filter to the z-plane of the digital filter, preserving stability.

### 5.5 Matched z-Transformation
- Uses a specific mapping of analog filter poles to create a digital filter that closely approximates the analog filter.

## 6. Commonly Used Analog Filters
- **Butterworth Filter**: Maximally flat response in the passband.
- **Chebyshev Filter**: Allows for ripple in the passband for a sharper cutoff.
- **Elliptic Filter**: Provides ripple in both the passband and stopband for the sharpest cutoff.

### Example: IIR Filter Design
1. Choose an analog prototype (e.g., Butterworth).
2. Specify the desired digital characteristics.
3. Use a transformation method (e.g., bilinear transformation) to obtain the digital filter coefficients.

## Summary
- Digital filters are essential for signal processing applications, enabling manipulation of signals in the discrete domain.
- The design process involves defining specifications, selecting the appropriate filter type, and employing design techniques for FIR and IIR filters.

