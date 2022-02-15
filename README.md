# TinyImageNetDataset

A [Tiny Imagenet Dataset](http://cs231n.stanford.edu/reports/2017/pdfs/930.pdf) for PyTorch, the usage is similar to ```torchvision.datasets```, this means each sample in the Dataset is a ```PIL.Image.Image```.

This script will download the dataset from the internet to your disk, and store preload data on your disk.

The script is a revision of [this](https://gist.github.com/z-a-f/b862013c0dc2b540cf96a123a6766e54).

## Prerequisites

```shell
pip install imageio tqdm
```

## Usage

For training data, use parameter ```mode='train'```, for validation data, use ```mode='val'```.

```python
from TinyImageNetDataset import TinyImageNetDataset

# for classification
ti = TinyImageNetDataset(root_dir="./path_to_folder", download=True, task='classification')

# for localization
ti = TinyImageNetDataset(root_dir="./path_to_folder", download=True, task='localization')
```
