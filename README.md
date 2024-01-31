# Segment Clothing
Segment clothing with 1 line of code. Takes in a PIL image and outputs a PIL of segmented clothing. Built on top of 🤗 Tranformers using the [mattmdjaga/segformer_b2_clothes](https://huggingface.co/mattmdjaga/segformer_b2_clothes) image segmentation model.
## Installation
```bash
pip install -r requirements.txt
```

## Usage

Import module
```python
from Embed import create_dataset_embeddings
```

Generates image embeddings and upload to 🤗
- **input_dataset** the source dataset
- **out_dataset** the name of dataset that will be created and uploaded to
- **token** HuggingFace write access token can be created [here](https://huggingface.co/settings/tokens)
```python
create_dataset_embeddings(input_dataset='tonyassi/fashion-decade-images-1',
                          output_dataset='tonyassi/fashion-decade-images-1-embeddings',
                          token='YOUR_TOKEN')

```
