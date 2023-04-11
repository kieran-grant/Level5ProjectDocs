# Expert Evaluation Plan

- Read ethics.
- Use overdrive (best val-loss seen VTCK), Multi-Band (best val-loss unseen VTCK).
- Create spreadsheet to save answers.

## For each effect
- `N_SUPERVISED_POINTS = 0`
- `COLOUR = None`

### Test 1
- Points A and B in the latent space, play audio (extreme points on x, y axis)
  - Ask user to think about point C in latent space in between
  - Play sample
  - How well does the effect match your expectations?
  - Do this in plotly
  - 3x for each effect

### Test 2
- Let user interact with latent space for a couple of minutes
- Pick initial point in latent space (predetermined)
- After each adjustment, as the user:
  - How well did the change match your expectation? Between 1 and 10.
  - Overdrive:
    - Make this audio twice as distorted.
    - Make this audio half as distorted.
    - Make this audio as distorted as possible.
    - Apply as little distortion as possible to this audio.
  - MultiBand:
    - Make the initial audio slightly brighter.
    - Make the initial audio much brighter.
    - Make the initial audio slightly bassier.
    - Make the initial audio much bassier.
