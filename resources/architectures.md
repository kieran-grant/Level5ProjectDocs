# Neural Synthesis Model Architectures

## Strided Convolution Models (SING, MCNN, WaveGAN)
> Models generate waveforms in the time domain using overlapping frames.

***Pros***:
- ...

***Cons***: 
- Model must align waveforms across frames.    
  - Audio oscillates at many frequencies with different phases. 
  - Model must align waveforms between these frames and learn filters to cover all possible phase variations.

--- 

## Fourier-based Models (Tacotron, GANSynth)
> Models generate waveforms in the frequency domain by predicting the relevant Fourier coefficients.

***Pros***:
- ...

***Cons***: 
- Similar phase alignment problem to strided convolution models above.  
- Must content with spectral leakage, where multiple sinusoids at neighboring frequencies and phases are combined to crete single sinusoid when Fourier basis frequency does not perfectly match audio.

--- 

## Autoregressive Waveform Models (WaveNet, SampleRNN, WaveRNN)
> Produce waveforms a single sample at a time based on preceding samples.

***Pros***:
- Can express arbitrary waveforms since it predicts one sample at a time.

***Cons***: 
- Generally large and require lots of data to train, also means that inference is slow (unusable in real-time).
- Some bias during generation due to teacher-forcing.
- Also incompatible with perceptual losses such as spectral features and discriminators. 

--- 

## Oscillator models (vocoders, synthesizers)
> Directly generates audio with oscillators.

***Pros***
- Use experts to fine tune synthesis parameters.
- Interpretable (parameters like loudness and frequency).
- Neural networks can be used to model pre-extracted synthesis parameters.

***Cons***
- Models cannot be trained end-to-end.
- Analysis parameters must be tuned by hand.
- Small errors in parameters can lead to large errors in the audio (since no back propagation can be performed).
  
--- 

## Spectrogram models (SpecGAN)
> Uses spectrograms from audio to train models using computer vision techniques. 

***Pros***:
- Can leverage techniques from computer vision which is generally more advanced than audio.
- Possibly the lowest maintenance in terms of feature engineering, can just pass in the unstructured data and train a NN.

***Cons***:
- Spectrograms difficult to invert?

--- 

## Differentiable DSP models 
> Use differentiable implementations of classical DSP methods to be trainable using backpropogation.

***Pros***:
- Can use structural priors to create higher fidelity sound and lower training times.
- Highly interpretable.
- Can be used with a variety of other architectures such as GANs and Diffusion models.

***Cons***:
- Requires a new differentiable implementation of each effect that needs to be modelled.  
- Can't take advantage of existing generic plugins as the model is trained with the specific DDSP modules.