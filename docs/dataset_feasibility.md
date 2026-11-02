
# MUSE – Dataset Feasibility Investigation

## 1. Objective

Identify datasets suitable for developing and evaluating:

- Lyrics-only music emotion analysis.
- Audio-only music emotion analysis.
- Multimodal music emotion analysis using corresponding audio and lyrics.

The primary requirement for multimodal experiments is reliable audio-lyrics pairing.

## 2. Dataset Candidates

### 2.1 MERGE Dataset

Source: https://zenodo.org/records/13939205

Description:
MERGE is a music emotion recognition dataset containing audio, lyrics, and paired audio-lyrics collections.

Reported sample counts:

| Collection | Complete | Balanced |
|---|---:|---:|
| Audio | 3,554 | 3,232 |
| Lyrics | 2,568 | 2,400 |
| Bimodal | 2,216 | 2,000 |

Available information:
- 30-second audio excerpts.
- Full lyrics in the relevant lyrics collection.
- Arousal and valence annotations.
- Four emotion quadrants based on Russell's Circumplex Model.
- Predefined training, validation, and test splits.

Advantages:
- Directly relevant to multimodal music emotion recognition.
- Provides separate collections for unimodal and bimodal experiments.
- Includes a balanced paired dataset.

Limitations and checks:
- Verify the license and permitted use of the audio and lyrics.
- Inspect the actual file structure and metadata.
- Confirm that audio and lyrics are correctly matched.
- Check missing values and duplicate records.
- Understand the annotation method and emotion label distribution.

Initial assessment: Strong primary candidate, pending license and data validation.

### 2.2 DEAM Dataset

Source: https://cvml.unige.ch/databases/DEAM/

Description:
DEAM contains 1,802 music excerpts and full songs annotated with valence and arousal, both continuously and at song level.

Potential use:
- Audio-only experiments.
- Acoustic feature extraction.
- Valence-arousal prediction.

Limitation:
It does not provide the corresponding song lyrics as its primary paired modality.

Initial assessment: Useful secondary audio dataset.

### 2.3 Song Interpretation Dataset

Source: https://zenodo.org/records/7019124

Description:
Contains audio excerpts from 27,834 songs, metadata, and approximately 490,000 user interpretations of lyrics.

Potential use:
- Investigating contextual song interpretation.
- Exploring relationships between music and human interpretations.

Limitation:
User interpretations are not equivalent to the original song lyrics or emotion labels.

Initial assessment: Possible advanced research resource, not the primary emotion classification dataset.

### 2.4 MVEmo Dataset

Source: https://huggingface.co/datasets/NEXTLab-ZJU/MVEmo

Description:
Contains 11,764 music-video samples with static and dynamic emotion annotations.

The dataset description reports:
- Lyrics for 7,923 samples.
- No lyrics for 3,841 samples.
- Music and video modalities.
- Static and dynamic emotion information.

Potential use:
- Alternative multimodal research.
- Investigation of dynamic emotion over time.

Limitations:
- Music-video samples are not automatically equivalent to clean audio recordings.
- Missing lyrics must be handled.
- Download and use conditions must be reviewed.
- Modality alignment and data availability need verification.

Initial assessment: Alternative candidate for further investigation.

### 2.5 MusicCaps Dataset

Source: https://huggingface.co/datasets/google/MusicCaps

Description:
Contains 5,521 music examples with natural-language captions describing musical properties.

Potential use:
- Audio-text semantic retrieval.
- Audio captioning experiments.

Limitation:
Captions describe audio. They are not the original lyrics sung in the recording.

Initial assessment: Optional future extension, not a substitute for paired lyrics.

## 3. Initial Dataset Decision

MERGE is selected as the first dataset to investigate because it provides a dedicated bimodal collection containing audio and lyrics.

The balanced bimodal collection contains 2,000 samples according to its Zenodo description.

This is a provisional selection, not a final approval for model training.

The following conditions must be satisfied first:

1. Confirm usage and licensing permissions.
2. Download the dataset from its official source.
3. Inspect the directory and file structure.
4. Verify the audio-lyrics mapping.
5. Examine annotation quality and label distribution.
6. Check data completeness and duplicates.
7. Confirm the available train, validation, and test splits.

## 4. Proposed Experimental Dataset Strategy

If MERGE passes validation:

### Experiment A: Lyrics Only
Use the corresponding lyrics collection.

### Experiment B: Audio Only
Use the corresponding audio collection.

### Experiment C: Multimodal
Use the paired bimodal collection.

All three experiments must use compatible labels and carefully controlled evaluation splits when they are compared directly.

If dataset splits differ, the comparison must use a common set of sample identifiers or another defensible evaluation design.

## 5. Data Governance

Before downloading and processing any dataset:

- Record the original source and citation.
- Read the license and terms of use.
- Record the dataset version.
- Do not redistribute copyrighted recordings or lyrics without permission.
- Do not upload raw dataset archives to the public GitHub repository.
- Keep raw and processed data separate.
- Document all transformations.

## 6. Dataset Storage Plan

The proposed local structure is:

MUSE/
    data/
        raw/
        processed/
        external/

Raw data must remain unchanged.

Processed data will contain cleaned and transformed records.

External data will contain references or supporting resources from other datasets.

Large data files will not be committed to GitHub.

## 7. Final Feasibility Status

- [x] Identified a primary paired dataset candidate.
- [x] Identified an audio-only candidate.
- [x] Identified alternative multimodal candidates.
- [x] Distinguished audio captions from actual lyrics.
- [ ] Confirm dataset licensing.
- [ ] Download and inspect the selected dataset.
- [ ] Validate audio-lyrics correspondence.
- [ ] Validate emotion annotations.
- [ ] Finalize dataset selection.

## 8. References

1. MERGE Dataset. https://zenodo.org/records/13939205
2. DEAM Dataset. https://cvml.unige.ch/databases/DEAM/
3. Song Interpretation Dataset. https://zenodo.org/records/7019124
4. MVEmo Dataset. https://huggingface.co/datasets/NEXTLab-ZJU/MVEmo
5. MusicCaps Dataset. https://huggingface.co/datasets/google/MusicCaps
