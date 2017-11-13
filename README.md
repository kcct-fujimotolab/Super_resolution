# Super_resolution
Easy model running super resolution based on SRCNN using Keras.

## Description

These programs can load images from the specified directory, resize these images and train the model.
Also you can load trained models and do super resolution.

## Requirements

- Python 3.0 or more
- Keras 2.0 or more (Tensorflow backend)
- Pillow
- numpy
- tqdm
- h5py

## Get started

1. Clone this repository:
```sh
git clone https://github.com/kcct-fujimotolab/Super_resolution.git
cd Super_resolution/
```

2. Make a directory for data sets:
```sh
mkdir images
```

3. Collect images (more than thousands better):
```sh
ls images/
data0000.jpg   data0001.jpg   ...   data9999.jpg
```

4. Start training with specifying image size, number of epochs, data set directory, etc.:
```sh
python train.py --input images/ --size 64 64 --epoch 1000
```

5. Do super resolution with running `sr2x`.py:
```sh
python sr2x.py
Using TensorFlow backend.
Enter the file name (*.jpg)
>> test/data.jpg
```

## Options

`--help` `-h`: show information

### train.py

`--input` `-i`: data sets path (default `-i images/`)  
`--size` `-z`: image size, **2 values required** (default `-z 64 64`)  
`--epoch` `-e`: number of epochs (default `-e 500`)  
`--batch` `-b`: batch size (default `-b 64`)  

## Results

We extracted 4096 images from the face data provided by [Labeled Faces in the Wild](http://vis-www.cs.umass.edu/lfw/), and trained.

## Author

[Fujimoto Lab](http://www.kobe-kosen.ac.jp/~fujimoto/) in [Kobe City College of Technology](http://www.kobe-kosen.ac.jp)  
Undergraduate Student of Electronics Department  
[@yoidea](https://twitter.com/yoidea)