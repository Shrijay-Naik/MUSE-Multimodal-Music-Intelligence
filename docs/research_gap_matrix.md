
# MUSE – Research Gap Matrix

## 1. Purpose

This document maps the research gaps identified in the reference systematic literature review to the proposed implementation and evaluation strategy of MUSE.

The objective is to ensure that every major project component has a clear research motivation and a measurable purpose.

## 2. Research Gap Matrix

| Research Gap | Problem Identified in Reference Paper | Proposed MUSE Implementation | Evaluation Strategy |
|---|---|---|---|
| Weak operationalization of meaning | Meaning is frequently reduced to task-specific labels such as sentiment, emotion, genre, or topic. | Develop a structured song interpretation using lyrical emotion, acoustic characteristics, and their relationship. | Examine prediction quality and whether the output captures meaningful differences between songs. |
| Dataset bias and cultural representation | Dominant languages and commercial music datasets may underrepresent local and culturally specific music. | Document dataset language, genre, source, and representation limitations. Investigate performance across available subsets. | Compare performance across available language or genre groups where sample sizes permit. |
| Evaluation inconsistency | Task-specific metrics do not necessarily establish semantic fidelity or generalization. | Establish separate evaluation protocols for lyrics-only, audio-only, and multimodal models. | Use appropriate classification metrics, confusion matrices, error analysis, and human assessment where feasible. |
| Limited interpretability | Multimodal systems may not explain how individual modalities influence predictions. | Present lyrical evidence and acoustic evidence associated with predictions. | Check whether explanations correspond to the inputs and model outputs. |
| Fragmented modality integration | Combining modalities does not necessarily explain how they jointly construct meaning. | Compare lyrics-only, audio-only, and multimodal predictions. Analyse agreement and disagreement. | Compare model performance and inspect cases where the modalities produce different predictions. |
| Weak pragmatic and functional modeling | Non-literal meaning, sarcasm, implicit meaning, and affective reversal remain under-modelled. | Investigate contextual lyrical interpretation as a possible extension. | Use manually reviewed examples or suitable annotated data if available. |
| Object-dependent methodological selection | Different semantic problems require different representations and methods. | Select separate methods for text processing, audio analysis, fusion, and explanation. | Justify each method according to its task and compare against appropriate baselines. |

## 3. Priority of Implementation

### Priority 1 – Essential

1. Dataset investigation and validation.
2. Lyrics preprocessing and representation.
3. Audio preprocessing and feature extraction.
4. Lyrics-only baseline.
5. Audio-only baseline.
6. Evaluation of both independent models.

### Priority 2 – Core Research Contribution

1. Multimodal fusion, if genuinely paired data is available.
2. Comparison of unimodal and multimodal performance.
3. Modality agreement and disagreement analysis.
4. Evidence-based explanations of predictions.

### Priority 3 – Advanced Extensions

1. Contextual and figurative lyric interpretation.
2. Cross-modal semantic retrieval.
3. Semantic search using natural-language queries.
4. Knowledge graph or structured semantic representation.

Advanced extensions will only be attempted after the core system works and has been evaluated.

## 4. Proposed System Output

For a song with available lyrics and audio, MUSE should aim to produce:

- Lyrics-based emotional interpretation.
- Audio-based emotional interpretation.
- Combined interpretation, if multimodal fusion is supported.
- Relevant acoustic characteristics.
- Relevant lyrical evidence.
- Confidence or uncertainty information.
- Explanation of agreement or disagreement between modalities.

The system must not assume that the emotion expressed by lyrics is identical to the emotion conveyed by the music.

## 5. Evaluation Plan

The proposed evaluation will distinguish between three experimental settings.

### Experiment A – Lyrics Only

Input: Song lyrics.

Output: Predicted emotional category or other defined semantic representation.

Possible metrics:
- Accuracy.
- Precision.
- Recall.
- Macro F1-score.
- Confusion matrix.

### Experiment B – Audio Only

Input: Song audio.

Output: Predicted emotional category or other defined acoustic interpretation.

Possible metrics:
- Accuracy.
- Precision.
- Recall.
- Macro F1-score.
- Confusion matrix.

### Experiment C – Multimodal

Input: Matched song lyrics and audio.

Output: Combined prediction and modality-level explanations.

Possible evaluation:
- Comparison against both unimodal baselines.
- Macro F1-score.
- Confusion matrix.
- Modality disagreement analysis.
- Human evaluation where feasible.

These are proposed evaluation methods, not achieved results. Final metrics will depend on the selected dataset and task formulation.

## 6. Critical Dataset Requirement

Multimodal experiments require genuine paired observations.

Each multimodal record must contain:

1. A valid audio recording.
2. The corresponding lyrics for that recording.
3. A reliable identifier connecting the two.
4. Suitable labels or a defensible annotation strategy.
5. Permission to use the material for the intended research and demonstration.

Audio-caption datasets must not be treated as lyric datasets.

Unpaired audio and lyrics must not be combined and presented as genuine song-level multimodal observations.

If a suitable paired dataset cannot be obtained, the research scope must be revised and the limitation explicitly documented.

## 7. Research Contribution

MUSE aims to investigate whether combining linguistic and acoustic representations can provide a more informative and interpretable account of musical emotion than either modality alone.

The proposed contribution is an applied comparison of unimodal and multimodal approaches, supported by modality-level analysis and evidence-based explanations.

Any claim of improved performance or semantic understanding must be supported by experimental results.

## 8. Current Status

- [x] Reference research gaps identified.
- [x] Research gaps mapped to proposed features.
- [x] Initial implementation priorities defined.
- [x] Evaluation strategy proposed.
- [ ] Dataset feasibility verified.
- [ ] Final research contribution approved.
- [ ] System architecture finalized.
