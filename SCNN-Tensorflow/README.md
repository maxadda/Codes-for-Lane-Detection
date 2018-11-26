Tensorflow version of SCNN in CULane.

## Installation
    conda create -n tensorflow_gpu pip python=3.5
    source activate tensorflow_gpu
    pip install --upgrade tensorflow-gpu==1.3.0
    pip3 install -r lane-detection-model/requirements.txt 

## Download VGG-16
Download the vgg.npy [here](https://github.com/machrisaa/tensorflow-vgg) and put it in lane-detection-model/data.

## Pre-trained model
Download the pre-trained model here. (Coming soon!)

## Test
    cd lane-detection-model
    CUDA_VISIBLE_DEVICES="0" python tools/test_lanenet.py --weights_path path/to/model_weights_file --image_path path/to/image_name_list

Note that path/to/image_name_list should be like [test_img.txt](./lane-detection-model/demo_file/test_img.txt).

## Train
    cd lane-detection-model
    CUDA_VISIBLE_DEVICES="0" python tools/train_lanenet.py --net vgg --dataset_dir path/to/CULane-dataset/

Note that path/to/CULane-dataset/ should contain files like [train_gt.txt](./lane-detection-model/demo_file/train_gt.txt) and [val_gt.txt](./lane-detection-model/demo_file/train_gt.txt).

## Acknowledgement
This repo is built upon [SCNN](https://github.com/XingangPan/SCNN) and [LaneNet](https://github.com/MaybeShewill-CV/lanenet-lane-detection)

## Contact
If you have any problems in reproducing the results, just raise an issue in this repo.