# Meeting 06/02/2023

## Minutes
- Went through slides and discussed progress in the last week.
- Strange that KLD is causing issues, John has linked some resources to check implementation.
- Showed the following diagrams:
  - UMAP projection of raw spectrograms.
  - Spectrogram reconstruction.
    - Check scaling of images, do reconstructions have mean=0 and std=1, if not something is wrong!
    - Use same colourbar scale for all images.
  - Latent spectrogram embeddings linear neural net.
    - Shows some structure between effects.
- Discussed simplification of network -> removing audio encoder and using controller VAE directly as a convolution VAE.
  - Sounds like a good plan - less to debug.

## To-do for this week 
- Check reconstruction values of spectrograms, do they have mean=0 variance=1?
- Check implementation of VAE using: https://github.com/rasbt/deeplearning-models/blob/master/pytorch_ipynb/autoencoder/ae-var.ipynb
- Implement new, simplified network.
  - Use concatenation of complex spectrograms of input and reference pair. 
  - I.e. a 4-channel image where the channels are:
    - Input spectrogram: real coefficient.
    - Input spectrogram: complex coefficient.
    - Reference spectrogram: real coefficient.
    - Reference spectrogram: complex coefficient.
  - Double check settings for STFT, make sure they capture the effects!
