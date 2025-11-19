# Phase-Modulation-using-NumPy-and-Matplotlib-Modulation-and-Demodulation

# __Aim__:

To implement and analyze phase modulation (PM) using Python's NumPy and Matplotlib libraries. 


# __Apparatus Required__:

1. Software: Python with NumPy and Matplotlib libraries
   
2. Hardware: Personal Computer
   
# __Theory__:

Phase Modulation (PM) is a technique where the phase of the carrier wave is varied in proportion to the 
instantaneous amplitude of the input signal (message signal). Unlike frequency modulation, where the frequency 
is varied, in phase modulation, the phase angle of the carrier wave changes with the amplitude of the message 
signal. 


The general form of a PM signal can be represented as:

<img width="483" height="254" alt="image" src="https://github.com/user-attachments/assets/8d5a2e54-cf93-4ff0-b0a6-e2000e078682" />






# __Algorithm__: 

1. Initialize Parameters:
   
o Set values for carrier amplitude (Ac), carrier frequency (fc), message frequency
 
(fm), sampling frequency, and phase deviation sensitivity (kp). 

2. Generate Time Axis: 

o Create a time vector for the signal duration based on the sampling frequency. 

3. Generate Message Signal: 

o Define the message signal as a cosine wave. 

4. Generate PM Signal:
 
o Apply the PM modulation formula to obtain the modulated signal.

5. Plot the Signals:
 
o Use Matplotlib to plot the message signal, carrier signal, and phase-modulated signal.
# PROGRAM:
```
import numpy as np 
import matplotlib.pyplot as plt 
Ac = 0.5 
fc = 200 
Am = 1.0
fm = 20 
fs = 70000 
t = np.arange(0, 2/fm, 1/fs) 
Wm = 2 * np.pi * fm 
Wc = 2 * np.pi * fc 
Em = Am * np.sin(Wm * t) 
Ec = Ac * np.sin(Wc * t) 
Edsbsc = ((Am / 2) * np.cos((Wc - Wm) * t)) - ((Am / 2) * np.cos((Wc + Wm) * t)) 
plt.figure(figsize=(10, 6)) 
plt.subplot(3, 1, 1) 
plt.plot(t, Em) 
plt.grid() 
plt.subplot(3, 1, 2) 
plt.plot(t, Ec)
plt.grid() 
plt.subplot(3, 1, 3) 
plt.plot(t, Edsbsc) 
plt.grid() 
plt.tight_layout() 
plt.show()
```


# __Output__:
![WhatsApp Image 2025-11-19 at 13 51 30_f2bbeff9](https://github.com/user-attachments/assets/dc8cc9b1-2437-4460-a7a6-12b30918bbb6)

# TABULATION

![WhatsApp Image 2025-11-19 at 13 59 43_7b3e5817](https://github.com/user-attachments/assets/e50a4a8a-8825-4848-aa78-1650de24dbfa)

# CALCULATION
![WhatsApp Image 2025-11-19 at 13 59 44_87e64049](https://github.com/user-attachments/assets/b09bcd68-745e-45f8-9a6b-4e98368629f2)






# __Result__:
The message signal, carrier signal, and phase-modulated (PM) signal will be displayed in separate plots. The modulated signal will show phase variations corresponding to the amplitude of the message signal.




