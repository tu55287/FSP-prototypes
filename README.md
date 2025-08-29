# Frame Semantic Parsing with Prototype Learning

This repository contains the implementation and supplementary materials of the Master’s thesis **"Prototype Learning for Frame Semantic Parsing with Transformers"** by Chao Yu (KU Leuven, 2025).

## Repository Contents
- `Prototype_Learning_for_Frame_Semantic_Parsing_with_Transformers.ipynb`  
  Main Google Colab notebook implementing prototype-based learning methods for frame semantic parsing.
- `frame_performance_appendix.xlsx`  
  Supplementary appendix containing exemplar performance results.

## How to Run
1. Open the notebook in Google Colab.  
2. Enable GPU acceleration.  
3. Mount your Google Drive to store checkpoints and results.  
4. Download the required datasets from the [OpenSesame repository](https://github.com/swabhs/open-sesame) and place them in your working directory.

**Note**: The code has been primarily tested in Google Colab. Running locally may require additional setup.

## Method Overview
- Prototype learning for frame semantic parsing using DistilBERT as the encoder.  
- Multiple prototype construction strategies (single, clustered, few-shot).  
- Stratified evaluation across frame frequency groups.  
- Optional frame element (FE) analysis for discriminativeness.

## Citation
If you use this repository in your research, please cite:

Yu, Chao. (2025). *Prototype Learning for Frame Semantic Parsing with Transformers*. Master’s Thesis, KU Leuven.
