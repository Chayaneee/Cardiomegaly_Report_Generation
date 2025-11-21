# Cardiomegaly_Report_Generation
Generating Clinically Relevant Reports from Chest X-Rays for Cardiomegaly Diagnosis

# Introduction
This repository contains the official implementation of our research work on generating clinically relevant radiology reports for cardiomegaly diagnosis from chest X-rays. Cardiomegaly, or an enlarged heart, is commonly assessed using the cardiothoracic ratio (CTR)—a geometric measurement comparing the width of the heart to the width of the thoracic cavity. Unlike large language models (LLMs) and vision-language models (VLMs), which often fail to capture such explicit geometric cues, our approach directly integrates CTR estimation into the report generation process.

🔍 Key Contributions:

1. CTR Annotation Set: We introduce a novel cardiomegaly-focused annotation set built from the MIMIC-CXR dataset, comprising 300 manually annotated bounding boxes for the heart and thoracic cavity.

2. YOLOv11-Based Detector: A customized YOLOv11-based object detector is trained to localize the heart and thorax, achieving >99% AP@50 on our annotation set.

3. CTR-Driven Report Generation: We incorporate the computed CTR into a Vision Encoder-Decoder (VED) report generation pipeline, allowing the model to produce more accurate and clinically meaningful cardiomegaly descriptions.

While ground-truth CTR labels are not available in MIMIC-CXR for quantitative validation, our qualitative analysis demonstrates that CTR-guided reporting yields improved clinical alignment and interpretable severity grading for cardiomegaly.

# Proposed Workflow
<img width="9210" height="6374" alt="Image" src="https://github.com/user-attachments/assets/77b62c94-0922-45e2-8db5-52ade4d55635" />
# Object Detection Pipeline
<img width="6145" height="1579" alt="Image" src="https://github.com/user-attachments/assets/3cd0f89a-6dcb-4703-9acf-9f4affe46c08" />


# Datasets
We have used two publicly available datasets for this experiment.
  - [MIMIC-CXR](https://physionet.org/content/mimiciii-demo/1.4/)
  - [VinDr-CXR](https://vindr.ai/datasets/cxr)
    
# Cardiomegaly Annotated Dataset
  - [VinDr_cxr_cardiomegaly_annotations](https://github.com/kaichenchai/vindr_cxr_cardiomegaly_annotations)
    
# Customised MIMIC-Cardiomegaly Dataset Preparation
<img width="789" height="403" alt="Image" src="https://github.com/user-attachments/assets/be9d42d5-08b7-45d2-8785-b903d6c4c08e" />

[Customised Mimic-Cardiomegaly Dataset](https://huggingface.co/datasets/ChayanM/MIMIC-Cardiomegaly-Dataset)


# Quantitative Results

| **Word-Overlap** | Result | **Semantic Similarity** | Result | **Classification Accuracy** | Result | **Clinical Evaluation** | Result |
| ---------------- | ------ | ----------------------- | ------ | --------------------------- | ------ | ----------------------- | ------ |
| BLEU-1           | 0.257  | ST                      | 0.846  | Accuracy                    | 0.918  | RadGraph-F1             | 0.510  |
| BLEU-2           | 0.227  | EmbedAvg                | 0.725  | WA-F1                       | 0.918  | RadGraph-Precision      | 0.489  |
| BLEU-3           | 0.208  | VE                      | 0.591  | WA-Precision                | 0.920  | RadGraph-Recall         | 0.485  |
| BLEU-4           | 0.180  | GM                      | 0.827  | WA-Recall                   | 0.918  | GREEN                   | 0.701  |
| METEOR           | 0.516  | —                       | —      | —                           | —      | —                       | —      |
| ROUGE-L          | 0.522  | —                       | —      | —                           | —      | —                       | —      |
| CIDEr            | 2.913  | —                       | —      | —                           | —      | —                       | —      |



# Qualitative Results
<img width="6075" height="2778" alt="Image" src="https://github.com/user-attachments/assets/329ed362-b34c-4051-aa58-39ccb28dbba1" />
