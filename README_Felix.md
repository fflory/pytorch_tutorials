# Compute

On databricks I typically use an A10. You can open a terminal and display info with

# Python dependencies

I created a conda env in a hidden subfolder and installed the requirements with
```bash
pip install -r requirements.txt
```

# GPU support

On my databricks GPU is supported but not with cuda so some code will have to change

```python
import torch
if torch.backends.mps.is_available():
    mps_device = torch.device("mps")
    print("MPS device is available.")
else:
    print("MPS device is not available.")
```


# NVIDIA Cuda support

not available on Mac

```bash
nvidia-smi
```

# Notebooks
I generated the notebooks from 
- https://pytorch.org/tutorials/beginner/basics/tensorqs_tutorial.html

by manually downloading them and importing them into Databricks and adding them to the repo there.

# completed folders:
- [`beginner_source/basics`](beginner_source/basics): links to [local repo](beginner_source/basics), [remote repo](https://github.com/fflory/pytorch_tutorials/tree/main/beginner_source/basics), and [web](https://pytorch.org/tutorials/beginner/basics/)
