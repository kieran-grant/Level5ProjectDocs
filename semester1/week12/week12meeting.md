# Meeting 05/12/2022

## Minutes
- Went through slides and discussed progress in the last week.
- DrumGAN method for preserving ordering is interesting - can use in my project.
- Discussed plan for next week:
  - For finding effects that just create noise, look at extreme changes in data. E.g. variance per frame, big changes in MFCCs.
- Interim report feedback:
  - Section 2 good, should preserve this.
  - Diagrams very helpful.
  - Literature review:
    - Some spelling errors: m/s instead of milliseconds, diluted - give it another proof read.
    - When discussing disentanglement, name $\beta$ as the single hyperparameter.
    - Reverb is long-time dependencies, but typically linear. Distortion is typically non-linear, fix this in report.
    - Section 3.5 is a little bit sparse. Maybe think about grouping class of evaluation methods in to those used during training/evaluation and those that are done after model training (listening tests).
      - Think about MFCC comparisons etc.
  - Section 4, probably remove personal development.
  - 4.3 - be more precise. Each bulletpoint should be roughly double the length.
  - In general, use author/paper name rather than saying 'in [1] we see that ...'.
  - Replace tubulation with tabulation.
  - Add severity and liklihood in risks section.
- A thought for final report - how to *show* effects as spectrogram? Other visual representations?

## To-do for this week 
- Finish SPSA example discussed last week.
- Create small ‘test’ dataset using generation method, check that parameter values are sensible (i.e. not silence or just noise).
- Start implementation of data preprocessing (including AudioCommons feature extractor) and dataset loading into model.
- Start implementation of DAFX into model with SPSA.
- Second draft of interim report.
