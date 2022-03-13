## Object Detection YOLOv5

#### Getting Started

Clone repo and install requirements.txt in a Python>=3.7.0 environment,
including PyTorch>=1.7. Models and datasets download automatically from the
latest YOLOv5 release.

```
git clone https://github.com/ultralytics/yolov5
cd yolov5 
pip install -r requirements.txt
```

#### Train on Custom Data

If you're training on an Intel Mac, you might encounter the error:

```
OMP: Error #15: Initializing libiomp5.dylib, but found libomp.dylib already initialized.
```

The solution ([found on Stack Overflow](https://stackoverflow.com/questions/53014306/error-15-initializing-libiomp5-dylib-but-found-libiomp5-dylib-already-initial)) for this is to:

```
conda update --all --yes
conda install nomkl
```

We're using a few datasets to train on.

##### Datasets

- SKU110K