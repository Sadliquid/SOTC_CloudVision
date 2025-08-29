# Sigils of The Codex

This project demonstrates how to use Google's Cloud Vision API to identify recyclable items in images using Python and Jupyter Notebook. The notebook guides you through running inferences, retrieving annotation labels, mapping them to recyclable categories, and building a scoring system to determine the best prediction for each image.

## Features
- **Object Localization**: Detects objects in images using Google Cloud Vision API.
- **Category Mapping**: Maps detected objects to recyclable categories defined in `config.json`.
- **Scoring System**: Resolves ties and improves accuracy using label detection.
- **Config Automation**: Automatically expands the label database for better recognition.
- **Image Preprocessing**: Optimizes images for inference.

## Getting Started

### Prerequisites
- Python 3.7+
- Google Cloud account and service account key (`serviceAccountKey.json`)
- Jupyter Notebook

### Installation
1. Clone this repository and navigate to the project folder.
2. Install required packages:
   ```bash
   pip install google-cloud-vision pillow
   ```
3. Place your Google Cloud service account key as `serviceAccountKey.json` in the project root.

### Usage
1. Open `SOTC_MasterCopy.ipynb` in Jupyter Notebook.
2. Follow the notebook cells to:
   - Authenticate with Google Cloud Vision API
   - Load and preprocess images
   - Run object localization and label detection
   - Map results to recyclable categories
   - Expand the label database for improved accuracy

### Folder Structure
```
images/                # Sample images for testing
config.json            # Maps categories to annotation labels
serviceAccountKey.json # Google Cloud credentials
SOTC_MasterCopy.ipynb  # Main notebook
```

## How It Works
- The notebook walks you through uploading images, running inferences, and updating the label database.
- You can add new recyclable categories and expand their label sets by running images through the helper functions.
- The pipeline improves reliability as more images and labels are added.