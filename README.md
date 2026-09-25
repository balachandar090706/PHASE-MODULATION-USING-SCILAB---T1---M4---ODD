# PHASE-MODULATION-USING-SCILAB---T1---M4---ODD


## Aim

To implement and analyze Phase Modulation (PM) using Scilab.

## Apparatus Required
1. **Software:** Scilab environment
2. **Hardware:** Personal Computer

---

## Theory
Phase Modulation (PM) is a technique where the phase of the carrier wave is varied in proportion to the instantaneous amplitude of the input signal (message signal). Unlike Frequency Modulation (FM), where the frequency is varied, in Phase Modulation, the phase angle of the carrier wave changes with the amplitude of the message signal.

### Mathematical Representation
The general form of a Phase Modulated signal $s(t)$ is given by:

$$s(t) = A_c \cos(2\pi f_c t + k_p m(t))$$

Where:
* $A_c$ : Amplitude of the carrier wave
* $f_c$ : Carrier frequency
* $m(t)$ : Message signal, typically $m(t) = A_m \cos(2\pi f_m t)$
* $k_p$ : Phase deviation sensitivity (in radians/volt)

## Scilab code:
~~~
Am = 2;
Ac = 5;
Fm = 20;
Fc = 200;
Fs = 2000;
Kp = 5` ;

t = 0:1/Fs:0.5;

Em =  Am*cos(2*%pi*Fm*t);
Ec =  Ac*cos(2*%pi*Fc*t);

Epm = Ac*cos(2*%pi*Fc*t+Kp*Em);

subplot(3,1,1);
plot(t,Em);
xlabel("Time(s)");
ylabel("Amplitude");
title("Message Signal");

subplot(3,1,2);
plot(t,Ec);
xlabel("TIme(s)");
ylabel("Amplitude");
title("Carrier Signal");

subplot(3,1,3);
plot(t,Epm);
xlabel("Time(s)");
ylabel("Amplitude");
title("Phase Modulation Signal");

~~~

## Algorithm
1. **Initialize Parameters:**
   * Define carrier amplitude ($A_c$), carrier frequency ($f_c$), message frequency ($f_m$), sampling frequency ($f_s$), and phase sensitivity ($k_p$).
2. **Generate Time Axis:**
   * Create a time array $t$ with suitable sampling steps over the signal duration.
3. **Generate Message Signal:**
   * Compute the message signal vector $m(t)$ using the cosine function.
4. **Generate Carrier Signal:**
   * Compute the unmodulated carrier signal vector $c(t) = A_c \cos(2\pi f_c t)$.
5. **Generate PM Signal:**
   * Compute the phase-modulated signal $s(t) = A_c \cos(2\pi f_c t + k_p m(t))$.
6. **Plot the Signals:**
   * Use Scilab's plotting commands (`subplot`, `plot`, `xtitle`, `xgrid`) to display message, carrier, and modulated signals.

---
##Tabulation:
<img width="1280" height="768" alt="image" src="https://github.com/user-attachments/assets/7a19f1bd-16e0-461f-9ea9-bf234aa13e20" />

##Calculation:

<img width="668" height="728" alt="image" src="https://github.com/user-attachments/assets/85eb3629-92bb-4ab5-829e-726f594ffc0d" />

## Result: 

 The message signal, carrier signal, and phase-modulated (PM) signal will be displayed in separate plots.
