**Given:** a dataset of audio recordings.

**Define:**
- *Audio dir*: Path to top level of audio dataset
- *Input dir*: List of paths to the directories containing input audio files
- *Subset*: One of "train", "val", "test"
- *Length*: Number of samples to lead for each example, default 65536
- *Train ratio*: the % of the dataset to use for training (default 0.8).
- *Val ratio*: the % of the dataset to use for validation (default 0.1).
  


Steps taken at AudioDataset initialisation:
- Get ***all*** filepaths for files.
- Split files depending on set (`split_dataset` function) and return related filenames.
- Setup dict `input_files`
- Get details about the audio files:
  - Filename
  - Load in audio to AudioFile class (get channels, frames etc).
  - If number of frames is less than 2*length: skip
  - Otherwise `input_files[file_id] = audio_file`
  - Keep track of frames to report total audio length


Steps taken at AudioDataset `__getitem__`:
- `generate_pair`
  - Select random file
  - Get random patch of size length*2
  - Peak normalise
  - Add audio augmentations
  - Apply frequency and compression corruption
    - 'Random' settings - in practice hand-chosen settings.
    - Need something similar for hand chosen effects.
  - Clone to create target
     - Apply frequency and compression corruption
- `conform_length` for x and y
  - Just pad or cut if length isn't right
- `linear_fade` for x and y
  - Apply 50ms of fade to audio
- Normalise to -12 dBFS

Steps taken during training:
- Split track in half and randomly select one side as input and other as reference.
- Run forward pass on input and reference.
  - Resample if required
  - Run x and y through encoder
  - Run encodings through controller
  - Process audio based on parameters (once for each channel)
- Calculate reconstruction loss between predicted y and ground truth.
- Return loss and data dictionary with: x (input), y (ground truth), p (parameter vector), e (latent embedding of input) and y_hat (model prediction)