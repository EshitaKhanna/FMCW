# FMCW for Contactless Sleep Apnea Detection using smartphones 

This repository implements Frequency-Modulated Continuous Wave (FMCW) radar technology to detect sleep apnea using a smartphone. The system uses a frequency-modulated signal (chirp signal) to capture reflections from objects, such as a person's chest, enabling the monitoring of subtle breathing movements.

Sleep apnea involves minute variations in breathing patterns, which can be challenging to detect. This implementation leverages FMCW radar to differentiate small frequency shifts (around 11.7 Hz) from other reflections, providing a non-invasive and contactless method for analyzing breathing patterns during sleep.

## Implementation Steps
To implement FMCW radar for contactless sleep apnea detection on smartphones, the following steps are typically taken:

1. **Setup**: Place the smartphone up to 1 meter from the subject.
2. **Transmission**: Emit an 18-20 kHz chirp signal from the phone's speaker.
3. **Reception**: Capture the reflected signals using the smartphone’s microphone.
4. **Measurement**:
   - **Frequency Shift Calculation**:
   $\Delta\ f = \frac{f_{\text{0}} - f_{\text{1}}}{T_{\text{sweep}}} \cdot \Delta t$
   - **Time Delay Calculation**:
   $\Delta\ t = \frac{2d}{v_{sound}}$ 
5. **Distance Calculation**:
   $d = \frac{\Delta\ t \cdot v_{sound}}{2}$ <br>
   Where:
   - $d$ is the distance to the human body
   - $\Delta\ t$ is the time delay between the transmitted and reflected signals
   - $v_{sound}$ is the speed of sound
6. **Breathing Tracking**: Monitor changes in distance over time to track breathing movements.

## Reference

[**Contactless Sleep Apnea Detection on Smartphones**](https://apnea.cs.washington.edu/apneaapp.pdf)
