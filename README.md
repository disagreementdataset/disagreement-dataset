
# Disagreement Dataset

## Repository Structure
- `Audio/`: The folder that contains the audio files for all clips. Clips are in `.wav` format, sampled at 16 kHz. Naming matches the `File name` column in `metadata.csv`.
- `Transcriptions/`: The folder contains automatic transcriptions at both the turn and word level
    - `Turn_Level_Transcriptions/`: This folder contains transcripts including each speaker turn for a given clip
    - `Word_Level_Transcriptions/`: This folder contains transcriptions with a row for each word and timing information.
  The `.csv` files have the same naming convention as the audio files.

- `metadata.csv`: This file contains the clip-level labels and `Fold` for the cross-validation protocol. See the column descriptions for 'metadata.csv' below. 


## Column Descriptions for `metadata.csv`
| Column       | Description |
|--------------|-------------|
| `File name`  | Unique identifier for each clip, beginning with the call name (e.g., `F01_1`) |
| `Item`       | The survival item being discussed in the clip |
| `Gender`     | Gender composition of the speakers (`MF` = Male and female, `MM` = both male, `FF` = both female) |
| `Rating`     | 'Disagreement' rating given to the clip (percentage of the time the speakers disagree). For classification, ratings < 26 are defined as 'Low Disagreement' and ratings ≥ 26 are 'High Disagreement'.|
| `Duration`   | Duration of the clip in seconds 
| `Call`       | Dyadic phone call the clip is from e.g. 'F01' |
| `Fold`       | Fold assignment for cross-validation protocol |
| `R Choice`   | Receiver's prior decision on whether to take the item (`Yes`/`No`) |
| `C Choice`   | Caller's prior decision on whether to take the item (`Yes`/`No`) |
| `Consensus`  | Final item selection decision made at the end of the conversation (`Yes`/`No`) |
