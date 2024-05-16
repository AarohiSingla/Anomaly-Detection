#### Paper: https://arxiv.org/pdf/1801.04264v3
![p9](https://github.com/AarohiSingla/Anomaly-Detection/assets/60029146/546dfe01-1cab-48af-abff-7e94d8beed7e)


![1a](https://github.com/AarohiSingla/Anomaly-Detection/assets/60029146/f35c00be-49c4-4065-a880-54f58224f88f)

![1b](https://github.com/AarohiSingla/Anomaly-Detection/assets/60029146/869a9b75-f2e9-4cf2-91ef-646c8b4ff29a)

#### Dataset: 
![data](https://github.com/AarohiSingla/Anomaly-Detection/assets/60029146/c85e5aa4-e88f-472f-bd21-fedb042586b2)



#### 1- Clone this github repo: 

git clone https://github.com/ekosman/AnomalyDetectionCVPR2018-Pytorch.git

#### 2- Setup the environment to run this code:

cd to AnomalyDetectionCVPR2018-Pytorch

You will see environment.yaml file. Open it. You need to install all these modules. I am not working on anaconda, so I can’t use environment.yaml as it is. You can convert this environment.yaml into requirements.txt or just all these modules 1 by 1 through command line using pip. Eg:

pip install torch==2.2.1 torchvision==0.17.1 torchaudio==2.2.1 --index-url https://download.pytorch.org/whl/cu118      

pip install numpy

pip install opencv-python

pip install matplotlib

pip install pandas 

pip install av

Note:  you have to check the cuda version installed in your machine and then pick the right command to install pytorch. IN my case I have installed the pytorch with cuda 11.8

You need to install LAV filters also. 

Visit this page https://github.com/Nevcairiel/LAVFilters/releases  and download LAVFilters-0.79.2-Installer.exe   which is under assets and then install it.


#### DATASET:

The dataset can be also downloaded from the following link: https://visionlab.uncc.edu/download/summary/60-data/477-ucf-anomaly-detection-dataset

You can also download dataset in parts through following link

https://www.dropbox.com/sh/75v5ehq4cdg5g5g/AABvnJSwZI7zXb8_myBA0CLHa?dl=0


#### Feature Extraction model:
Download the pretrained C3D weights (Sports1M) from here: http://imagelab.ing.unimore.it/files/c3d_pytorch/c3d.pickle

#### Paste it in pretrained folder and then run this command:

python video_demo.py --feature_extractor "pretrained/c3d.pickle" --feature_method "c3d" --ad_model "D:\\anomaly_detection\\AnomalyDetectionCVPR2018-Pytorch\\exps\\c3d\models\\epoch_80000.pt"

