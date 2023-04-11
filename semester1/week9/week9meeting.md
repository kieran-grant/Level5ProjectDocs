# Meeting 14/11/2022

## Minutes
- Went through slides and discussed progress in the last week.
- Discussed both architecture diagrams and their feasibility.
- Suggested that they can be combined:
  - Main idea is to have half the network which is pre-trained and frozen.
  - The other half takes the audio embeddings and maps to an arbitrary new audio effect.
- Discussed that diagrams are very useful for communicating ideas.

## To-do for this week 
- Think about the range of effects to use.
- What sort of parameters to model - all of them, some of them?
- How to load in plugins to network - Pedalboard or BB DDSP library?