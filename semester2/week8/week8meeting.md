# Meeting 27/02/2023

## Minutes
- Went through slides and discussed progress in the last week.
- There is a slight concern that the biggest variation in latent dimension is volume. Need to make sure that latent representation is able to capture more than this.
  - Otherwise may need to retrain VAE and normalise spectrograms as well as fix output_db.
- Very little structure to Delay representation, not sure if much will be learnable.
- Should try with RingMod - might be a good one to show if different settings map differently to latent space.
- Potentially should log the current parameter settings of DAFX to match against reconstructions?
- Regarding question about training stability, can try:
  - Xavier initialisation with different parameters.
  - Try LayerNorm.
  - Can try a more extreme clamping than sigmoid.

## To-do for this week 
- Find some way to convince supervisors latent space is learning more that just volume. Use RingMod to see pair-plot domain colouring. Might need to think about retraining VAE.
  - If retraining the VAE, find some way to take out volume as much as possible. Normalise across spectrograms? Train with more effects?
- Finalise Evaluation plan.
  - Should include some usability test (with one or two experts -  Liam and James?).
- Can retry training with static delay params.

