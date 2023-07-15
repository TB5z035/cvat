FROM ubuntu:22.04

ENV NVIDIA_VISIBLE_DEVICES=all
ENV DEBIAN_FRONTEND=noninterative
WORKDIR /opt/nuclio/sam
RUN apt-get update && apt-get -y install curl git python3 python3-pip ffmpeg libsm6 libxext6
RUN pip3 install torch torchvision torchaudio opencv-python pycocotools matplotlib onnxruntime onnx -i https://pypi.tuna.tsinghua.edu.cn/simple
RUN pip3 install git+https://github.com/facebookresearch/segment-anything.git
RUN curl -O https://dl.fbaipublicfiles.com/segment_anything/sam_vit_h_4b8939.pth
RUN ln -s /usr/bin/pip3 /usr/local/bin/pip && ln -s /usr/bin/python3 /usr/bin/python
