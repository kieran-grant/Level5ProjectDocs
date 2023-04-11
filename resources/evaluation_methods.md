# Evaluation methods

## Losses/objective functions
- Mean average error (MAE), mean squared error (MSE) and variants
- Error-to-signal ratio (ESR)
  - Usually used alongside pre-emphasis filters (first-order HP/LP, folded differentiator) to account for real-world perceptual accuracy.
- Short-term Fourier Transform (STFT)
  - Has also been combined with MAE.
- Multi-scale Spectral Loss (MSSL)
  - Used to compare spectrograms.
  - Aligns with perceptual loss.
- Frechet Audio Distance (FAD)
  - Reference-free and relates to human perception.
  - Used with generative models.
- KL-Divergence
  - Can be used with a classifier for audio data. 
  - Then feed it a real and generated sample to calculate divergence.

## Real-time capabilities
- Number of operations.
- Timing inference.
- Real-time factor ($RTF = \frac{\text{Processing Time}}{\text{RT Constraint}}$).

## Listening tests
- MUSHRA 
  - https://en.wikipedia.org/wiki/MUSHRA
- Aural comparison of prediction and target
- Web Audio Evaluation Tool
  - https://github.com/BrechtDeMan/WebAudioEvaluationTool

