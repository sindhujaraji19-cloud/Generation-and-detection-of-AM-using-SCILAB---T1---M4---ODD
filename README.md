# Generation-and-detection-of-AM-using-SCILAB---T1---M4---ODD
# AIM

To generate and detect the amplitude modulation and demodulation using SCILAB and to calculate modulation index of AM.

# EQUIPMENTS REQUIRED

* Computer with i3 Processor
* SCI LAB

# THEORY

Modulation can be defined as the process by which the characteristics of carrier wave are varied in accordance with the modulating wave (signal). Modulation is performed in a transmitter by a circuit called a modulator.

Need for modulation is as follows:

* Avoid mixing of signals
* Reduction in antenna height
* Long distance communication
* Multiplexing
* Improve the quality of reception
* Ease of radiation

Amplitude Modulation is the process of changing the amplitude of a relatively high frequency carrier signal in proportion with the instantaneous value of the modulating signal. The output waveform contains all the frequencies that make up the AM signal and is used to transport the information through the system. Therefore the shape of the modulated wave is called the AM envelope. With no modulating signal the output waveform is simply the carrier signal. Coefficient of modulation is a term used to describe the amount of amplitude change present in an AM waveform. There are three degrees of modulation available based on value of modulation index.

1. **Under modulation:** `m < 1`, `Em < Ec`
2. **Critical modulation:** `m = 1`, `Em = Ec`
3. **Over modulation:** `m > 1`, `Em > Ec`

**Note:** Keep all the switch faults in off position.

# ALGORITHM

### 1. Define Parameters

First, define the parameters for your signals:

* Carrier frequency (fc)
* Modulating signal frequency (fm)
* Sampling frequency (Fs)
* Duration of the signal (T)

### 2. Create Time Vector

Create a time vector based on the sampling frequency and duration.

### 3. Create Modulating Signal

Define the modulating signal (message signal).

### 4. Create Carrier Signal

Define the carrier signal.

### 5. Perform Amplitude Modulation

Multiply the carrier signal by the modulating signal plus 1 (to ensure the modulation depth).

### 6. Plot the Signals

Visualize the modulating, carrier, and modulated signals.

### 7. Demodulate the AM Signal

To demodulate, you can use envelope detection. One way is to rectify the signal and then apply a low-pass filter.

### 8. Plot the Demodulated Signal

Visualize the demodulated signal.

### 9. Compare Signals

Compare the original modulating signal with the demodulated signal.

## CODE
clc;
clear;
close;

// Time
t = 0:0.00001:0.01;

// Message signal
Am = 1;
fm = 1000;
m = Am*sin(2*%pi*fm*t);

// Carrier signal
Ac = 2;
fc = 10000;
c = Ac*cos(2*%pi*fc*t);

// Modulation index
mu = Am/Ac;

// AM generation
am = Ac*(1 + mu*sin(2*%pi*fm*t)) .* ...
     cos(2*%pi*fc*t);

// AM detection using envelope
detected = abs(am);

// Plot Message Signal
subplot(3,1,1);
plot(t,m);
xlabel("Time (s)");
ylabel("Amplitude");
title("Message Signal");

// Plot Carrier Signal
subplot(3,1,2);
plot(t,c);
xlabel("Time (s)");
ylabel("Amplitude");
title("Carrier Signal");

// Plot AM Signal
subplot(3,1,3);
plot(t,am);
xlabel("Time (s)");
ylabel("Amplitude");
title("AM Signal");

# PROCEDURE

* Refer Algorithms and write code for the experiment.
* Open SCILAB in System.
* Type your code in New Editor.
* Save the file.
* Execute the code.
* If any Error, correct it in code and execute again.
* Verify the generated waveform using Tabulation and Model Waveform.

# MODEL GRAPH
<img width="503" height="350" alt="image" src="https://github.com/user-attachments/assets/939a5540-7b17-4dc2-8615-fcb78bf63c8c" />

# TABULATION

<img width="1600" height="1209" alt="image" src="https://github.com/user-attachments/assets/63ad375e-0184-4b45-b6f5-13a80c51bbc5" />


# CALCULATION

<img width="1600" height="991" alt="image" src="https://github.com/user-attachments/assets/1d70b0a8-da0e-406e-8d02-ed4df98f9c0e" />


# OUTPUT
<img width="1146" height="629" alt="image" src="https://github.com/user-attachments/assets/96a6c069-b7c1-45d9-8abe-c9e241221129" />

# RESULT

Successfully generated and detected the amplitude modulation and demodulation using SCILAB and to calculate modulation index of AM.





