# Datasets 

## SPICE
  - https://en.wikipedia.org/wiki/SPICE
  - Program used to model analogue circuits, frequently used in white-box approaches to VA modelling.

## SignalTrain: 
  - https://github.com/drscotthawley/signaltrain
  - https://zenodo.org/record/3348083
  - Very large dataset containing many hours of recordings using the LA2A dynamic compressor including full songs and individual instruments/voices.
  
## Freesound:
  - https://annotator.freesound.org/fsd/
  - Large collection of annotated audio snippets. 
  - Sometimes used alongside SPICE (clean DI'd guitar from FreeSound through SPICE simulation)

## IDMST-SMT-Guitar/Bass/Drums/Chords/Audio Effects:
  - https://www.idmt.fraunhofer.de/en/publications/datasets/guitar.html
  - https://www.idmt.fraunhofer.de/en/publications/datasets/bass.html
  - A number of very large dataset comprising of DI recordings of various instruments using different playing techniques and configurations of the instrument.

## AES Guitar Amplifier Sounds Dataset:
  - https://www.aes.org/e-lib/browse.cfm?elib=19754
  - Dataset contains five different styles of guitar sounds passing through different guitar amplifiers with 10 steps of a gain parameter.
  - Input/output also provided in matrix form.
  
## NSynth:
  - https://magenta.tensorflow.org/datasets/nsynth
  - Very large dataset containing >300k musical notes, with unique pitch, timbre and envelope.
  - Notes are from 1006 instruments available from sample libraries and for each there is a 4 second, **16kHz** sample at up to 88 pitches with 5 different velocities for each pitch.
  - Dataset includes annotations for sound qualities (bright, dark etc) and instrument families (guitar, organ, vocal etc).

## MusOpen:
  - https://musopen.org/music/
  - Database of royalty-free music recordings.
  - Mostly <20th century, but each recording includes tags for mood and instruments present.

## MagnaTagATune
- https://mirg.city.ac.uk/codeapps/the-magnatagatune-dataset
- Large corpus of audio (mostly classical) with user tags added.
- Most are genre/instrument tags, but some are timbre tags.

## SAFE-DB
- https://somagroup.co.uk/applications/safe-db
- https://github.com/semanticaudio/safe-api
- *Stables, Ryan et al. “SAFE: A System for the Extraction and Retrieval of Semantic Audio Descriptors.” (2014).*
- Database containing semantically annotated music production metadata, taken from an international group of sound engineers.
- Contains parameter values for 4 audio effects: compressor, distortion, parametric EQ and reverb.
- Each contains a string representing a user's description of the audio transformation (warm, bright, fluffy etc)

## SocialFx
- https://www.dropbox.com/sh/ns6r58ypvqqhnpl/AADkzuTih8O01aMgYRlKQt-ka?dl=0
- *SocialFX: Studying a Crowdsourced Folksonomy of Audio Effects Terms (2016)*
- Dataset was created by asking listeners to give descriptive words to how an effect changed an audio signal.
- Slightly different to SAFE-DB as it is aimed at non-musical participants (Amazon Mechanical Turk).
- Contains parameter values for each effect (EQ, compression and reverb).
- Could maybe be combined with SAFE-DB in some meaningful way?

## Other:
  - Some papers use custom datasets, either using physical analogue equipment or SPICE simulations.
  - These will be used with DI guitar/bass recordings or function generators.
  - For drum sounds, there are thousands of sample packs available online which are generally organised into categories (snare, kick, fx...) which would be suitable for training.

