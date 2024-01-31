# Segment Clothing
Segment clothing with 1 line of code. 

Takes in a PIL image and outputs a PIL image of segmented clothing. Built on top of 🤗 Tranformers using the [mattmdjaga/segformer_b2_clothes](https://huggingface.co/mattmdjaga/segformer_b2_clothes) image segmentation model.
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
![](https://cdn.discordapp.com/attachments/1120417968032063538/1202309847287345253/image-1.jpg?ex=65ccfd4d&is=65ba884d&hm=5411ab346668fea69ff2986cb5dab0b4fec042ff165a1d20724529125dbc535f&)

Segment Clothing
- **img** input image of type PIL
```python
result = segment_clothing(img=image)
result.save('segmented.png')
```
![](https://cdn.discordapp.com/attachments/1120417968032063538/1202309847543185499/segmented-1.png?ex=65ccfd4d&is=65ba884d&hm=be1484ac852ef1b2043e3327c1f52a798a332862d323140f1f7a27317e87d3af&)

You can also explicitly specify which clothes to segment
- **img** input image of type PIL
- **clothes** list of strings. by default ["Hat", "Upper-clothes", "Skirt", "Pants", "Dress", "Belt", "Left-shoe", "Right-shoe", "Scarf"]
```python
result = segment_clothing(img=image, clothes= ["Hat", "Upper-clothes", "Skirt", "Pants", "Dress", "Belt", "Left-shoe", "Right-shoe", "Scarf"])
result.save('segmented.png')
```
