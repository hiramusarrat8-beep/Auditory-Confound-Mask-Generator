# Auditory-Confound-Mask-Generator
# Auditory Confound Masking Generator for Transcranial Ultrasound

This repository provides a Python-based utility to generate auditory masking stimuli matched to commonly used pulsed transcranial ultrasound (TUS) parameters. The purpose of this project is to support transparent control and demonstration of auditory confounds in human TUS experiments(Kop et al., eLife 2023)

## Background

Pulsed TUS protocols, particularly those using audible pulse repetition frequencies, can generate sound via bone conduction. This auditory component can influence neural and behavioral measures if not explicitly controlled. As a result, masking or sound-only control stimuli should closely match the temporal structure and perceptual characteristics of the ultrasound pulse train.

This project implements a masking stimulus based directly on parameters reported in published human TUS studies.

## Masking Sound Design

The masking sound is constructed to mirror the temporal characteristics of pulsed TUS:

- A 1 kHz square-wave carrier is used to approximate the harsh, click-like percept associated with bone-conducted sound.
- The carrier is gated at a pulse repetition frequency (PRF) of 1000 Hz.
- Each pulse has a duration (pulse width) of 0.3 ms, corresponding to a 30% duty cycle.
- The total duration of the stimulus matches the ultrasound pulse-train duration (default: 500 ms).
- White noise is added at a fixed signal-to-noise ratio (SNR) of 14:1 to better approximate the irregular auditory percept of TUS.

All parameters are explicitly defined and can be adjusted at the top of the generation script.

### Reference

Kop, B., et al. (2023). Auditory confounds can drive online effects of transcranial ultrasonic stimulation in humans. eLife.


