# Object Detection with YOLOv5

## Getting Started

Clone this repo and install `requirements.txt` in a `Python>=3.7.0` environment, 
including `PyTorch>=1.7`. The models and datasets download automatically from the
latest YOLOv5 release.

```bash
git clone https://github.com/datasith/ds-experiments-yolov5
cd ds-experiments-yolov5
git submodule init
git submodule update
pip install -r yolov5/requirements.txt
```

Alternatively, use the links provided below to open them in **Google Colab**.

## Training on Custom Data

All the notebooks in this repo make use of the <a href="https://github.com/ultralytics">@Ultralytics</a> scripts for training 
YOLOv5 models on custom data.

<table class="tg">
  <tr>
    <th class="tg-yw4l"><b>Name</b></th>
    <th class="tg-yw4l"><b>Dataset</b></th>
    <th class="tg-yw4l"><b>Description</b></th>    
    <th class="tg-yw4l"><b>Notebook</b></th>
  </tr>
  
  <tr>
    <td class="tg-yw4l">Demo SKU110K</td>
    <td class="tg-yw4l"><a href="https://www.kaggle.com/datasets/thedatasith/sku110k-annotations">SKU110K</a></td>    
    <td class="tg-yw4l">Densely packed images of objects on shelves</td>
    <td class="tg-yw4l"><a href="https://colab.research.google.com/github/datasith/ds-experiments-yolov5/blob/main/demo_sku110k.ipynb">
      <img src="https://colab.research.google.com/assets/colab-badge.svg" width="" >
    </a></td>
  </tr>

  <tr>
    <td class="tg-yw4l">Demo CoTS (Kaggle)</td>
    <td class="tg-yw4l"><a href="https://www.kaggle.com/competitions/tensorflow-great-barrier-reef/data">CoTS</a></td>    
    <td class="tg-yw4l">Detect Crown-of-Thorns Starfish in real-time by training a model on underwater videos of coral reefs</td>
    <td class="tg-yw4l"><a href="https://colab.research.google.com/github/datasith/ds-experiments-yolov5/blob/main/demo_kaggle_cots.ipynb">
      <img src="https://colab.research.google.com/assets/colab-badge.svg" width="" >
    </a></td>
  </tr>  
</table>

## Errata

For running the notebooks locally, if you're training on an Intel Mac, you might 
encounter the error below after installing the requirements:

```bash
OMP: Error #15: Initializing libiomp5.dylib, but found libomp.dylib already initialized.
```

The solution ([found on Stack Overflow](https://stackoverflow.com/questions/53014306/error-15-initializing-libiomp5-dylib-but-found-libiomp5-dylib-already-initial)) for this is to:

```bash
conda update --all --yes
conda install nomkl
```

## Datasets

I'm using a few datasets to train on. This list will be updated with each added one.

- SKU110K
- CoTS (Kaggle)

---

🐞 If you find any bugs or have any questions regarding these notebooks, please open an issue. I'll address it as soon as I can. 

🐦 Reach out on [Twitter](https://twitter.com/datasith) if you have any questions. 

🔗 Please cite the following if you use the code examples in your research:
```bibtex
@misc{zabala2022ml,
  author    = {Zabala, Francisco},
  title     = {DS Experiments YOLOv5},
  journal   = {GitHub},
  year      = {2022},
  url       = {https://github.com/datasith/ds-experiments-yolov5},
}
```
