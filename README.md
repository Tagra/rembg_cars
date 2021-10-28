# rembg_carros
Extension of Rembg for adding custom model from library

# Rembg

[![Downloads](https://pepy.tech/badge/rembg)](https://pepy.tech/project/rembg)
[![Downloads](https://pepy.tech/badge/rembg/month)](https://pepy.tech/project/rembg/month)
[![Downloads](https://pepy.tech/badge/rembg/week)](https://pepy.tech/project/rembg/week)
[![License](https://img.shields.io/badge/License-MIT-blue.svg)](https://img.shields.io/badge/License-MIT-blue.svg)

Rembg is a tool to remove images background. That is it.

<p style="display: flex;align-items: center;justify-content: center;">
  <img src="https://raw.githubusercontent.com/danielgatis/rembg/master/examples/car-1.jpg" width="100" />
  <img src="https://raw.githubusercontent.com/danielgatis/rembg/master/examples/car-1.out.png" width="100" />
  <img src="https://raw.githubusercontent.com/danielgatis/rembg/master/examples/car-2.jpg" width="100" />
  <img src="https://raw.githubusercontent.com/danielgatis/rembg/master/examples/car-2.out.png" width="100" />
  <img src="https://raw.githubusercontent.com/danielgatis/rembg/master/examples/car-3.jpg" width="100" />
  <img src="https://raw.githubusercontent.com/danielgatis/rembg/master/examples/car-3.out.png" width="100" />
</p>

<p style="display: flex;align-items: center;justify-content: center;">
  <img src="https://raw.githubusercontent.com/danielgatis/rembg/master/examples/animal-1.jpg" width="100" />
  <img src="https://raw.githubusercontent.com/danielgatis/rembg/master/examples/animal-1.out.png" width="100" />
  <img src="https://raw.githubusercontent.com/danielgatis/rembg/master/examples/animal-2.jpg" width="100" />
  <img src="https://raw.githubusercontent.com/danielgatis/rembg/master/examples/animal-2.out.png" width="100" />
  <img src="https://raw.githubusercontent.com/danielgatis/rembg/master/examples/animal-3.jpg" width="100" />
  <img src="https://raw.githubusercontent.com/danielgatis/rembg/master/examples/animal-3.out.png" width="100" />
</p>

<p style="display: flex;align-items: center;justify-content: center;">
  <img src="https://raw.githubusercontent.com/danielgatis/rembg/master/examples/girl-1.jpg" width="100" />
  <img src="https://raw.githubusercontent.com/danielgatis/rembg/master/examples/girl-1.out.png" width="100" />
  <img src="https://raw.githubusercontent.com/danielgatis/rembg/master/examples/girl-2.jpg" width="100" />
  <img src="https://raw.githubusercontent.com/danielgatis/rembg/master/examples/girl-2.out.png" width="100" />
  <img src="https://raw.githubusercontent.com/danielgatis/rembg/master/examples/girl-3.jpg" width="100" />
  <img src="https://raw.githubusercontent.com/danielgatis/rembg/master/examples/girl-3.out.png" width="100" />
</p>

#### *** If you want to remove background from videos try this this fork: https://github.com/ecsplendid/rembg-greenscreen ***

### Requirements

* python 3.8 or newer

* torch and torchvision stable version (https://pytorch.org)

#### How to install torch/torchvision

Go to https://pytorch.org and scrool down to `INSTALL PYTORCH` section and follow the instructions.

For example:
```
PyTorch Build: Stable (1.7.1)
Your OS: Windows
Package: Pip
Language: Python
CUDA: None
```


### Installation

Install it from pypi

```bash
pip install rembg_carros
```


### Usage as a library

#### Example: Using PIL

In `app.py`
```python
from rembg.bg import remove
import numpy as np
import io
from PIL import Image
input_path = 'input.png'
output_path = 'out.png'
f = np.fromfile(input_path)
result = remove(f,model_name="carros")
img = Image.open(io.BytesIO(result)).convert("RGBA")
img.save(output_path)
```

Then run
```
python app.py
```

### References

- https://arxiv.org/pdf/2005.09007.pdf
- https://github.com/NathanUA/U-2-Net
- https://github.com/pymatting/pymatting


### License

Copyright (c) 2020-present [Daniel Gatis](https://github.com/danielgatis)

Licensed under [MIT License](./LICENSE.txt)
