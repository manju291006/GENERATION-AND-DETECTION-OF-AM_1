GENERATION-AND-DETECTION-OF-AM_1
AIM:
To generate and detect the amplitude modulation and demodulation u s i n g S C I L A B and to calculate modulation index of AM.

EQUIPMENTS REQUIRED
• Computer with i3 Processor

• SCI LAB

THEORY:
Modulation can be defined as the process by which the characteristics of carrier wave are varied in accordance with the modulating wave (signal). Modulation is performed in a transmitter by a circuit called a modulator.

Need for modulation is as follows:

• Avoid mixing of signals

• Reduction in antenna height

• long distance communication

• Multiplexing

• Improve the quality of reception

• Ease of radiation.

Amplitude Modulation is the process of changing the amplitude of a relatively high frequency carrier signal in proportion with the instantaneous value of the modulating signal. The output waveform contains all the frequencies that make up the AM signal and is used to transport the information through the system. Therefore the shape of the modulated wave is called the AM envelope. With no modulating signal the output waveform is simply the carrier signal. Coefficient of modulation is a term used to describe the amount of amplitude change present in an AM waveform. There are three degrees of modulation available based on value of modulation index.

Under modulation : m<1, Em < Ec

Critical modulation: m-1, Em = Ec

Over modulation: m>1, Em > Ec

Note: Keep all the switch faults in off position

ALGORITHM
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

PROCEDURE
• Refer Algorithms and write code for the experiment.

• Open SCILAB in System

• Type your code in New Editor

• Save the file

• Execute the code

• If any Error, correct it in code and execute again

• Verify the generated waveform using Tabulation and Model Waveform

MODEL GRAPH:
image
PROGRAM:
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
TABULATION:
16816069-68d9-48a3-a6a5-1c12f1fb9582

CALCULATION:
8326a889-1be4-4320-90d3-09e6c487a5bb

OUTPUT:
image
RESULT:
Thus the amplitude modulation and demodulation is experimentally done and the output is verified.
