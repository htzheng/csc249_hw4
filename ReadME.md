# Image Captioning with Pytorch

## Usage

Main dependencies: Python 2.7 and Pytorch-0.4.0 (https://pytorch.org/get-started/previous-versions/)

To setup enviroment, install Anaconda and type the following command
```
######### create a new environment
conda create -n myenv python=2.7
conda activate myenv
######### install the following packages
conda install pytorch=0.4.1 cuda92 -c pytorch
conda install -c anaconda cython
conda install -c conda-forge matplotlib
```


#### 1. Download and compile some toolboxes from coco. Please make sure that you are using python 2.7
```bash
$ git clone https://github.com/pdollar/coco.git
$ cd coco/PythonAPI/
$ make
$ python setup.py build
$ python setup.py install
$ cd ../../
$ git clone https://github.com/YapengTian/csc249_hw4.git
$ cd csc249_hw4
```
#### 2. Download data and evaluation toolboxes
```bash
$ download support.zip from https://drive.google.com/file/d/1ZqJs2AGtMTfGTgH1oHTP_ZEFXRNX3uLj/view?usp=sharing (1.7 GB)
$ unzip the file and copy folders: data, pycocotoolscap, pycocoevalcap into csc249_hw4
$ download stanford NLP models (require java 1.8.0): run ./get_stanford_models.sh 
$ pip install -r requirements.txt
```

#### 3. Train
```bash
$ python train.py
```

#### 4. Prediction for one input image
```bash
$ python predict.py --image img/bird.png
```

#### 5. Evaluation on 100 image from MSCOCO and save the results
```bash
$ python eval.py
```
