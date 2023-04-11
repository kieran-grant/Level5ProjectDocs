# Plan for remainder of the year

# Where would I like to be by the end of the year?
- Have a one-sentence description of the overall aim of the model.
- A convincing interim report which outlines where this project fits in with the rest of the field.
- Have the 'basic' architecture implemented:
  - Know what the inputs and outputs of the model will be.
  - Decide what the training data will look like.
  - Decide what loss functions will be applicable.
    - Parameter or audio domain?
    - Loss which makes the latent space in the VAE more useful?
      - KL-divergence?
      - $\beta$-VAE loss?
  - Model should be able to:
    - Take in an input and reference signal.
    - Calculate some embedding (using pretrained weights)
    - A VAE which takes these embeddings and predicts parameter values.

# How to get there

## Practical steps for model implementation.

1. Get Style Transfer code working.
    - Use the pre-trained weights to process data :white_check_mark:
    - Download (music) dataset. :white_check_mark:
    - Preprocessing/generation of training data.
    - Train model on small sample of dataset.
2. Check that pretrained weights can be loaded into encoder section - decide whether to use EfficientNet or MobileNet as fixed feature extractor.
3. Figure out how to load in arbitrary DAFX.
    - Either Pedalboard or BB-DDSP method.
    - What effects to use?
      - One at a time, or chain of effects?
      - What type of effects? Distortion, reverb, EQ, compression? 
      - Can use the SAFE-DB effects as a starting point or something 'friendlier' (i.e. something that doesn't crash DAWs)?
4. Implement custom numerical gradient for DAFX layer.
    - Can look at SPSA implementation of Style Transfer code.
    - Create 'toy' example in PyTorch. 

> **IMPORTANT:** try to do the training of the model using the small dataset again to test SPSA is working with arbitrary DAFX.

5. Replace the controller network with a VAE.
   - Use existing controller as basis for encoder part.
   - Think about what parts will be frozen when retraining with new DAFX.

## Getting a better understanding of the field
- Read about VAEs, understanding latent space.
- Other alternatives to style transfer with reference tracks:
  - Using emulations of sounds vocally.
  - Are there limitations to reference tracks?
    - Not one-to-one
    - May only wish to emulate one instrument.
    - No way to know what type of effects might be used.
    - Most are non-linear.


# For next semester
- How to give structure to the latent space?
  - Use some labelling from SocialFX or Safe-DB datasets?