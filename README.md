# Pig Face Detection with YOLOv8

A small computer vision project focused on detecting pig faces using YOLOv8.

## Project overview

This project explores a basic computer vision pipeline for precision livestock farming:

CVAT annotations → YOLO format → dataset preparation → model training → validation → inference

The project uses an annotated pig image dataset and fine-tunes a pretrained YOLOv8n model to detect pig faces.

## What I did

- Inspected CVAT XML annotations
- Converted bounding-box annotations from CVAT format to YOLO format
- Prepared a train/validation split
- Fine-tuned a pretrained YOLOv8n model
- Evaluated the model on a held-out validation set
- Ran inference and visualized predicted bounding boxes

## Results

The dataset contained 27 annotated images:

- Training: 21 images
- Validation: 6 images
- Classes: `pig_face`

Validation results:

- Precision: 0.993
- Recall: 0.375
- mAP50: 0.422
- mAP50-95: 0.177

Because the dataset is very small, these results should be considered a proof of concept rather than a robust benchmark.

## Example prediction

The trained model successfully detected pig faces and produced bounding-box predictions on validation images.

## Project structure

```text
precision-livestock-ai/
│
├── 06_annotation_conversion.ipynb
└── README.md
