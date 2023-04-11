# Meeting 09/01/2023

## Minutes
- Went through slides and discussed progress in the last week.
- Discussed training VAE:
  - Should use a few different effects that are representative of those that are to be used.
  - Run each effect for a few epochs before switching out for something else.
  - Can have 1 'meta effect' which selects an effect then applies some preset to the audio.
  - Probably want somewhere between 12 and 100 presets for an effect.
  - Can add some noise during training to change these slightly.
- Visualisation of trained VAE:
  - If 2/3D can visualise directly.
  - If more (but not too many) can use a pair-plot to visualise pairs of dimensions.
- Mapping latent space to parameter settings.
  - Use something like UMAP to map from 64D to 2-8D.
  - Then a small feed forward network to the parameter settings.
- Schedule:
  - Want to wrap up implementation in the next month.
  - Think about how you're going to evaluate the results.
  - Should be running last experiments at end of March at the latest.
  - Writing up should be okay, should start early.
- Need to get an idea of how long training is going to take.

## To-do for this week 
- Implement VAE training.
- Get an idea of how long training might take.
- If trained - start visualisations.