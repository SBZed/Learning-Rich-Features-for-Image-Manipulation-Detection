# Learning-Rich-Features-for-Image-Manipulation-Detection

Image tampering detection based on dual-stream Faster R-CNN network

# Code description

This experiment is mainly to learn and modify the code of the **Faster-RCNN-TensorFlow-Python3** GitHub warehouse of **[dBeker](https://github.com/dBeker)**, thus realizing double-flow tampering Detection.

Reference link:
https://github.com/dBeker/Faster-RCNN-TensorFlow-Python3

## Deployment instructions

First modify the `_lib` folder to `lib`.

Due to the limitation of GitHub file upload size, please download the preprocessed network and trained model from the network disk:
Link: https://pan.baidu.com/s/1eav5wfVrHFzeP1xCsp_fsQ
Extraction code: pm8m

Sharing includes two folders:

-   vgg16 network
-   Trained network parameters

*   Put the `.ckpt` file in the vgg16 network folder under the `Learning-Rich-Features-for-Image-Manipulation-Detection/data/imagenet_weights/` folder;
*   Put the four files in the trained network parameter folder under the `Learning-Rich-Features-for-Image-Manipulation-Detection/default/gene_2007_trainval/default/` folder.
*   Then run the `Dual Stream Faster R-CNN.ipynb` file directly.

### Run exception handling

-   When generating a data set, if it appears:
    ```python
    ModuleNotFoundError: No module named 'tensorflow'
    ```
    Need to download the `tensorflow` module, enter on the command line:
    ```python
    pip install tensorflow
    ```
-   Missing cython_bbox function
    You need to recompile bbox.c under your environment to generate the cython_bbox.so file, and execute it on the command line:
    ```python
    cd ./lib
    python setup.py build_ext -i
    ```
