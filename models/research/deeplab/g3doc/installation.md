# Installation

## Dependencies

DeepLab depends on the following libraries:

*   Numpy
*   Pillow 1.0
*   tf Slim (which is included in the "tensorflow/models/research/" checkout)
*   Jupyter notebook
*   Matplotlib
*   Tensorflow

For detailed steps to install Tensorflow, follow the [Tensorflow installation
instructions](https://www.tensorflow.org/install/). A typical user can install
Tensorflow using one of the following commands:

```bash
# For CPU
pip install tensorflow
# For GPU
pip install tensorflow-gpu
```

The remaining libraries can be installed on Ubuntu 14.04 using via apt-get:

```bash
sudo apt-get install python-pil python-numpy 
sudo pip install jupyter
sudo pip install matplotlib
```

## Add Libraries to PYTHONPATH

When running locally, the tensorflow/models/research/ and slim directories
should be appended to PYTHONPATH. This can be done by running the following from
tensorflow/models/research/:

```bash
# From tensorflow/models/research/
export PYTHONPATH=$PYTHONPATH:`pwd`:`pwd`/slim
```

Note: This command needs to run from every new terminal you start. If you wish
to avoid running this manually, you can add it as a new line to the end of your
~/.bashrc file.

# Testing the Installation

You can test if you have successfully installed the Tensorflow DeepLab by
running the following commands:

Quick test by running model_test.py:

```bash
# From tensorflow/models/research/
python deeplab/model_test.py
```

Quick running the whole code on the PASCAL VOC 2012 dataset:

```bash
# From tensorflow/models/research/deeplab
sh local_test.sh
```

