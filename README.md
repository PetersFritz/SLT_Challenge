# SLT_Challenge

## Process Challenge git repo.


## Code overview
- **CTD_CIU_Distance.ipynb**: Extract seqeuence of CIUs from CTD and calculate distance between adjacent CIUs. 
- **gnn_classification_class_weights.ipynb**: Preprocess graphical data, and train and evaluate a GNN-based classifier with class weights added
- **PROCESS_METADATA_ALL.csv**:
- **graph_features_classification.ipynb**:
- **phonetic_similarity.ipynb**: Calculate phonetic similarity between adjacent words from the phonetic transcripts of the VFT and PFT tasks.
- **SemSimilarity.ipynb**: Calculate semantic similarity between adjacent words in VFT and PFT transcripts
- **phonetic_transcript.ipynb**: Convert participant transcripts into IPA transcriptions and save in new files.
- **extract_SFT.ipynb**: Pre-process transcripts and save in new file structure (to use with Montreal Forced Aligner )
- **two_stage_gnn_classification.ipynb**: Train and evaluate a two-stage GNN, which first distinguishes dementia from non-dementia participants and then classifies the  non-dementia group into healthy controls and mild cognitive impairment (MCI)
