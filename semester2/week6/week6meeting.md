# Meeting 13/02/2023

## Minutes
- Went through slides and discussed progress in the last week.
- Spectrograms *seem* to be working okay.
- Should just do some more verification on input and reconstructed spectrograms.
- Can use UMAP to map down to 2-8D for latent space then back up.

## To-do for this week 
- Check spectrograms are sensible.
  - Looks like there is a symmetry - check NN video.
  - Use inverse to check input and reconstructions.
  - Also check interpolation spectrograms, do they also make sense?
- Try unseen audio effects, do their latent embeddings make sense?
- Try with a single audio effect and apply 4/5 different settings. Where do they get mapped to?
- Continue with training of simple end-to-end network.
  - Need to think about settings to use, maybe a small subset for the moment?
