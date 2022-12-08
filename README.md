# Handwritten-Character-Generator
## Google Colab
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


## Locally 
```
$ git clone https://github.com/marsof02/Handwritten-Character-Generator.git
$ cd Handwritten-Character-Generator
```
