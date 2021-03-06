# Deep Learning Project: Unsupervised Anomaly Detection on X-Ray Images
## Project Summary
In our project we plan on using Generative Adversarial Network (GAN) to detect anomaly in X-ray images. A GAN is a class of AI systems, where Two neural organizations challenge with one another in a game (as a lose-lose situation, where one specialist's benefit is another specialist's misfortune). For our project we will be using two GANs- AlphaGAN and AnoGAN in Mura-1.1 dataset from Stanford.

1. **AlphaGAN**: The generator of this network is a convolutional encoder-decoder network that is trained both with help of the ground-truth alphas as well as the adversarial loss from the discriminator, and the discriminator is a patchGAN Discriminator.
2. **AnoGAN**: The firstly proposed method using GAN for anomaly detection. The generator of GAN is trained to produce patches and fit the data distribution. Based on the second loss, the generator takes not only the information to fool the discriminator but the rich information of the feature representation

## Inference Pipeline Architecture to detect Anomaly
![Inference-Pipeline](https://github.com/plodha/CMPE-297-DeepLearning/blob/main/Deliverables/Inference_Pipeline.png)

## Summary
In this repository you will find the files required to train multiple different models in-order to find anomalies in X-ray images.

In this repository you will find
  - Jupyter Notebooks / Google Colab Notebooks: Contains colab for AlphaGAN Training; f-AnoGAN Training; Inference Code for Anomaly Detection. 
      - All metrics computation
      - Tensorboard
      
  - Deliverables<br/>
         1. Proposal [pdf](https://github.com/plodha/CMPE-297-DeepLearning/blob/main/Deliverables/Project%20Proposal%20-%20TheMeanSquares.pdf)<br/>
         2. Project Report [pdf](https://github.com/plodha/CMPE-297-DeepLearning/blob/main/Deliverables/X-Ray%20Anomaly%20Detection%20Project%20Paper.pdf)<br/>
         3. Presentation [pdf](https://github.com/plodha/CMPE-297-DeepLearning/blob/main/Deliverables/CMPE%20297%20Deep%20Learning%20Project.pdf)<br/>
  - WebApp (frontend, backend)
  - TFX
    - TFX preprocessing to create tfrecord file
    - TFX_mura.ipynb -TFX for mura dataset
    
## Python packages used
* PyTorch 1.7
* OpenCV
* Scikit-Image
* Pillow

## Differentiator
* Trained AlphaGAN in GCP-TPU 
* Developed and trained f-AnoGAN for mura dataset
* Compared the metrics of AlphaGan and f-AnoGAN
* TFX end-to-end pipeline for mura dataset

![metrics](https://github.com/plodha/CMPE-297-DeepLearning/blob/main/Deliverables/metrics.png)
