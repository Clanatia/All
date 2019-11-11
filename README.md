# This Folder is etc files folder

## Tensorflow whl(install file) link
    https://mirrors.tuna.tsinghua.edu.cn/tensorflow/windows/gpu

## Tensorflow 한글 영상 강의 자료
    https://drive.google.com/file/d/0B_AgfGkstx4kX2JPVDNab2c3NFU/view?usp=sharing 
    https://hunkim.github.io/ml

## 손풀이 강좌
	https://www.youtube.com/watch?v=5T5a9zIp-ZM&list=PL1H8jIvbSo1q6PIzsWQeCLinUj_oPkLjc
    

## 딥러닝 강의2
    https://cs.nyu.edu/~yann/talks/lecun-ranzato-icml2013.pdf 
    https://docs.google.com/presentation/d/1HxGdeq8MPktHaPb-rlmYYQ723iWzq9ur6Gjo71YiG0Y/edit#slide=id.g12af6bd97a_0_289 

## Deep API  (파이선 , NodeJS, object c ..)
    https://deepai.org/ai-image-processing
     
## Keras binarize net 
    https://github.com/DingKe/BinaryNet

## Tensorflow binarize net
    https://github.com/jonathanmarek1/binarynet-tensorflow
    https://github.com/itayhubara/BinaryNet.tf


## 딥러닝 코드 및 자료링크모음
    https://github.com/mrgloom/awesome-semantic-segmentation

## 책Download Site
    https://www.academia.edu/
   
## python opencv face dection code (windows working)
    https://github.com/informramiz/opencv-face-recognition-python
   
## gan Url
    https://github.com/hwalsuklee/tensorflow-generative-model-collections
   
## inception net
    https://github.com/tensorflow/models/tree/master/research/inception#getting-started
    
## Ubunto 16 install nvidia cuda install
    https://marcnu.github.io/2016-08-17/Tensorflow-v0.10-installed-from-scratch-Ubuntu-16.04-CUDA8.0RC-cuDNN5.1-1080GTX/
  
## torch error - gcc update
    ubunto14에서..
    sudo add-apt-repository ppa:ubuntu-toolchain-r/test
    sudo apt-get update
    sudo apt-get install gcc-5 g++-5
   
# err (OpenBLAS Probleam) : recipe for target '../libopenblas_haswellp-r0.3.0.dev.so' failed
    need downgrade gfortran : sudo apt-get install gfortran-4.9
   
# error  cuda 9.0 "error: more than one operator "==" matches these operands" (https://github.com/torch/cutorch/issues/797)
    insert export TORCH_NVCC_FLAGS="-D__CUDA_NO_HALF_OPERATORS__"
   
##torch
 http://torch.ch/docs/getting-started.html
 git clone https://github.com/torch/distro.git ~/torch --recursive
 cd ~/torch; bash install-deps;
 ./install.sh
 (cd bin)
 luarocks install image
 luarocks list
  

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
    
    
## caffe 기초 설치법
    https://gist.github.com/arundasan91/b432cb011d1c45b65222d0fac5f9232c

    leveldb -> sudo apt-get install libleveldb-dev libsnappy-dev libhdf5-serial-dev

    sudo apt-get install libprotobuf-dev libleveldb-dev libsnappy-dev libhdf5-serial-dev protobuf-compiler
    sudo apt-get install --no-install-recommends libboost-all-dev

## makefile에서 python3.5일 경우
	PYTHON_LIBRARIES ?= boost_python-py35 python3.5m
	PYTHON_INCLUDE := /usr/include/python3.5m \
	    	/usr/lib/python3.5/dist-packages/numpy/core/include

    	/src/caffe/cpm_data_transformer.cpp파일에서	
	opencv2/contrib/contrib.hpp -> opencv2/face.hpp


## /usr/bin/ld: cannot find -lopencv_contrib
    makefile에 opencv_contrib를 없에준다.(opencv3버전에서는 contrib가 없더라)
    

## src/caffe/layers/hdf5_data_layer.cpp:13:18: fatal error: hdf5.h: 그런 파일이나 디렉터리가 없습니다
	makefile에 추가
	INCLUDE_DIRS += $(PYTHON_INCLUDE) /usr/local/include /usr/include/hdf5/serial/
	LIBRARY_DIRS += $(PYTHON_LIB) /usr/local/lib /usr/lib /usr/lib/x86_64-linux-gnu/hdf5/serial/


## undefined reference to H5LTget_dataset_ndims 문제   http://ms-cheminfo.com/?q=node/106
	caffe/cmake/Dependencies.cmake, at line 28
	list(APPEND Caffe_LINKER_LIBS ${HDF5_LIBRARIES})
	to
	list(APPEND Caffe_LINKER_LIBS ${HDF5_LIBRARIES} ${HDF5_HL_LIBRARIES})


## db_leveldb.cpp:16] Check failed: status.ok() Failed to open leveldb 
	Fix this by change: src/caffe/test/test_layer_factory.cpp:line 33
	if (iter->first == "Data") {
	to
	if(iter->first == "Data" || iter->first == "BoxData")


## 경로문제
	sudo gedit ~/.bashrc
	export PYTHONPATH=/media/vit/DATA/Tensor/caffe_train/build/python:$PYTHONPATH


## Check failed: error == cudaSuccess (10 vs. 0)  invalid device ordinal
    gpu버전세팅빌드가 재대로 안되서 그렇다.
    caffe를 make할때 CUDA_ARCH 부분을 재대로 설정해주어야함.
    CUDA_ARCH := -gencode arch=compute_20,code=sm_20 \
    -gencode arch=compute_20,code=sm_21 \
    -gencode arch=compute_30,code=sm_30 \
    -gencode arch=compute_35,code=sm_35 \
    -gencode arch=compute_50,code=sm_50 \
    -gencode arch=compute_50,code=compute_50
    -gencode=arch=compute_52,code=sm_52 \
    -gencode=arch=compute_52,code=compute_52 \
    -gencode=arch=compute_60,code=sm_60 \
    -gencode=arch=compute_61,code=sm_61 \



