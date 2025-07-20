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


# Datasets



# Quantitative Results


# Qualitative Results
