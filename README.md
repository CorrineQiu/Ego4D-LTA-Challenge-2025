# The champion solution for Ego4D Long-Term Action Anticipation Challenge in CVPR 2025

## 📂 Data Preparation

### 1. Datasets
Supports **Ego4D**.  
Follow the official download instructions and organize under `./data`.

### 2. Feature Extraction

Run **Hand Object Detector**, **SAM2**, and **EgoVideo** in sequence, following their **official tutorials**, to obtain both **frame features** and **HOI (hand-object) features**.

## 🎯 Pretrained Models
Download and store all pretrained weights under:
```
/pretrain_model/
  ├── EgoVideo/
  ├── SAM2/
  ├── Hand Object Detector/
  └── fintuned Llama2 model/
```
## 🧩 Project Structure (minimal)
```
.
├── HandObject/ 
├── AntGPT_Inference/ 
├── pretrain_model/ 
└── data/                    
```

## 🤖 Running Experiments

### Stage 1: Hand-Object Semantic Action Recognition

For all **Stage 1** training and evaluation, please use the implementation from our **AAAI 2026 paper**:

HandObject module of **INSIGHT**: https://github.com/CorrineQiu/INSIGHT/tree/main/HandObject  

> Follow the repository’s README for environment setup, feature extraction, training, and evaluation.  

### Stage 2: Long-Term Action Anticipation

In **Stage 2**, we primarily utilize the released weights of a finetuned Llama2 model from **AntGPT** for inference.

## 🙏 Acknowledgements

We thank the authors of **[Ego4D](https://ego4d-data.org/)** for providing the open-source datasets that support our experiments.  

We also thank the developers of **[Hand Object Detector](https://github.com/ddshan/hand_object_detector)**, **[SAM2](https://github.com/facebookresearch/sam2)**, **[EgoVideo](https://github.com/OpenGVLab/EgoVideo)** and **[AntGPT](https://github.com/brown-palm/AntGPT/tree/main)** for their released pretrained models and codebases.  

## 🔖 License
[MIT License]()