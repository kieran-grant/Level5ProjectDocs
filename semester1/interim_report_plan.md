# Interim Report Plan

# Overall narrative
## Why arbitrary DAFX rather than DDSP modules?
- DDSP offers a way of style matching in a auto-differentiable way. However, it relies on each audio module to be implemented in a framework which supports auto-differentiation.
- The overwhelming majority of audio units are implemented in frameworks such as VST, AU and LV2. These DAFX are tools which are used by audio engineers to shape and mix audio signals which are then released as songs, podcasts, films and myriad other applications.
- Audio engineers will then use their preferred tools to sculpt sounds, or those wishing to learn audio engineering may only have a small selection of audio units.
- The goal of this project is to implement a style-matching deep learning model which can learn parameter values from a arbitrary DAFX without the need for a differentiable implementation of the effect.

## Why use reference tracks?
- Communicating audio transformations through semantic language is a difficult challenge - not least because of the subjectiveness of describing sounds.
- Many researchers across various fields have attempted to create dictionaries of descriptive language used for discussing sounds.
- However, there are difficulties such as cultural (two different cultures with shared language have different meanings for 'warm') and language barriers (no exact translation from one language to another, some words have different connotations based on language).
- Also these semantic descriptors are heavily dependant on the context: e.g. warm in a classical setting may not describe what is meant by warm in electronic music.
- Other authors have attempted to implement models which learn parameter settings by matching sounds to humans emulating the sounds they would like: drums etc. However, these also have some problems.
- While reference tracks have limitations (not one-to-one, only want to emulate one sound in the recording, recording may be poor quality, many effects are non-linear).

# Group papers read

## Black-Box Emulation of Amplifiers and Effects
- A Review of Neural Network-Based Emulation of Guitar Amplifiers
- Deep Learning for Tube Amplifier Emulation
- Efficient Neural Networks for Real-time Analog Audio Effect Modeling

## Learning user preferences with sound processing
- A method for rapid personalization of audio equalization parameters
- Learning to Build Natural Audio Production Interfaces

## Semantic descriptions of sound
- SAFE: A SYSTEM FOR THE EXTRACTION AND RETRIEVAL OF SEMANTIC AUDIO DESCRIPTORS
- Semantic Description of Timbral Transformations in Music Production
- SocialFX: Studying a Crowdsourced Folksonomy of Audio Effects Terms
- Speaking about sounds: A tool for communication on sound features
- Timbral Attributes for Sound Effect Library Searching
- Word Embeddings for Automatic Equalization in Audio Mixing

## Deep Learning for Synthesizing Audio
- Adversarial Audio Synthesis (WaveGAN)
- AudioGen: Textually Guided Audio Generation
- WaveNet: A Generative Model for Raw Audio

## Deep Learning for Audio Style Matching
- Blind Arbitrary Reverb Matching
- One-Shot Parametric Audio Production Style Transfer with Application to Frequency Equalization
- Style Transfer of Audio Effects with Differentiable Signal Processing

## Differentiable Digital Signal Processing
- DDSP: Differentiable Digital Signal Processing
- Differentiable Signal Processing With Black-Box Audio Effects
- Lightweight and Interpretable Neural Modeling of an Audio Distortion Effect Using Hyperconditioned Differentiable Biquads

## Autoencoders
- $\beta$-VAE: Learning Basic Visual Concepts with a Constrained Variational Framework









