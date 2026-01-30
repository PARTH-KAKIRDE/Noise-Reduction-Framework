# SNR Performance Summary

Noise model:
- Additive white Gaussian noise
- Bernoulli–Gaussian impulsive noise (p = 0.005)

| Method | Output SNR (dB) |
|------|---------------|
| No filtering | -0.44 |
| Rectangular FIR | 6.86 |
| Hamming FIR | 7.02 |
| Blackman FIR | 7.05 |
| Hanning FIR | 7.04 |
| Matched Filter | 31.83 |

Matched filtering provides the highest SNR improvement due to coherent integration of the known pulse shape.
