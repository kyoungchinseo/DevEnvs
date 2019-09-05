# docker for au heatmaps
# anaconda-based installation

FROM nvidia/cuda:9.0-cudnn7-devel-ubuntu16.04

RUN apt-get update
RUN apt-get install -y --no-install-recommends \
    ca-certificates curl git vim less \
    build-essential cmake pkg-config wget


#RUN wget https://repo.anaconda.com/archive/Anaconda3-2019.07-Linux-x86_64.sh && \
#    sh -y Anaconda3-2019.07-Linux-x86_64.sh

#RUN pip install dlib && \
#    pip install cv2

# install dlib
# pip install dlib

# install opencv 
# pip install cv2 --> error
# pip install opency-python --> import cv2 error

# conda install opencv --> it works!

# install additional libraries
# pip install scipy
# pip install matplotlib

# install pytorch
# conda install pytorch torchvision cudatoolkit=9.2 -c pytorch

# dlib detecter
# wget http://dlib.net/files/shape_predictor_68_face_landmarks.dat.bz2
# bzip2 -d shape_predictor_68_face_landmarks.dat.bz2 


# execution
nvidia-docker run --device=/dev/video0:/dev/video0 -v /tmp/.X11-unix:/tmp/.X11-unix -e DISPLAY=$DISPLAY -e QT_X11_NO_MITSHM=1 -p 5000:5000 -p 8888:8888 -it -v $(pwd):/workspace autheatmaps:1.0 /bin/bash
