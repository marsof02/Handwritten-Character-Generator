# Handwritten-Character-Generator
## Quick Start
### Google Colab
[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/marsof02/Handwritten-Character-Generator/blob/main/CharacterGAN.ipynb)

Needs Google Drive mount for loading data. Download CData file and upload it onto Google Drive.
Copy just below top code cell.
```
from google.colab import drive
drive.mount('/content/drive')
```
And then copy this below the last one.
```
dset = pd.read_csv('/content/drive/MyDrive/CData/emnist-balanced-train.csv', header=None)
dset.head()
```
Finally, comment out the following block.
```
dset = pd.read_csv('CData/emnist-balanced-train.csv', header=None)
dset.head()

```


### Locally 
```
$ git clone https://github.com/marsof02/Handwritten-Character-Generator.git
$ cd Handwritten-Character-Generator
```
## Generative Adversarial Network (GAN)
This model is composed by two neural networks: a generator that takes a random distribution as input and outputs some data (typically an image), and a discriminator that takes a fake image from the generator and a real one from the training set as input, and must guess whether the input image is fake or real.
The goal of the generator is to trick the discriminator and the goal of the discriminator is to tell fake images from real ones correctly, despite the increased accuracy of the generator's results.

<img width="576" alt="Screen Shot 2022-12-08 at 7 24 05 AM" src="https://user-images.githubusercontent.com/66377681/206445637-5a22b0aa-adde-43b1-b3cc-29e95294d88c.png">

This model was trained on the EMNIST (Extended MNIST) dataset from https://www.kaggle.com/datasets/crawford/emnist

Consulted the following sources for implementation details:

- Hands-On Machine Learning with Scikit-Learn, Keras, and TensorFlow: Concepts, Tools, and Techniques to Build
Intelligent Systems by Aurélien Géron (https://a.co/aotQFto)
- Deep Convolutional Generative Adversarial Network Tutorial by TensorFlow (https://www.tensorflow.org/tutorials/generative/dcgan)
- Generative Adversarial Networks (GAN) in Tensorflow Tutorial by Sundog Education (https://www.youtube.com/watch?v=LZov6445YAY)

Results were compared to the ones of the Variational Autoencoder (VAE) in the book referenced on the previous list using the same dataset.

<img width="739" alt="Screen Shot 2022-12-08 at 7 38 36 AM" src="https://user-images.githubusercontent.com/66377681/206448262-c9330b99-307b-46df-a85f-a02173435caa.png">

<img width="742" alt="Screen Shot 2022-12-08 at 7 51 53 AM" src="https://user-images.githubusercontent.com/66377681/206451223-42a484f8-03ea-40da-9648-111f9c16b0ee.png">

