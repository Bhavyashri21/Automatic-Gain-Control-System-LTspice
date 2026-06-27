# Automatic-Gain-Control-System-LTspice
Automatic Gain Control (AGC) System using a JFET-Based Variable Gain Amplifier designed and simulated in LTspice.

An Automatic Gain Control (AGC) system designed and simulated in **LTspice** using a **2N3819 N-channel JFET-based Variable Gain Amplifier (VGA)** and **ADTL082 operational amplifiers**. The project automatically regulates output amplitude by detecting the signal envelope and applying a negative control voltage to the JFET gate.

---

## Project Overview

The AGC consists of three major stages:

- Variable Gain Amplifier (VGA) using a 2N3819 N-channel JFET
- Precision Peak Detector & Envelope Extractor
- Closed-loop Automatic Gain Control feedback

The output signal is continuously monitored by the peak detector. The detected envelope generates a control voltage that biases the JFET gate, automatically reducing or increasing amplifier gain to maintain a nearly constant output amplitude.

---

## Components Used

- 2N3819 N-Channel JFET
- ADTL082 Dual Operational Amplifier
- 1N4148 Diodes
- Resistors (8.2kΩ, 82kΩ, 100kΩ)
- Capacitors (100nF, 1µF)
- ±12V Supply
- LTspice

---

## Design Specifications

| Parameter | Value |
|-----------|-------|
| Supply Voltage | ±12 V |
| Input Signal Frequency | 1 kHz |
| Input Range | 80 mV – 600 mV |
| Gate Control Voltage | 0 V to -3 V |
| Controlled Output Range | Approximately 140 mV – 300 mV |

---

## Working Principle

1. The input signal is amplified by the JFET-based Variable Gain Amplifier.
2. A precision peak detector extracts the signal envelope.
3. The envelope is filtered to generate a DC control voltage.
4. The control voltage is fed back to the JFET gate.
5. As the input amplitude increases, the gate voltage becomes more negative, reducing VGA gain.
6. This negative feedback stabilizes the output amplitude over a wide input range.

---

## Simulation Results

The repository contains simulation results for:

### Variable Gain Amplifier (VGA)

- Gate Voltage = 0 V
- Gate Voltage = -0.5 V
- Gate Voltage = -1 V
- Gate Voltage = -1.5 V
- Gate Voltage = -2 V
- Gate Voltage = -2.5 V
- Gate Voltage = -3 V

These simulations demonstrate the decrease in amplifier gain as the gate voltage becomes increasingly negative.

### Precision Peak Detector

- Circuit implementation
- Envelope detection waveforms
- Peak detector output verification

### Complete AGC System

Transient simulations were performed for input amplitudes of:

- 80 mV
- 100 mV
- 200 mV
- 300 mV
- 400 mV
- 500 mV
- 600 mV

The AGC successfully adjusts the VGA gain through feedback to regulate the output over the applied input range.

All circuit diagrams and simulation waveforms are available in the **AGC_results** folder.

---

## Repository Structure

```
Automatic-Gain-Control-System-LTspice
│
├── AGC.asc
├── Automatic Gain Control (AGC) System.pdf
├── README.md
│
└── AGC_results
    ├── AGC_Circuit.png
    ├── Variable Gain Amplifier.png
    ├── VGA_0.png
    ├── VGA_-0.5.png
    ├── VGA_-1.png
    ├── VGA_-1.5.png
    ├── VGA_-2.png
    ├── VGA_-2.5.png
    ├── VGA_-3.png
    ├── Precision Peak Detector.png
    ├── Precision Peak Detector_results_1.png
    ├── Precision Peak Detector_results_2.png
    ├── AGC_80mV.png
    ├── AGC_100mV.png
    ├── AGC_200mV.png
    ├── AGC_300mV.png
    ├── AGC_400mV.png
    ├── AGC_500mV.png
    └── AGC_600mV.png
```

---

## Software Used

- LTspice XVII

---

