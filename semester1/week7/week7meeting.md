# Meeting 31/10/2022

## Minutes
- Went through slides and discussed progress in the last week.
- Talked about switching NLP for style transfer.
- Need to think about how to search for sounds which might be used for style transfer.
  - Extract audio descriptors and use those to filter?
- Think about decomposition problem for reference tracks.
  - May only want one part of song - section or instrument.
  - Use instrument separation layer?

## To-do for this week 
- **Priority**: make a diagram for the architecture of what you have in mind.
- How hard is it going to be to implement (good) audio effects.
  - Setting parameters to reasonable ranges etc.
  - Most are already differentiable, but require long dependencies.
- Look at *Style Transfer* codebase.
- Another style transfer paper?