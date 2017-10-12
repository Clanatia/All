# This Folder is etc files folder

##Tensorflow 한글 영상 강의 자료
    https://drive.google.com/file/d/0B_AgfGkstx4kX2JPVDNab2c3NFU/view?usp=sharing

##딥러닝 한글강의2
    http://hunkim.github.io/ml/

##Deep API  (파이선 , NodeJS, object c ..)
    https://deepai.org/ai-image-processing
     

##딥러닝 코드 및 자료링크모음
    https://github.com/mrgloom/awesome-semantic-segmentation

##책Download Site
   https://www.academia.edu/
   
##python opencv face dection code (windows working)
   ##https://github.com/informramiz/opencv-face-recognition-python
   
   
##Ubunto 16 install nvidia cuda install
  ##https://marcnu.github.io/2016-08-17/Tensorflow-v0.10-installed-from-scratch-Ubuntu-16.04-CUDA8.0RC-cuDNN5.1-1080GTX/
  
#torch error - gcc update

   ubunto14에서..
   sudo add-apt-repository ppa:ubuntu-toolchain-r/test
   sudo apt-get update
   sudo apt-get install gcc-5 g++-5
   
#err (OpenBLAS Probleam) : recipe for target '../libopenblas_haswellp-r0.3.0.dev.so' failed

  need downgrade gfortran : sudo apt-get install gfortran-4.9
   
##torch

  http://torch.ch/docs/getting-started.html
  git clone https://github.com/torch/distro.git ~/torch --recursive
  cd ~/torch; bash install-deps;
  ./install.sh
  

sudo update-alternatives --install /usr/bin/gcc gcc /usr/bin/gcc-5 60 --slave /usr/bin/g++ g++ /usr/bin/g++-5

## CUDAnn file link    
    #5.1ver (befor tensorflow 1.2) https://drive.google.com/file/d/0B_AgfGkstx4kdnpXcHBuakQxOG8/view?usp=sharing
    #6.0ver (teonsorflw 1.3) https://drive.google.com/open?id=0B_AgfGkstx4keXhRV2x5M0NBRHc

## Install Opencv (Anaconda python 3)
    
    conda install --channel https://conda.anaconda.org/menpo opencv3
    
    
    conda install -c menpo opencv3

## Homework4 video link
    
    https://www.youtube.com/watch?v=elj4pxEmFOY


## How to install caffe?

    1. Download https://github.com/BVLC/caffe/tree/windows
    
    2. :: Set python 2.7 with conda as the default python
    if !PYTHON_VERSION! EQU 2 (
        set CONDA_ROOT={conda install loot} => C:\Program Files\Anaconda3
    )
    :: Set python 3.5 with conda as the default python
    if !PYTHON_VERSION! EQU 3 (
        set CONDA_ROOT={conda install loot} => C:\Program Files\Anaconda3
    )

    3. if you want gpu mod, 
        :: Add -DCUDNN_ROOT={CUDA loot} => C:\Program Files\NVIDIA GPU Computing Toolkit\CUDA\v8.0 ^
        
    4. open cmd, and typing
    \caffe> scripts\build_win.cmd
    conda config --add channels conda-forge
    conda config --add channels willyd
    conda install --yes cmake ninja numpy scipy protobuf==3.1.0 six scikit-image pyyaml pydotplus graphviz
    
    5. and caffe folder to your site_packages folder.
