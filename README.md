# Segment Clothing
Segment clothing with 1 line of code. 

Takes in a PIL image and outputs a PIL image of segmented clothing. Built on top of 🤗 Tranformers using the [mattmdjaga/segformer_b2_clothes](https://huggingface.co/mattmdjaga/segformer_b2_clothes) image segmentation model.

Try out the Web Demo: [![Hugging Face Spaces](https://img.shields.io/badge/%F0%9F%A4%97%20Hugging%20Face-Spaces-blue)](https://huggingface.co/spaces/tonyassi/clothing-segmentation)

## Installation
```bash
pip install -r requirements.txt
```
Python 3.9
Transformers 4.37.2
Torch 2.2.0
Pillow 10.2.0
NumPy 1.26.3

## Usage

Import module
```python
from SegCloth import segment_clothing
```

Import PIL and open image
```python
from PIL import Image
image = Image.open('image.jpg')
```

![](https://cdn.discordapp.com/attachments/1120417968032063538/1202309847287345253/image-1.jpg?ex=65e8accd&is=65d637cd&hm=f42cd1095001982434a3b05907409ef8d3a380a860a7c7e079ab82f558842697&)
---

Segment Clothing
- **img** input image of type PIL
```python
result = segment_clothing(img=image)
result.save('segmented.png')
```
![](https://cdn.discordapp.com/attachments/1120417968032063538/1202309847543185499/segmented-1.png?ex=65e8accd&is=65d637cd&hm=eed593adeca5b6d37ae2576499d5e142e4117f9c3f7bbd076d5cb575655e0efc&)

You can also explicitly specify which clothes to segment
- **img** input image of type PIL
- **clothes** list of strings. by default ["Hat", "Upper-clothes", "Skirt", "Pants", "Dress", "Belt", "Left-shoe", "Right-shoe", "Scarf"]
```python
result = segment_clothing(img=image, clothes= ["Hat", "Upper-clothes", "Skirt", "Pants", "Dress", "Belt", "Left-shoe", "Right-shoe", "Scarf"])
result.save('segmented.png')
```
