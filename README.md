### Code repository for the manuscript: "Impact of Mydriasis on Image Gradability and Automated Diabetic Retinopathy Screening with a Handheld Camera in Real-World Settings".

Authors: Iago Diogenes 1; David Restrepo 2,3; Lucas Zago Ribeiro 1; Andre Kenzo Aragaki 1; Fernando Korn Malerbi 1; Caio Saito Regatieri 1; Luis Filipe Nakayama 1,3
1.	Sao Paulo Federal University, Ophthalmology Department, Sao Paulo – SP, Brazil
2.	Laboratory of Mathematics and Computer Science (MICS), Centrale Supélec, Paris-Saclay University, Gif-sur-Yvette, France
3.	Laboratory for Computational Physiology, Massachusetts Institute of Technology, Cambridge, MA, USA

This project focuses on enhancing DR screening in resource-constrained settings by leveraging portable retinal cameras and artificial intelligence (AI). Specifically, it investigates the role of mydriasis (pupil dilation) in improving image quality and the subsequent performance of AI models in detecting DR.

## Project Purpose
Diabetic retinopathy (DR) is a leading cause of blindness globally, with a significant burden in low- and middle-income countries (LMICs) due to limited access to specialized ophthalmological care. This project explores the effectiveness of portable retinal cameras combined with AI to streamline DR screening processes. It specifically examines how mydriasis affects image quality and AI-based DR detection, aiming to optimize screening protocols in resource-limited environments.

## Methods
### Data Collection
* Participants: 327 patients undergoing retinal exams before and after mydriasis with Tropicamide 0.5% eyedrops.
* Imaging Protocol: Two images per eye (macula-centered and optic disc-centered) captured using the Phelcom Eyer portable retinal camera.
* Data Collected: Demographics (age, gender, race), clinical comorbidities (diabetes duration, systemic hypertension).

### Image Gradability Assessment
* Labeling: Two masked ophthalmologists independently graded images based on the ICDR score. A third specialist adjudicated disagreements.
* Gradability Criteria: Images were considered gradable if at least two-thirds of the retina were visible with adequate focus.
* Statistical Analysis: Logistic regression identified factors affecting image gradability, including age, gender, race, diabetes duration, and hypertension.

### AI Model Development
* Algorithm: ResNet-200d convolutional neural network (CNN) pre-trained on ImageNet.
Dataset:
* Training: mBRSET dataset (5,164 mydriatic retinal images).
* Validation: Study dataset with mydriatic and non-mydriatic images.
* Preprocessing: Resizing to 224×224 pixels, normalization, and data augmentation (flips, rotations).
* Training Parameters:
Loss Function: Cross-entropy loss
Optimizer: Adam
Epochs: 50
Batch Size: 4
* Performance Metrics: Accuracy, F1 score, Area Under the ROC Curve (AUC).
