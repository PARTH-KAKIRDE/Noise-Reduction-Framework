# Key Observations

1. FIR windowed filters reduce high-frequency noise but cannot remove in-band noise.
2. Blackman window provides superior stopband attenuation at the cost of wider transition bandwidth.
3. Median filtering effectively suppresses impulsive noise spikes prior to linear filtering.
4. Matched filtering significantly improves SNR by correlating the received signal with the known Gaussian pulse.
5. The matched filter output exhibits a time shift corresponding to filter group delay, which is compensated during trimming.
