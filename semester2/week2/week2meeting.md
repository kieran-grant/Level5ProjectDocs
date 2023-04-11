# Meeting 16/01/2023

## Minutes
- Went through slides and discussed progress in the last week.
- Discussed training VAE progress.
- Latent space doesn't look as though it has much meaningful structure - should see some clustering between the effects.
- Need to simplify training with more debugging to make sure VAE is learning meaningful representation.
- Try 2 DAFX that are quite different with **fixed** parameter settings. 
- Run training for longer.
- Store each feature separately and run dimensionality reduction on each separately and together to make sure there is something to learn.
- Can also try PCA or TSNE for dimensionality reduction.
- Can also try subtracting feature vectors, rather than concatenating.
- Try a smaller dimensionality in latent space (32D or even 16D)?
- Need to check the range of values the audio embeddings and AudioCommons features take, and how this might affect reconstruction loss.

## To-do for this week 
- Run the above training for the VAE.
- Make lots of visualisations to bring to the meeting next week.
- Make a plan for model evaluation.
- Start report document.  