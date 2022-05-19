# Text-to-Image-GAN

In this project, we evaluate a few popular GAN-based text-to-image generation models for the CUB and COCO datasets, and provide a detailed analysis of the generative models using evaluation metrics such as the Inception Score (IS) and the Fr´echet Inception Distance (FID) to compare the output images
across different architectures. Our experiments reveal that
the lightweight architecture for text-guided image manipulation
achieves the best FID of 10.2 for the CUB dataset
also while being more efficient than other GAN-based textto-
image models.


### Results
*Experimental Results*

<img src="images/results.png" width="400">

*Synthesized images*

<img src="images/images.png" width="400">

##### Our final weight files for trained models 
- [DF-GAN](https://drive.google.com/file/d/17iSeUJZVGyLwqkwKOCLtKOH76fNjRf5P/view?usp=sharing)
- [ManiGAN](https://drive.google.com/file/d/1qMNtmqAqFt2aNzWOY2CyK_MRtcjNCDvS/view?usp=sharing)
- [Lightweight ManiGAN](https://drive.google.com/file/d/1QhPx2GZmIUU17Nc6NY8e9jEATcM9ow1r/view?usp=sharing)
Download and save it to `models/` in order to get results

### References
[1] Deep Fusion GAN - [DF-GAN](https://arxiv.org/abs/2008.05865)

[2] Text-Guided Image Manipulation - [ManiGAN](https://arxiv.org/abs/1912.06203)

[3] Lightweight Architecture for Text-Guided Image Manipulation - [Lightweight ManiGAN](https://arxiv.org/abs/2010.12136)

[4] PyTorch Implementation for Inception Score (IS) - [IS](https://github.com/sbarratt/inception-score-pytorch) 

[5] PyTorch Implementation for Fréchet Inception Distance (FID) - [FID](https://github.com/mseitzer/pytorch-fid) 
