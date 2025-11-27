# NutriSight (Reference Repository)

![DRG4FOOD](https://img.shields.io/badge/DRG4FOOD-project-green)
![Status](https://img.shields.io/badge/status-reference-lightgrey)
![License](https://img.shields.io/badge/license-MIT-brightgreen)

NutriSight is a DRG4FOOD-funded project (Open Call #2), developed by Open Food Facts and El CoCo and carried out from **April 2024 to April 2025**.  
It delivers an open, multilingual AI model for automatically extracting nutrition values from photos of food packaging, helping to accelerate the enrichment of the global Open Food Facts database.

This repository serves as the official DRG4FOOD Toolbox reference for NutriSight.  
All code, models, datasets, and documentation remain hosted in the Open Food Facts repositories; this page provides a structured overview and direct links to those resources.

---

## Overview

NutriSight uses computer vision, OCR and layout analysis to read nutrition tables from packaging images and convert them into structured data.  
Integrated into the Open Food Facts contributor workflow, it reduces manual transcription time and improves accuracy across languages, markets and packaging formats.

This makes it easier for developers, researchers, and contributors to build trustworthy and transparent food-system applications.

---

## About the solution

When a contributor uploads a product image:

1. OCR detects text and bounding boxes.  
2. NutriSight analyses the layout and extracts nutrients and values.  
3. Confidence scores are provided for human validation.  
4. Validated values are added to the Open Food Facts database.

The model supports:

- multiple languages  
- varied table formats  
- per-100g and per-serving values  
- ambiguous units (kJ/kcal, ≤1g, multi-line formatting)

This strengthens fairness and inclusiveness in multilingual food data processing.

---

## Open-source components

NutriSight provides a complete open toolchain, including:

### Annotated multilingual dataset  
A professionally verified dataset of nutrition tables.  
HuggingFace dataset:  
https://huggingface.co/datasets/openfoodfacts/nutrient-detection-layout

### Nutrition extraction model  
LayoutLMv3-based model trained on the dataset.  
HuggingFace model:  
https://huggingface.co/openfoodfacts/nutrition-extractor

### Training scripts and dataset tools  
All dataset generation tools and training code:  
https://github.com/openfoodfacts/openfoodfacts-ai/tree/develop/nutrisight

### ML backend integration (Robotoff)  
Model integrated into the Open Food Facts ML backend:  
https://github.com/openfoodfacts/robotoff

### Validation tool ("Hunger Game")  
Interactive tool for validating extracted nutrition values:  
https://github.com/openfoodfacts/hunger-games/

### Predict API (OpenAPI specification)  
For programmatic prediction via Robotoff:  
https://openfoodfacts.github.io/robotoff/references/api/#tag/Predict/paths/~1predict~1nutrition/get

### Developer demo  
A simple usage demonstration for developers:  
https://github.com/openfoodfacts/openfoodfacts-ai/tree/develop/nutrisight#demo

### Scientific documentation and evaluation paper  
Technical paper describing the dataset, model architecture, and evaluation results, published for transparency and reproducibility.  
https://github.com/openfoodfacts/openfoodfacts-ai/blob/develop/nutrisight/paper/paper.pdf

---

## How you can use it

NutriSight can be applied in:

### Developer and research workflows  
- nutrition extraction  
- open food dataset enrichment  
- model retraining  
- benchmarking document AI systems

### Consumer and mobile apps  
- fast nutrition capture from photos  
- real-time enrichment of Open Food Facts

### Public health and policy contexts  
- analysis across multilingual datasets  
- nutrition informatics research

---

## Contribution to the DRG4FOOD Toolbox

NutriSight contributes:

- an open dataset of annotated nutrition tables  
- an open model with confidence scores  
- a reproducible training pipeline  
- annotation scripts and guidelines  
- API integration and a validation demo

These assets demonstrate responsible AI design and practice, aligned with DRG4FOOD principles on data fairness, trustworthiness, and human agency.

---

## License

NutriSight resources are published under open licenses:

- Dataset: open license (HuggingFace)  
- Model: open license (HuggingFace)  
- Software components: AGPL-3.0 (Open Food Facts repositories)

