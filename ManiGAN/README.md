# ManiGAN 
Pytorch implementation for ManiGAN

**[ManiGAN: Text-Guided Image Manipulation](https://arxiv.org/abs/1912.06203).**  
[Bowen Li](https://mrlibw.github.io/), [Xiaojuan Qi](https://xjqi.github.io/), [Thomas Lukasiewicz](http://www.cs.ox.ac.uk/people/thomas.lukasiewicz/), [Philip H. S. Torr](http://www.robots.ox.ac.uk/~phst/).<br> University of Oxford <br> CVPR 2020 <br>

### Training
- Train main module for bird dataset:
```
python main.py --cfg cfg/train_bird.yml --gpu 2
```
- Train main module for coco dataset: 
```
python main.py --cfg cfg/train_coco.yml --gpu 3
```

`*.yml` files include configuration for training and testing.

#### Pretrained DAMSM Model
- [DAMSM for bird](https://drive.google.com/file/d/1ZqlwNWIaV4KblBwZ6eqlX9-_SzLlP17h/view?usp=sharing). Download and save it to `DAMSMencoders/`
- [DAMSM for coco](https://drive.google.com/file/d/1ewMMhCDf-QfAD_vs07ZFgg2L9quIKRUN/view?usp=sharing). Download and save it to `DAMSMencoders/`

### Testing
- Test ManiGAN model for bird dataset:
```
python main.py --cfg cfg/eval_bird.yml --gpu 4
```
- Test ManiGAN model for coco dataset: 
```
python main.py --cfg cfg/eval_coco.yml --gpu 5
```
### Evaluation

- To generate images for all captions in the testing dataset, change B_VALIDATION to `True` in the eval_*.yml.
