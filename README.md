# Segment Clothing
Segment clothing with 1 line of code. 

Takes in a PIL image and outputs a PIL image of segmented clothing. 

Built on top of 🤗 Tranformers using the [mattmdjaga/segformer_b2_clothes](https://huggingface.co/mattmdjaga/segformer_b2_clothes) image segmentation model.
## Installation
```bash
pip install -r requirements.txt
```

## Usage

Import module
```python
from SegCloth import segment_clothing
```

Import PIL
```python
from PIL import Image
```

Open image
```python
image = Image.open('image.jpg')
```

Segment Clothing
- **img** input image of type PIL
```python
result = segment_clothing(img=image)
result.save('segmented.png')
```

You can also explicitly specify which clothes to segment
- **img** input image of type PIL
- **clothes** list of strings. by default ["Hat", "Upper-clothes", "Skirt", "Pants", "Dress", "Belt", "Left-shoe", "Right-shoe", "Scarf"]
```python
result = segment_clothing(img=image, clothes= ["Hat", "Upper-clothes", "Skirt", "Pants", "Dress", "Belt", "Left-shoe", "Right-shoe", "Scarf"])
result.save('segmented.png')
```
