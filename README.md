 Channel Estimation Using Pilot Subcarriers

This module performs pilot-based channel estimation for an OFDM system.
The goal is to estimate the channel frequency response across all occupied subcarriers using only the known pilot tones.

Processing Steps
1. Extract Pilot Subcarriers
   
The received OFDM grid and transmitted grid (containing pilots) are sampled at the pilot indices to obtain .These pilots serve as reference signals for channel estimation.

2. Estimate Channel at Pilot Positions
   
Since pilot values are known, the channel at each pilot subcarrier is computed as seen from the code.This gives the exact channel response at the pilot frequencies (assuming a noiseless channel).

3. Interpolate Channel for All Subcarriers
   
Channel values for the non-pilot subcarriers are obtained using linear interpolation.This produces a full channel estimate that can be applied to all data subcarriers.

4. Visualization
   
PLots generated showing:
Pilot-based channel estimates.
Interpolated channel response.
