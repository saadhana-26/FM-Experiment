# FM

EXP NO: 4	GENERATION AND DETECTION OF FM


AIM:
To write a program for Frequency Modulation and Demodulation using SCILAB and to observe and measure the frequency deviation and the modulation index of FM.


EQUIPMENTS REQUIRED

•	Computer with i3 Processor
•	SCI LAB

THEORY:

Frequency modulation is a type of modulation in which the frequency of the high frequency (carrier) is varied in accordance with the instantaneous value of the modulating signal.
FREQUENCY DEVIATION f and MODULATION INDEX m f :
The frequency deviation f represents the maximum shift between the  modulatedsignal
frequency, over and under the frequency of the carrier.

We define modulation index m f the ratio between f and the modulating frequency
m= f / fm


FREQUENCY MODULATION GENERATION:
The circuits used to generate a frequency modulation must vary the frequency of a high frequency signal (carrier) as function of the amplitude of a low frequency signal (modulating signal). In practice there are two main methods used to generate FM.
Algorithm
1.	Define Parameters:
•	Fs: Sampling frequency.
•	T: Duration of the signal.
•	Fc: Carrier frequency.
•	Fm: Frequency of the modulating signal.
•	Beta: Modulation index, which controls the extent of frequency deviation.
2.	Generate Signals:
•	Modulating signal: Sinusoidal signal used for modulation.
•	Carrier signal: The high-frequency carrier signal.
•	Modulated signal: FM modulated signal calculated by varying the carrier frequency according to the modulating signal.
3.	FM Modulation:
•	Modulated signal is obtained by modulating the carrier signal with the modulating signal.
 
4.	FM Demodulation:
•	Differentiation: Computes the derivative of the modulated signal to extract frequency variations.
•	Envelope Detection: Takes the absolute value to retrieve the envelope of the signal.
•	Low-pass Filtering: Applies a Butterworth low-pass filter to smooth the envelope and recover the original modulating signal.
5.	Visualization:
•	Plots the modulating signal, carrier signal, FM modulated signal, and demodulated signal for analysis.



PROCEDURE


•	Refer Algorithms and write code for the experiment.
•	Open SCILAB in System
•	Type your code in New Editor
•	Save the file
•	Execute the code
•	If any Error, correct it in code and execute again
Verify the generated waveform using Tabulation and Model Waveform

MODEL GRAPH:

<img width="512" height="365" alt="image" src="https://github.com/user-attachments/assets/acd787bd-5281-4f1b-802f-1aa39fac9189" />


Program
~~~
am=10.9;
fm=480;
fc=4800;
fs=48000;
t=0:1/fs:2/fm;
m=am*cos(2*3.14*fm*t);
subplot(3,1,1);
plot(t,m);
ac=21.8;
c=ac*cos(2*3.14*fc*t);
subplot(3,1,2);
plot(t,c);
b=3.15;
s=ac*cos((2*3.14*fc*t)+(b*sin(2*3.14*fm*t)));
subplot(3,1,3);
plot(t,s);
~~~

Output Waveform

<img width="766" height="727" alt="Screenshot 2025-11-11 102037" src="https://github.com/user-attachments/assets/98c2354f-2d9a-44cb-888c-24ec8ebf4eb2" />



Tabulation

![WhatsApp Image 2025-11-11 at 11 07 55_7b4d142f](https://github.com/user-attachments/assets/aaa7c703-ab23-4134-9a88-658318dd277b)


Calculation
![WhatsApp Image 2025-11-11 at 11 07 56_e8fc8904](https://github.com/user-attachments/assets/c737cadf-c7a1-45ee-ad74-e8b1b094f107)



Frequency Deviation Practical = 1536.96

Modulation Index Practical	= 3.15

Modulation Index Theoretical	= 3.15



RESULT:

Thus, the frequency modulation and demodulation is successfully done and the output is experimentally verified.


