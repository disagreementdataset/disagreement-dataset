
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

## Paper

If you are using this dataset, please kindly cite this paper.

```bibtex
@inproceedings{10.1145/3716553.3750754,
author = {Buker, Areej and Smith, Emily and Perepelkina, Olga and Vinciarelli, Alessandro},
title = {Multimodal Analysis of Disagreement in Dyadic Conversations: An Approach Based on Emotion Recognition},
year = {2025},
isbn = {9798400714993},
publisher = {Association for Computing Machinery},
address = {New York, NY, USA},
url = {https://doi.org/10.1145/3716553.3750754},
doi = {10.1145/3716553.3750754},
abstract = {This article proposes a multimodal approach for the detection of disagreement in dyadic conversations, where disagreement means that people express different opinions about a topic under discussion. The key-assumption underlying the work is that people tend to manifest different emotions depending on whether they are disagreeing or not. Therefore, emotions can provide evidence that disagreement is taking place. The experiments were performed over a corpus of 684 clips involving 60 dyads (120 persons and roughly 8 hours of speech). Each clip revolves around a decision-making task and it is annotated in terms of the percentage of time people spend in disagreement. For the sake of reproducibility, the Glasgow Disagreement Corpus, the data used in the experiments, has been made accessible through a link available in the paper. The results show that a multimodal approach based on language and paralanguage can predict such a percentage with Mean Absolute Error 9.7 and correlation 0.52 between actual and predicted percentage of time spent in disagreement.},
booktitle = {Proceedings of the 27th International Conference on Multimodal Interaction},
pages = {228–237},
numpages = {10},
keywords = {Disagreement detection, multimodal analysis of language and paralanguage, dyadic conversations.},
location = {
},
series = {ICMI '25}
}

