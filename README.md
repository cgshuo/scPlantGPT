# scPlantGPT

# Single-Cell Plant Generative pre-trained transformer model

This project aims to pretrain a large model using 1 million plant single-cell data and further pretrain a cell annotation model and a batch integration model based on this pretrained model. Ultimately, we can use these pretrained models for cell annotation, providing an efficient method for handling large-scale plant single-cell data.

## Project Overview

1. **Data Preparation**: Use 1 million plant single-cell data for training.
2. **Pretraining the Generative Model**: Pretrain a generative model.
3. **Pretraining the Cell Annotation Model**: Use the pretrained generative model's weights to further pretrain the cell annotation model on the 1 million plant single-cell data.
4. **Pretraining the Batch Integration Model**: Use the pretrained generative model's weights to further pretrain the batch integration model on the 1 million plant single-cell data.
5. **Cell Annotation Application**: Use the pretrained cell annotation model for cell annotation. You can choose to apply it directly or fine-tune it before application.

## Table of Contents

- [Installation](#installation)
- [Usage](#usage)
- [File Structure](#file-structure)
- [Contribution](#contribution)
- [License](#license)
- [Contact](#contact)

## Installation

### Environment Dependencies

- Python 3.8+
- Refer to `requirements.txt` for the list of dependencies.

### Steps

1. Clone this repository
    ```bash
    git clone https://github.com/your_username/cell-pretrain-annotation.git
    cd cell-pretrain-annotation
    ```

2. Create and activate a virtual environment (optional)
    ```bash
    python -m venv venv
    source venv/bin/activate  # For Windows, use `venv\Scripts\activate`
    ```

3. Install dependencies
    ```bash
    pip install -r requirements.txt
    ```

## Usage

### Data Preparation

Ensure your data format meets the project requirements. You need to provide 1 million plant single-cell data. The data should be stored in the `data/` directory.

### Pretraining the Generative Model

Run the following command to pretrain the generative model:

```bash
python scripts/train_generator.py --data_dir data/train_data/ --output_dir models/generator/
