Reconfigurable Intelligent Surface (RIS) Aided MIMO-OFDM System

Project Overview

This repository contains a Simulink-based physical layer model designed to evaluate the performance of Reconfigurable Intelligent Surfaces (RIS) in next-generation wireless networks. The project demonstrates how an RIS can be used to mitigate Rayleigh fading and noise by creating a controlled reflection path that constructively interferes with the direct signal.
The system utilizes a 16-QAM MIMO-OFDM architecture, comparing a degraded direct-link channel against an optimized RIS-assisted channel.

System Architecture

The model is divided into three primary stages:

Transmitter:
Data Source: Bernoulli Binary generator
Modulation: 16-QAM mapping for high spectral efficiency.
Multiplexing: OFDM Modulator to combat frequency-selective fading.

Channel Environment (Dual-Path):
Direct Path: A Rayleigh MIMO channel with AWGN representing standard environmental interference.
RIS Path: A cascaded channel involving a Transmitter-to-RIS link, an Intelligent Phase-Shift Controller, and an RIS-to-Receiver link.

Receiver:
Signal Combiner: Summation of direct and RIS-reflected signals.
Demodulation: OFDM Demodulator and 16-QAM De-mapper.
Analysis: Bit Error Rate (BER) calculation and Constellation Diagram visualization.

Performance Analysis

The project includes a real-time Constellation Diagram that highlights the "RIS Gain":
Yellow Cluster (Direct Link): Shows high dispersion and variance. The signal is heavily affected by multi-path fading, making it difficult for the receiver to distinguish symbols.
Blue Cluster (RIS-Aided Link): Shows a highly focused and tight distribution around the 16-QAM ideal points. This demonstrates the RIS's ability to perform passive beamforming, effectively increasing the Signal-to-Noise Ratio (SNR).

Key Features

Dynamic Phase Shifting: Custom MATLAB function (RIS_PhaseShift) to simulate real-time phase adjustment of reflecting elements.
MIMO Support: Built using Rayleigh MIMO blocks to simulate spatial diversity.
Visual Proof-of-Concept: Easy-to-read scopes for immediate verification of signal improvement.

*How to Use*
1. Clone this repository: git clone https://github.com/your-username/RIS-MIMO-OFDM.git
2. Open MATLAB (R2021a or later recommended).
3. Ensure the Communications Toolbox and DSP System Toolbox are installed.
4. Open the .slx file and click Run.
5. Observe the Constellation Diagram and Error Rate Calculation blocks.

*Future Work*
Implementation of Deep Learning based phase-shift optimization.
Expansion to Multi-user MIMO (MU-MIMO) scenarios.
Hardware-in-the-loop (HIL) testing using ADALM-Pluto SDR.

