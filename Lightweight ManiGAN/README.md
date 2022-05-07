# Lightweight Generative Adversarial Networks for Text-Guided Image Manipulation
Pytorch implementation for Lightweight GAN

**[Lightweight Generative Adversarial Networks for Text-Guided Image Manipulation](https://proceedings.neurips.cc/paper/2020/file/fae0b27c451c728867a567e8c1bb4e53-Paper.pdf).**  
[Bowen Li](https://mrlibw.github.io/), [Xiaojuan Qi](https://xjqi.github.io/), [Philip H. S. Torr](http://www.robots.ox.ac.uk/~phst/), [Thomas Lukasiewicz](http://www.cs.ox.ac.uk/people/thomas.lukasiewicz/).<br> University of Oxford, University of Hong Kong <br> NeurIPS 2020 <br>

### Data

1. Download the preprocessed metadata for [bird](https://drive.google.com/file/d/1D87x3JAt0w9ymlKElh7ArpAviKUqkNbN/view?usp=sharing) and [coco](https://drive.google.com/file/d/1hNEsFDj7S0aG1tXFvJy1DXtQWSl2Z9gZ/view?usp=sharing), and save both into `data/`
2. Download [bird](http://www.vision.caltech.edu/visipedia/CUB-200-2011.html) dataset and extract the images to `data/birds/`
3. Download [coco](http://cocodataset.org/#download) dataset and extract the images to `data/coco/`

### Training

- Train the model for bird dataset:
```
python main.py --cfg cfg/train_bird.yml --gpu 2
```
- Train the model for coco dataset: 
```
python main.py --cfg cfg/train_coco.yml --gpu 3
```

`*.yml` files include configuration for training and testing. To reduce the number of parameters used in the model, please edit DF_DIM and/or GF_DIM values in the corresponding `*.yml` files.

#### Pretrained DAMSM Model for text encoding
- [DAMSM for bird](https://drive.google.com/file/d/1n-qKR7K4V-4oVC1GaGeIHLTQfIzPsTsE/view?usp=sharing). Download and save it to `DAMSMencoders/`
- [DAMSM for coco](https://drive.google.com/file/d/1GnXhzMKtFM-RK_ATsfU1tomta1Ko72vr/view?usp=sharing). Download and save it to `DAMSMencoders/`


### Testing
- Test our model on bird dataset:
```
python main.py --cfg cfg/eval_bird.yml --gpu 4
```
- Test our model on coco dataset: 
```
python main.py --cfg cfg/eval_coco.yml --gpu 5
```
### Evaluation

- To generate images for all captions in the testing dataset, change B_VALIDATION to `True` in the `eval_*.yml`. 




