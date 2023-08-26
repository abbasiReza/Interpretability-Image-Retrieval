# Interpretability in Histopathology Image Retrieval using GradCAM

## Description

This project aims to provide interpretability for a histopathology image retrieval system using gradient-weighted class activation mapping (GradCAM) techniques.

The image retrieval model is built on top of a previous project using self-supervised learning for histopathology image encodings. GradCAM is then applied on top of this model to understand why certain images are retrieved as being similar or dissimilar. 

Specifically, GradCAM generates heatmap visualizations highlighting important regions in the image for the retrieval task. This provides visual explanations for the model's outputs.

GradCAM, GradCAM++, and SmoothGrad methods are explored and evaluated.

## Image Retrieval Model

The image retrieval backbone uses [self-supervised learning models] to encode histopathology images. This model is pretrained and generates embeddings for indexing/retrieval.

## GradCAM Methods

- **GradCAM** - Uses gradients to identify important regions w.r.t the target output. 
- **GradCAM++** - An improvement to GradCAM to better highlight salient regions.
- **SmoothGrad** - Uses random sampling around an image to reduce noise in saliency maps.

These methods will be applied on the retrieval model to understand similar and dissimilar outputs.

## Datasets  

- [BracS](https://www.bracs.icar.cnr.it/) - Breast Cancer Histopathology Images
- [CRC](https://warwick.ac.uk/fac/cross\_fac/tia/data/extended\_crc\_grading/) - Colorectal Cancer Histopathology Images  
- [BATCH](https://iciar2018-challenge.grand-challenge.org/Dataset/) - BreAst Cancer Histology Images

## Usage

The system generates GradCAM visualizations on retrieved images to explain model outputs. Users can understand regions the model focuses on for judging similarity. 

Code is provided to generate GradCAM heatmaps and visualizations.

## References

- [GradCAM paper](https://arxiv.org/abs/1610.02391)
- [SmoothGrad paper](https://arxiv.org/abs/1706.03825)
