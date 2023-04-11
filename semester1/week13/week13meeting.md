# Meeting 12/12/2022

## Minutes
- Went through slides and discussed progress in the last week.
  - Just need to include Jonathan's feedback and hand it in!
- Not much feedback for interim report - pretty much ready for submission!
- GPU issue:
  - Can look at something like TorchSpy to see if any tensors are still on the GPU.
  - Alternatively run as separate process (using something like multithreading)
- Training VAE:
  - Probably just want to train reconstruction for VAE at first to learn a good autoencoder latent space.
  - Maybe down to a slightly higher number of parameters than final latent space (128/256?)
  - Use PCA and a bunch of input data to map down to 2 dimensions and check that latent space is kind of sensible.
- Think about if including phase in loss (say including complex coefficient as another channel) creates a better parameterisation.
- When choosing effect to use maybe start with:
  - Something with a single or very few parameters (low pass filter)
  - Then something non-linear (simple distortion etc)
  - Then something more complicated (multi-band compressor)

## To-do for this week 
- Complete and hand-in interim report.
- Finish data generation and preprocessing pipeline.
- Finish end-to-end model implementation.
