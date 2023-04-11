# Meeting 23/01/2023

## Minutes
- Went through slides and discussed progress in the last week.
- Interim report looks good
- Discussed training VAE progress.
- Even with using the proper weights there is not much meaningful embeddings of audio with pretrained encoder.
- Could potentially be that encoder is only able to encode differences in EQ/compression.
- Can also try scaling embeddings for numerical stability.
- Feedback on evaluation plan:
  - Probably want some sort of user evaluation. Either a MUSHRA test with a few participants or me going through the latent space with an expert and judging whether transformations are valid.
  
## To-do for this week 
- Implement simple VAE and test that it works on an example VAE dataset (MNIST).
- Train this with Mel-spectrograms from audio.
- Check embedding of latent space and report visualisations.
- Try using test signals rather than audio dataset to simplify debugging further.
  