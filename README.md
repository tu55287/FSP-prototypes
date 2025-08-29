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
- Prototype-based frame identification using DistilBERT span encoders, covering the full 1,014-frame inventory of FrameNet 1.7.  
- Prototypes constructed via mean pooling; optionally extended with clustering-based multi-prototypes.  
- Few-shot regimes (3/5/10-shot) to test data efficiency and frame-specific variability.  
- Training with temperature-scaled similarity scores, cross-entropy loss, and a lightweight separation regulariser.  
- Stratified evaluation across frame frequency groups (rich, medium, poor, very poor).  
- Cross-dataset testing on both the Original and Fulltext splits.  

## Key Contributions
- **Comprehensive prototype framework**: First systematic application of prototype learning to frame semantic parsing, achieving 97.20% Top-1 and 99.31% Top-3 accuracy on FrameNet 1.7.  
- **Architectural minimalism**: Lightweight design using standard Transformer encoders (DistilBERT), requiring no complex modifications or heavy hyperparameter tuning.  
- **Transparent inference**: Frames predicted via similarity in a shared semantic space, enabling ranked predictions and confidence-based filtering.  
- **Empirical insights**:  
  - Single-prototype schemes outperform multi-prototype alternatives.  
  - DistilBERT offers competitive performance with reduced computational cost.  
  - Cross-entropy loss is more critical than separation loss for frame prediction.  
  - Few-shot learning remains challenging, with ~10 examples per frame needed on average.  
- **Future extensions**: Prototype learning for frame element identification, cross-lingual alignment, unsupervised frame discovery, and improved generalisation for low-resource and novel frames.  


## Citation
If you use this repository in your research, please cite:

Yu, Chao. (2025). *Prototype Learning for Frame Semantic Parsing with Transformers*. Master’s Thesis, KU Leuven.
