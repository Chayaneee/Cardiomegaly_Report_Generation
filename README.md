#Cardiomegaly_Report_Generation
Generating Clinically Relevant Reports from Chest X-Rays for Cardiomegaly Diagnosis

#Introduction
This is the official repository of our proposed research work entitled "Generating Clinically Relevant Reports from Chest X-Rays for Cardiomegaly Diagnosis" which focuses on cardiomegaly, a common thoracic condition where the cardiothoracic ratio (CTR)—a measurement derived from the width and height of the heart relative to the thorax—is an essential diagnostic metric. Unlike large language models (LLMs) or vision-language models (VLMs), which struggle to extract such precise geometric features, our approach explicitly incorporates CTR estimation into the report generation process. Our contributions are threefold: (1) we introduce a novel cardiomegaly-specific annotation set based on the MIMIC-CXR dataset, comprising 300 manually annotated bounding boxes of the heart and thoracic cavity; (2) we develop a YOLOv11-based cardiomegaly detector that achieves over 99\% AP@50 performance; and (3) we integrate the CTR computation into a Vision Encoder Decoder (VED)-based report generation model, enabling more refined and clinically aligned radiology reports. Although ground truth CTR values are not available in the dataset for quantitative evaluation, our qualitative results demonstrate that incorporating CTR enables more accurate and interpretable severity descriptions of cardiomegaly. This highlights the effectiveness of incorporating explicit anatomical measurements in enhancing clinical usability. 

#Proposed Workflow


#Datasets



#Quantitative Results


#Qualitative Results
