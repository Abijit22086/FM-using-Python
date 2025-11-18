<img width="813" height="586" alt="Screenshot 2025-11-18 110656" src="https://github.com/user-attachments/assets/20ddfdd1-178a-477b-aafd-f996c0bd2221" /># FM-using-Python

Aim


To implement and analyze frequency modulation (FM) using Python's NumPy and Matplotlib libraries. 

Apparatus Required

1.	Software: Python with NumPy and Matplotlib libraries
2.	Hardware: Personal Computer
  
Theory

Frequency Modulation (FM) is a method of transmitting information over a carrier wave by varying its frequency in accordance with the amplitude of the input signal (message signal). The frequency of the carrier wave is varied according to the instantaneous amplitude of the message signal. The general form of an FM signal is:



Algorithm


1.	Initialize Parameters: Set the values for carrier frequency, message frequency, sampling frequency, and frequency deviation.
2.	Generate Time Axis: Create a time vector for the signal duration.
3.	Generate Message Signal: Define the message signal as a cosine wave.
4.	Compute the Integral of the Message Signal: Calculate the integral of the message signal over time.
5.	Generate FM Signal: Apply the FM modulation formula to obtain the modulated signal.
6.	Plot the Signals: Use Matplotlib to plot the message signal, carrier signal, and modulated signal.

Program
```
import numpy as np
import matplotlib.pyplot as plt

Am=4.3
Ac=8.6
fm=324
fc=3240
fs=32400
t=np.arange(0,3/fm,1/fs)
m=Am*np.cos(2*np.pi*fm*t)
c=Ac*np.cos(2*np.pi*fc*t)
b=4.5
eFM =Ac*np.cos(2 * np.pi * fc * t + b * np.sin(2 * np.pi * fm * t))
plt.subplot(3,1,1)
plt.plot(t,m)
plt.grid()
plt.subplot(3,1,2)
plt.plot(t,c)
plt.grid()
plt.subplot(3,1,3)
plt.plot(t,eFM)
plt.grid()

plt.tight_layout()
plt.show()
```

Output Waveform:

<img width="813" height="586" alt="Screenshot 2025-11-18 110656" src="https://github.com/user-attachments/assets/70fec272-b9ce-4157-87be-d268a7ab3e08" />

Tabular Column

![fm table py](https://github.com/user-attachments/assets/0348bc33-21e5-48db-af80-4b7e8b9ce201)

Calculation

![fm calcultion py](https://github.com/user-attachments/assets/952e113c-cc92-4a29-9646-2001d91604e4)

Result


The message signal, carrier signal, and frequency modulated (FM) signal will be displayed in separate plots. The modulated signal will show frequency variations corresponding to the amplitude of the message signal.
