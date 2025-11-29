# FM-using-Python

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
import numpy as nm
import matplotlib.pyplot as pot
Am = 6.9
fm = 437
Ac = 13.8
fc = 4370
fs = 43700
b = 5.75
t = nm.arange(0,2/fm,1/fs)
m= Am*nm.cos(2*nm.pi*fm*t)
pot.subplot(3,1,1)
pot.plot(t,m)
c= Ac*nm.cos(2*nm.pi*fc*t)
pot.subplot(3,1,2)
pot.plot(t,c)
s=Ac*nm.cos(2*nm.pi*fc*t+b*nm.sin(2*nm.pi*fm*t))
pot.subplot(3,1,3)
pot.plot(t,s)
```


Output Waveform

<img width="867" height="651" alt="image" src="https://github.com/user-attachments/assets/cf8c669d-b74a-4086-9635-c7b0e33d1262" />



Tabular Column

![WhatsApp Image 2025-11-29 at 06 43 31_409124d7](https://github.com/user-attachments/assets/7cfe513b-85f9-41fb-acb0-687adfd68003)


Calculation
![WhatsApp Image 2025-11-29 at 06 43 31_cce25626](https://github.com/user-attachments/assets/bcd88fa4-c03b-4cef-bb02-224f64ba7d06)




Result


The message signal, carrier signal, and frequency modulated (FM) signal will be displayed in separate plots. The modulated signal will show frequency variations corresponding to the amplitude of the message signal.
