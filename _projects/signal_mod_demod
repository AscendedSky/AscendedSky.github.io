---
layout: post
title: "Modulated Signal Transmission and Demodulation"
description: "Designed and implemented a modulated signal transmission and reception pipeline, including a 4th-order Butterworth low-pass filter with a 937 Hz cutoff for demodulation, achieving accurate signal recovery with less than 2% amplitude error."
skills:
  - Signal Processing
  - Analog Filter Design
  - Circuit Design
  - Breadboarding
  - Debugging
main-image: "/demodulated_signal.png"
date: 2025-10-15
---
My role in this project was to design and implement a modulated signal transmission and reception pipeline, with emphasis on analog demodulation and signal recovery.

The system design began with the definition of the baseband signal bandwidth and modulation parameters. To recover the original signal at the receiver, a 4th-order Butterworth low-pass filter was designed for the demodulation stage, with a cutoff frequency of 937 Hz. This filter order was selected to provide a flat passband response while sufficiently attenuating high-frequency components introduced during modulation.

{% include image-gallery.html images="modulated_signal.png" height="400" %}
<span style="font-size: 14px">Modulated Signal</span>

The low-pass filter was implemented using discrete analog components and constructed on a breadboard. Component values were selected to meet the desired frequency response, and the circuit was assembled and verified through incremental testing.

{% include image-gallery.html images="Breadboard.jpg" height="400" %}
<span style="font-size: 14px">Hardware Implementation – 4th-Order Butterworth Low-Pass Filter</span>

The complete transmission and reception chain was then tested using a modulated input signal. The demodulated output was measured and compared against the original baseband signal to evaluate recovery accuracy.

{% include image-gallery.html images="demodulated_signal.png" height="400" %}
<span style="font-size: 14px">Demodulated Signal</span>

The system achieved accurate signal recovery with peak noise less than 2% of the signal amplitude, confirming the effectiveness of the filter design and the overall demodulation approach.
