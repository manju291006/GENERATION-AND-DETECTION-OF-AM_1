# GENERATION-AND-DETECTION-OF-AM_1
## AIM:
To generate and detect the amplitude modulation and demodulation u s i n g S C I L A B and to calculate modulation index of AM.

## EQUIPMENTS REQUIRED
•	Computer with i3 Processor 
•	SCI LAB

Note: Keep all the switch faults in off position

## ALGORITHM:

Define Parameters

First, define the parameters for your signals:

• Carrier frequency (fc)

• Modulating signal frequency (fm)

• Sampling frequency (Fs)

• Duration of the signal (T)

Create a time vector based on the sampling frequency and duration.

Create Modulating Signal:Define the modulating signal (message signal).

Create Carrier Signal:Define the carrier signal.

Perform Amplitude Modulation:Multiply the carrier signal by the modulating signal plus 1 (to ensure the modulation depth).

Plot the Signals:Visualize the modulating, carrier, and modulated signals.

Demodulate the AM Signal:To demodulate, you can use envelope detection. One way is to rectify the signal and then apply a low-pass filter.

Plot the Demodulated Signal:Visualize the demodulated signal.

Compare Signals:Compare the original modulating signal with the demodulated signal.

## PROCEDURE
• Refer Algorithms and write code for the experiment.

• Open SCILAB in System

• Type your code in New Editor

• Save the file

• Execute the code

• If any Error, correct it in code and execute again

• Verify the generated waveform using Tabulation and Model Waveform


  
## MODEL GRAPH:
<img width="919" height="1290" alt="image" src="https://github.com/user-attachments/assets/c2c81cc3-db20-437b-9a63-257bb86aeaaa" />


## PROGRAM:
```
Am = 7;
Ac = 14;
fm = 653;
fc = 6530;
fs = 653000;
t = 0:1/fs:2/fm;
m = Am * cos(2*3.14*fm*t);
c = Ac * cos(2*3.14*fc*t);
s = (Ac + m) .* cos(2*3.14*fc*t);
envelope_signal = abs(hilbert(s));
demod = envelope_signal - Ac;
subplot(4,1,1);
plot(t, m, 'b');
title('Message Signal');
xlabel('Time (s)');
ylabel('Amplitude');

subplot(4,1,2);
plot(t, c, 'r');
title('Carrier Signal');
xlabel('Time (s)');
ylabel('Amplitude');

subplot(4,1,3);
plot(t, s, 'k');
title('AM Modulated Signal');
xlabel('Time (s)');
ylabel('Amplitude');

subplot(4,1,4);
plot(t, demod, 'g');
title('Demodulated Signal');
xlabel('Time (s)');
ylabel('Amplitude');
```

## TABULATION:
<img width="720" height="1280" alt="image" src="https://github.com/user-attachments/assets/ebeeb37a-f2ac-4f20-8119-e90462d5c496" />

## calculation:
<img width="720" height="1280" alt="image" src="https://github.com/user-attachments/assets/44d1b70e-d5cc-4500-aa97-093f10a12087" />

## output: 
<img width="687" height="573" alt="image" src="https://github.com/user-attachments/assets/6867e117-a219-4a52-b469-fd7de86cf69c" />



## RESULT:
Thus the amplitude modulation and demodulation is experimentally done and the output is verified.

