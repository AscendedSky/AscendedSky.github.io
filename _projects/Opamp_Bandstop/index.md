---
layout: post
title: "Op-Amp Based Audio Noise Suppression Using a 3rd-Order Chebyshev Band-Stop Filter"
description: "Design and hardware implementation of a 3rd-order active Chebyshev band-stop filter for targeted audio noise suppression. The filter was designed around operational amplifiers and validated through LTspice simulation, Bode and frequency-response analysis, and physical breadboard testing. The implemented circuit achieved approximately 10 dB attenuation at the target frequency of 5 kHz while preserving overall signal amplitude and minimising distortion outside the stopband."
skills:
  - Analog Circuit Design
  - Operational Amplifiers
  - Active Filters
  - Signal Processing
  - Frequency Response Analysis
  - SPICE Simulation

main-image: "/real_spectrum.png"
---
## More Details 

My role in this project was to design and tune the High-Pass Filter (HPF), which was then combined with a Low-Pass Filter (LPF) through a summing amplifier to create a Band-Stop filter. Designing the HPF required selecting an op-amp that met the gain-bandwidth (GBW) constraints of the filter. The chosen op-amp was the TL084, which is not specified in the schematic below.

<img src="/_projects/Opamp_Bandstop/HPF_schematic.png" alt="3rd-Order Chebyshev High-Pass Filter Schematic" height="400"> <span style="font-size: 14px">Circuit Schematic – 3rd-Order Chebyshev High-Pass Filter</span>

An LTspice simulation of the overall Band-Stop filter was conducted, and both the frequency response and FFT spectrum were obtained using actual audio input.

<img src="/_projects/Opamp_Bandstop/simulated_filter_response.png" alt="LTspice Simulation Frequency Response" height="300"> <span style="font-size: 14px">LTspice Simulation – Frequency Response</span> <img src="/_projects/Opamp_Bandstop/simulated_spectrum.png" alt="LTspice Simulation Spectrum" height="300"> <span style="font-size: 14px">LTspice Simulation – Spectrum</span>

The HPF was also constructed and tested on a breadboard to verify that the hardware produced the approximate cutoff required for the designed Band-Stop filter.

<img src="/_projects/Opamp_Bandstop/HPF_filter_response.png" alt="Actual Frequency Response of HPF" height="300"> <span style="font-size: 14px">Actual Frequency Response of HPF</span> <img src="/_projects/Opamp_Bandstop/breadboard.jpg" alt="Breadboard Setup HPF Only" height="300"> <span style="font-size: 14px">Hardware Implementation – Breadboard Setup (HPF Only)</span>

Finally, the overall Band-Stop filter was tested by combining the HPF and LPF on two breadboards to ensure that the target frequency and attenuation specifications were met.

<img src="/_projects/Opamp_Bandstop/real_filter_response.png" alt="Measured Frequency Response 12 dB at 5 kHz" height="300"> <span style="font-size: 14px">Measured Frequency Response: 12 dB Attenuation at 5 kHz</span> <img src="/_projects/Opamp_Bandstop/real_spectrum.png" alt="Measured Spectrum 10 dB at 5 kHz" height="300"> <span style="font-size: 14px">Measured Spectrum: 10 dB Attenuation at 5 kHz</span>
