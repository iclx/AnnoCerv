# AnnoCerv
A segmented and annotated colposcopy image set

## Description
This repository contains a dataset of 527 colposcopy images sourced from 100 medical records. Expert specialists segmented and annotated each image to differentiate between healthy and pathological cervical tissues. The dataset is complemented with Swede scores and some accompanying code exemplifying processing an modelling of the data.


## Dataset Structure and Format

### Directory Structure
Each individual medical case is encapsulated within its own unique folder, named as "Case ID".

### Image Files
- Within each case folder, you'll find one or more cervix images saved in JPG format.
- The images within a single case can be of various types, namely:
  - Acetic acid images
  - Iodine images
  - Green-filtered images

### Filename Convention
Images are named with a standardized convention for clarity. It consists of:
1. Case identifier
2. Image type
3. An index enclosed within parentheses to distinguish multiple images of the same type.

### Annotation Files
- Each acetic acid image (denoted by 'Aceto' in the filename) has a corresponding PNG annotation file.
- This file carries the same primary filename but with a .png extension.
- Example: An image named `C1Aceto (1).jpg` will have its annotations in `C1Aceto (1).png`.

### Annotation Encoding
The PNG annotation files use specific color encoding to represent various observed features:
- **Blue**: Squamous-cylindrical junction
- **Purple**: Aceto-white areas
- **Red**: Atypical vessels and punctations
- **Brown**: Mosaics
- **Yellow**: Naboth cysts
- **Black**: Cuffed gland openings

The background of these PNG files is transparent. If no notable features were detected by the medical professional, the PNG remains entirely transparent without any colored pixels.

### Swede Scores
Swede scores for each case are cataloged in the CSV file named `dataset/swede_scores.csv`.

## Notebooks
The release includes code that demonstrates data handling and processing and exemplifies a simple feature extraction and classification technique.

Dataset processing notebook
<a target="_blank" href="https://colab.research.google.com/github/iclx/AnnoCerv/blob/main/data_summary.ipynb">
  <img src="https://colab.research.google.com/assets/colab-badge.svg" alt="Open In Colab"/>
</a>

Data modeling and evaluation notebook
<a target="_blank" href="https://colab.research.google.com/github/iclx/AnnoCerv/blob/main/data_modelling.ipynb">
  <img src="https://colab.research.google.com/assets/colab-badge.svg" alt="Open In Colab"/>
</a>

## Citing
If you use this dataset in your research or project, please ensure you attribute it accordingly, respecting the Creative Commons Attribution 4.0 International License.


Shield: [![CC BY 4.0][cc-by-shield]][cc-by]

This work is licensed under a
[Creative Commons Attribution 4.0 International License][cc-by].

[![CC BY 4.0][cc-by-image]][cc-by]

[cc-by]: http://creativecommons.org/licenses/by/4.0/
[cc-by-image]: https://i.creativecommons.org/l/by/4.0/88x31.png
[cc-by-shield]: https://img.shields.io/badge/License-CC%20BY%204.0-lightgrey.svg



