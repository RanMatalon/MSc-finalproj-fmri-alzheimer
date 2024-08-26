# MSc-finalproj-fmri-alzheimer
My MSc final project, predicting and analyzing Alzheimer disease through MRI and fMRI.

To uncover patterns in neuroimaging data for diagnosing Alzheimer disease (AD) among older adults, researchers have explored range of statistical methods and machine learning algorithms.

In our research, we examined various deep learning models: (i) 3D-CNN (Convolutional Neural Network) for MRI (2600 SUBJECTS, 3 categories: CN, MCI, AD)), with emphasize on the benefit of dropout layers. (ii) Vision transformer and 2D-CNN for processed and reduced dimensionality fMRI data that included time and ROIs (Regions of Interest), and 3D-CNN for MRI (155 subjects, 2 categories, HC and MCI). The 3D-CNN achieved 84.7% accuracy (chance-level 33%). Interestingly, using fMRI to detect the Alzheimer's stage in individual patients, 2D-CNN achieved up to 95.6% accuracy (chance-level 50%), surpassing 3D-CNN on the same MRI data (75%). Thus, fMRI seems promising in distinguishing between healthy controls to those with cognitive impairments, demonstrating its potential as a valuable tool in clinical applications. Additionally, we extracted the activation patterns of the trained 3d-CNN layers, as a tool that could pinpoint to the regions involved with the progress of Alzheimer's Disease. These findings contribute the understanding of the disease and offer practical applications for early diagnosis and patient care.

3D CNNs are powerful tools for analyzing volumetric data, excellent at capturing local spatial features:

![image](https://github.com/user-attachments/assets/1fd8dcb8-a60e-454d-93fb-b7b17c08afa0)

Vision transformer (ViT) offers an efficient, interpretable, and scalable solutions for predicting AD from MRI and fMRI data.
The image is divided into fixed-size patches, each of which is linearly embedded. Position embeddings are added to the embedded patches to preserve spatial information. The resulting sequence of vectors is then fed into a standard Transformer encoder. The encoder sends the encoded data sequentially, making it easy to the multi-head attention head to find trends and connections in the image's sequence in space/time. To perform classification, an additional learnable "classification token" is appended to the sequence.

![image](https://github.com/user-attachments/assets/e8c2ecd4-c728-4d53-8e13-7ab73e9a4061)

LSTM (Long Short-Term Memory) is a type of RNNs (Recurrent Neural Network) that can detain long-term dependencies in sequential data) Integrating information from multiple modalities (fMRI, structural MRI, PET) .
The model is beneficial in capturing temporal dependencies in sequential data, while ignoring noise (not important data or dependencies).
LSTM mechanisms from natural language processing domains, implemented in transformers, were explored for Alzheimer's prediction. Transformer-based models, such as TrasforMesh and an optimized vision transformer (OViTAD), demonstrated capabilities in longitudinal modeling and 3D data analysis.[

![image](https://github.com/user-attachments/assets/512264af-d45e-49b2-a555-3a9b4049dcce)

The MRI dataset used in this project belongs to ADNI (Alzheimer’s Disease Neuroimaging Initiative), which is a major research project aimed at studying Alzheimer's disease. link to ADNI : adni.loni.usc.edu

The fMRI data was given and pre-processed by Dr. Gergo Bolla  from Semmelweis University, Budapest, Hungary.
Participants in this dataset were tested in ADNI too.
This data is divided into 2 classes – HC (Healthy Control) and MCI which was discussed earlier,
Any file is a 4D nii file (3D image with a measure of time).
We were blessed to cooperate with Dr. Bolla who helped us in this project, and we were inspired  
a lot from his article that aimed to diagnose and compare ML models for MCI detection.
