## Amplitude-Modulation-and-Demodulation-using-NumPy-and-Matplotlib

### Aim: 
To implement and analyze amplitude modulation (AM) using Python's NumPy and Matplotlib libraries. 
### Apparatus Required: 
Software: Python with NumPy and Matplotlib libraries 
Hardware: Personal Computer 
### Theory: 
Amplitude Modulation (AM) is a technique used in electronic communication, primarily for transmitting 
information via a radio carrier wave. In AM, the amplitude of the carrier wave is varied in proportion to that of 
the message signal. The general form of an AM signal is: 
### Algorithm:
1. Initialize Parameters: Set the values for carrier frequency, message frequency, and sampling frequency. 
2. Generate Time Axis: Create a time vector for the signal duration. 
3. Generate Message Signal: Define the message signal as a cosine wave. 
4. Generate Carrier Signal: Define the carrier signal as a cosine wave. 
5. Modulate Signal: Apply the AM formula to obtain the modulated signal. 
6. Plot the Signals: Use Matplotlib to plot the message signal, carrier signal, and modulated signal.
### Program :
```
import numpy as np 
import matplotlib.pyplot as plt 
Am = 14.2
Fm = 540
Ac = 28.4 
Fc = 5400 
Fs = 295000 
t = np.arange(0, 2/Fm, 1/Fs) 
em = Am * np.sin(2 * np.pi * Fm * t) 
plt.subplot(3, 1, 1) 
plt.plot(t, em) 
plt.grid() 
ec = Ac * np.sin(2 * np.pi * Fc * t) 
plt.subplot(3, 1, 2) 
plt.plot(t, ec) 
plt.grid() 
eam = (Ac + (Am * np.sin(2 * np.pi * Fm * t))) * np.sin(2 * np.pi * Fc * t) 
plt.subplot(3, 1, 3) 
plt.plot(t, eam) 
plt.grid() 
plt.tight_layout() 
plt.show()
```
### Output:
<img width="845" height="589" alt="Screenshot 2025-11-16 230655" src="https://github.com/user-attachments/assets/b7f003f1-b79c-4fff-b3a7-c17244875649" />


### Result:
The message signal, carrier signal, and amplitude modulated (AM) signal will be displayed in separate plots. 
Thus, AM is implemented using numPy and Matplotlib.
