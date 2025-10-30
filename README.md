# GENERATION-AND-DETECTION-OF-AM_1
## AIM:
To generate and detect the amplitude modulation and demodulation u s i n g S C I L A B and to calculate modulation index of AM.

## EQUIPMENTS REQUIRED

•	Computer with i3 Processor

•	SCI LAB

## THEORY:
Modulation can be defined as the process by which the characteristics of carrier wave are varied in accordance with the modulating wave (signal). Modulation is performed in a transmitter by a circuit called a modulator.

Need for modulation is as follows:

•	Avoid mixing of signals

•	Reduction in antenna height

•	long distance communication

•	Multiplexing

•	Improve the quality of reception

•	Ease of radiation.

Amplitude Modulation is the process of changing the amplitude of a relatively high frequency carrier signal in proportion with the instantaneous value of the modulating signal. The output waveform contains all the frequencies that make up the AM signal and is used to transport the information through the system. Therefore the shape of the modulated wave is called the AM envelope. With no modulating signal the output waveform is simply the carrier signal. Coefficient of modulation is a term used to describe the amount of amplitude change present in an AM waveform. There are three degrees of modulation available based on value of modulation index.

1)	Under modulation :	m<1, Em < Ec
	
2)	Critical modulation: m-1, Em = Ec
  
3)	Over modulation:	m>1, Em > Ec

Note: Keep all the switch faults in off position

## ALGORITHM
1.	Define Parameters
   
    First, define the parameters for your signals:
    
    •	Carrier frequency (fc)
    
    •	Modulating signal frequency (fm)
    
    •	Sampling frequency (Fs)
    
    •	Duration of the signal (T)

2.	Create a time vector based on the sampling frequency and duration.
 
3.	Create Modulating Signal:Define the modulating signal (message signal).

4.	Create Carrier Signal:Define the carrier signal.

5.	Perform Amplitude Modulation:Multiply the carrier signal by the modulating signal plus 1 (to ensure the modulation depth).

6.	Plot the Signals:Visualize the modulating, carrier, and modulated signals.

7.	Demodulate the AM Signal:To demodulate, you can use envelope detection. One way is to rectify the signal and then apply a low-pass filter.

8.	Plot the Demodulated Signal:Visualize the demodulated signal.

9.	Compare Signals:Compare the original modulating signal with the demodulated signal.

 ## PROCEDURE
•	Refer Algorithms and write code for the experiment.

•	Open SCILAB in System

•	Type your code in New Editor

•	Save the file

•	Execute the code

•	If any Error, correct it in code and execute again

•	Verify the generated waveform using Tabulation and Model Waveform

## MODEL GRAPH:
<img width="600" height="800" alt="image" src="https://github.com/user-attachments/assets/7bc77926-9c2a-42c6-994b-6c67433b11d2" />

## PROGRAM:
```
Ac = 12.2;
Am = 6.1;
Fc = 5630;
Fm = 563;
Fs = 56300;
t = 0:1/Fs:2/Fm;
e1 = (Ac*sin(2*3.14*Fm*t));
subplot(4,1,1);
plot(t,e1);
xgrid;
title('Message Signal');
xlabel('Time');
ylabel('Amplitude');

e2 = (Ac*sin(2*3.14*Fc*t));
subplot(4,1,2);
plot(t,e2);
xgrid;
title('Carrier Signal');
xlabel('Time');
ylabel('Amplitude');

e3 = (Ac + (Am*sin(2*3.14*Fm*t))).*sin(2*3.14*Fc*t);
subplot(4,1,3);
plot(t,e3);
xgrid;
title('AM Modulated Signal');
xlabel('Time');
ylabel('Amplitude');

demodulated_signal = abs(hilbert(e3)) - Ac;
subplot(4,1,4);
plot(t,demodulated_signal);
xgrid;
title('Demodulated Signal');
xlabel('Time');
ylabel('Amplitude');
```
 
## TABULATION:
![WhatsApp Image 2025-10-30 at 22 06 37_5206b9f2](https://github.com/user-attachments/assets/812b8499-3f36-4ccf-a0b5-8b760cba6f32)


## CALCULATION:
![WhatsApp Image 2025-10-30 at 22 11 08_999261bf](https://github.com/user-attachments/assets/4b98a5f7-b802-4902-9631-696f7f93f5a9)




## OUTPUT:
<img width="757" height="719" alt="image" src="https://github.com/user-attachments/assets/27e730a8-cc64-40e9-925b-7ba5fae066b8" />


## RESULT:
Thus the amplitude modulation and demodulation is experimentally done and the output is verified.
