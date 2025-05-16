# SLT_Challenge

This repo is part of the SLT challenge requirements for passing COM61005 
- **Team**: Yao Xiao, Paul Gering, Fritz Peters
- **Challenge**: PROCESS Challenge, ICASSP 2025 [[link](https://processchallenge.github.io/)]

## Process Challenge.
The PROCESS challenge was conducted as part of ICASSP 2025. It provides a novel speech data set of participants (HC, Mild Cognitive Impairment, Dementia) completing tasks routinely used in cognitive assessments: 
- Cookie Theft Picture Description task
- Semantic Verbal Fluency
- Phonemic Verbal Fluency

The challenge proposes two tasks:
1. **Classification**: Three-way classification (HC vs MCI vs Dementia)
2. **Regression**: Predicting an individual's MMSE score as a measure of their cognitive health.

## Our approach 
We focused on addressing the classification task by leveraging graphical representations of patient speech. Two approaches were implemented and tested. **Firstly**, we investigated the feasibility of using Graph Neural Networks (GNN) for the classification of diagnostic categories. Simple directed speech graphs were constructed as input for these GNNs. **Secondly**, we included more informative features of a patient's speech (lexical, phonetic, semantic) into the constructed graphs by weighing the graph's edges according to these features. Subsequently, graphical features were extracted and used in various classification models.

## Code overview
- **CTD_CIU_Distance.ipynb**: Extract sequence of CIUs from CTD and calculate distance between adjacent CIUs. 
- **gnn_classification_class_weights.ipynb**: Preprocess graphical data, and train and evaluate a GNN-based classifier with class weights added
- **PROCESS_METADATA_ALL.csv**:
- **graph_features_classification.ipynb**:
- **phonetic_similarity.ipynb**: Calculate phonetic similarity between adjacent words from the phonetic transcripts of the VFT and PFT tasks.
- **SemSimilarity.ipynb**: Calculate semantic similarity between adjacent words in VFT and PFT transcripts
- **phonetic_transcript.ipynb**: Convert participant transcripts into IPA transcriptions and save in new files.
- **extract_SFT.ipynb**: Pre-process transcripts and save in new file structure (to use with Montreal Forced Aligner )
- **two_stage_gnn_classification.ipynb**: Train and evaluate a two-stage GNN, which first distinguishes dementia from non-dementia participants and then classifies the  non-dementia group into healthy controls and mild cognitive impairment (MCI)
