## Sound Analysis, Synthesis and Processing - Homework 1

This project is the implementation of Homework #1 from the *DAAP* course (*Talking Instrument*). It uses Linear Predictive Coding (LPC) to perform a cross-synthesis between a speech signal (`speech.wav`) and a musical signal (monophonic `piano.wav`). The main idea is to run a short-time LPC analysis on the speech to obtain all-pole filters (shaping), and then use the residual (whitening) of the music signal as the excitation. The musical excitation is then processed through the filters derived from the speech.

Main objectives:

* Implement the closed-form solution of the Wiener–Hopf equations to compute LPC coefficients.
* Implement the iterative steepest descent method to solve the autocorrelation equations and compare stability and convergence.
* Apply whitening and shaping filters **in the frequency domain** (not direct convolution), and reconstruct the output frame-by-frame using overlap-and-add (OLA), ensuring the COLA condition and limiting temporal aliasing.
* Save the synthesized result into a WAV file.

> All methods are implemented without using high-level functions that directly perform LPC (`lpc()`, etc.). Library functions for FFT are used.

**Authors:** 
Chiara Lunghi,
Alice Portentoso
