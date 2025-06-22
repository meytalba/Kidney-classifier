# Kidney CT classifier

A deep learning-based tool designed to automatically classify kidney CT scans as normal or abnormal (presence of findings such as tumors or cysts).

# Project Overview
This project utilizes medical imaging data from the KiTS23 Kidney CT dataset, divided into two categories:

•	Normal scans

•	Abnormal scans (tumor or cyst present)

The model was trained using the EfficientNetB3 architecture with the following data split:
•	80% training
•	10% validation
•	10% testing

# Model Performance
Metric	Value
Accuracy	96.90%
AUC	0.9956
Precision	97.93%
Recall	96.59%

# Model Architecture – Why EfficientNetB3?
EfficientNetB3, developed by Google AI, is a convolutional neural network architecture known for achieving high accuracy with low computational overhead. It uses compound scaling to balance network depth, width, and image resolution.
Reasons for using EfficientNetB3 in this project:

•	High-resolution feature extraction, essential for identifying small abnormalities

•	Strong generalization on smaller datasets, important for medical applications

•	Efficient resource usage, allowing practical deployment in research and clinical settings

These capabilities helped the model detect subtle differences in kidney tissue, resulting in high classification performance.
Dataset – KiTS23

The project is based on data from the 2023 Kidney and Kidney Tumor Segmentation Challenge (KiTS23). This publicly available dataset includes:

•	489 annotated kidney CT scans

•	Expert segmentations of kidneys, tumors, and cysts

KiTS23 supports the development of automated kidney disease detection systems and serves as a benchmark dataset in medical imaging research. Kidney cancer affects over 430,000 people annually and causes approximately 180,000 deaths worldwide.
Intelligent Decision Support

The classifier integrates a triage system to support clinical decision-making:

•	If a scan is predicted as normal with high confidence (≥70%), the result is considered reliable.

•	If predicted as normal but with low confidence, the scan is flagged for radiologist review.

•	If predicted as abnormal, the scan is automatically flagged for clinical attention.

This approach helps ensure that uncertain or high-risk cases are not missed, supporting timely and accurate diagnosis in clinical workflows.


