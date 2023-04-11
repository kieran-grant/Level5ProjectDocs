# Meeting 06/03/2023

## Minutes
- Went through slides and discussed progress in the last week.
- Agreed that latent space doesn't look great
- Suggested revisiting architecture - should have spectrogram VAE recreate a single Spectrogram, rather than joint.
  - Then join for feed forward
- Also try lowering the dimensionality of the latent space to see if it helps
- Thinking about going forward - if a good (traversable) latent space cannot be found, just map parameters directly to low dimensional space and evaluate that.
- Evaluation plan is fine, but probably evaluating too much. The listening and user tests are probably the main focus.

## To-do for this week 
- Adjust architecture for single spectrogram VAE
- Train new VAE and make visualisations
- Work on latent control space (any libraries that let you interact with 2D plot?)
- 

