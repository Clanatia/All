# This Folder is etc files folder

##Tensorflow 한글 영상 강의 자료
    https://drive.google.com/file/d/0B_AgfGkstx4kX2JPVDNab2c3NFU/view?usp=sharing

## CUDAnn file link
    https://drive.google.com/file/d/0B_AgfGkstx4kdnpXcHBuakQxOG8/view?usp=sharing

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
