
# MUSE – Research Analysis

## 1. Research Reference

**Paper Title:** Semantic Mediation in Audio and Music Intelligence Through Natural Language Processing: A Systematic Literature Review

**Authors:** Novia Ratnasari and Aji Prasetya Wibawa

**Journal:** Natural Language Processing Journal, Volume 16 (2026), Article 100225

**DOI:** https://doi.org/10.1016/j.nlp.2026.100225

## 2. Research Motivation

Traditional audio and music analysis systems have often focused on acoustic characteristics, signal processing, and statistical pattern recognition.

However, musical meaning cannot always be understood through acoustic signals alone. Lyrics, language, emotional expression, context, and musical characteristics can interact to shape how listeners interpret a song.

The reviewed research indicates a shift towards integrating Natural Language Processing (NLP) into audio and music intelligence. Language is increasingly treated not merely as an additional input but as a mechanism for constructing, mediating, and explaining meaning across modalities.

## 3. Scope and Contribution of the Reference Paper

The paper presents a systematic literature review of 139 peer-reviewed journal articles published between 2021 and 2025.

It follows the PRISMA framework and examines research across three intersections:

1. NLP and Audio.
2. NLP and Music.
3. NLP, Audio, and Music.

Its purpose is to organize existing research, examine how linguistic functions are represented as computational tasks, and identify methodological and conceptual research gaps.

**Important:** This paper is a systematic literature review. It does not propose a specific MUSE architecture or provide a ready-made implementation to reproduce.

## 4. Major Research Gaps Identified

The following gaps are drawn from the review's discussion and Table 9.

### 4.1 Weak Operationalization of Meaning

Many systems represent meaning through task-specific labels such as sentiment, emotion, genre, topic, intent, or captions.

These outputs do not necessarily capture the relationships and context behind musical meaning.

**Implication for MUSE:** Explore representations that connect lyrical meaning with acoustic characteristics rather than relying only on isolated classification labels.

### 4.2 Dataset Bias and Cultural Representation

Existing datasets frequently favor dominant languages, commercial music, accessible audio collections, and curated benchmarks.

Local, low-resource, culturally specific, and non-mainstream contexts may be underrepresented.

**Implication for MUSE:** Document dataset language, genre, cultural coverage, and limitations. Avoid claiming broad cultural generalization without suitable evaluation data.

### 4.3 Evaluation Inconsistency and Limited Semantic Validation

Different studies use different datasets, tasks, metrics, and evaluation protocols.

High accuracy or F1-score does not necessarily prove that a model understands semantic meaning.

**Implication for MUSE:** Combine appropriate predictive metrics with semantic evaluation, error analysis, and human assessment where feasible.

### 4.4 Limited Interpretability and Traceability

Multimodal models may combine text and audio without clearly explaining how each modality contributes to the final output.

**Implication for MUSE:** Provide explanations showing which lyrical and acoustic evidence influenced a prediction.

### 4.5 Fragmented Modality Integration

Text, audio, lyrics, and other contextual signals are often combined as features without adequately explaining how they jointly construct meaning.

**Implication for MUSE:** Compare lyrics-only, audio-only, and multimodal approaches, and investigate when the two modalities agree or disagree.

### 4.6 Weak Pragmatic and Functional Modeling

Sarcasm, implicit meaning, affective reversal, and other non-literal expressions remain difficult to model.

**Implication for MUSE:** Treat contextual and figurative interpretation as an exploratory extension, not a capability we can claim without suitable data and evaluation.

### 4.7 Object-Dependent Methodological Selection

Different semantic problems require different representations and evaluation approaches. One method cannot address every semantic phenomenon.

**Implication for MUSE:** Select models and evaluation methods according to the particular task instead of using one model for every component.

## 5. Proposed MUSE Research Direction

MUSE (Multimodal Understanding and Semantic Exploration of Music) is proposed as an applied research-inspired system investigating how lyrical and acoustic information can complement one another when analysing music.

The system will investigate three main approaches:

1. Lyrics-only analysis: extracting linguistic and emotional information from song lyrics.
2. Audio-only analysis: extracting acoustic and musical characteristics from audio.
3. Multimodal analysis: combining the two representations and investigating their agreement, disagreement, and contribution to the final interpretation.

The system will also aim to make its outputs interpretable by presenting relevant textual and acoustic evidence.

This is an original applied implementation inspired by the research gaps identified in the reference paper. It is not a reproduction of the paper's experiments.

## 6. Initial Research Questions

**RQ1:** How effectively can NLP techniques extract semantic and emotional information from song lyrics?

**RQ2:** How effectively can acoustic features represent musical characteristics relevant to music understanding?

**RQ3:** Does combining lyrical and acoustic representations improve music emotion analysis compared with using either modality independently?

**RQ4:** How can the contribution of lyrics and audio to a multimodal prediction be explained to users?

## 7. Initial Project Objectives

1. Develop a text-processing pipeline for song lyrics.
2. Develop an audio-processing pipeline for extracting relevant acoustic features.
3. Establish separate lyrics-only and audio-only baselines.
4. Design and evaluate a multimodal fusion approach, subject to paired dataset availability.
5. Investigate agreement and disagreement between lyrical and audio-based predictions.
6. Develop an evidence-based explanation mechanism for model outputs.
7. Evaluate performance using suitable quantitative and qualitative methods.

## 8. Feasibility Risks and Constraints

The main implementation risk is obtaining a legally usable dataset containing genuinely paired song audio and corresponding lyrics.

Audio-caption datasets cannot automatically be treated as audio-lyrics datasets. Captions describe audio, while lyrics are the words sung in a song.

Before implementing multimodal fusion, the project must verify:

- Whether audio and lyrics refer to the same recording.
- Whether the pairing is reliable.
- Whether the data can legally be used for this project.
- Whether suitable emotion or semantic labels are available.
- Whether the dataset is large and diverse enough for meaningful evaluation.

If suitable paired data cannot be obtained, the project scope must be adjusted rather than fabricating pairs or presenting unpaired experiments as multimodal results.

## 9. Current Research Status

- [x] Reference paper identified.
- [x] Major research gaps extracted.
- [x] Initial research direction proposed.
- [x] Initial research questions drafted.
- [ ] Dataset feasibility investigation.
- [ ] Final problem statement.
- [ ] Finalized system scope and methodology.
