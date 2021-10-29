# rembg_cars
Extension of Rembg tool to remove backgrounds for adding a car custom model from library

<p style="display: flex;align-items: center;justify-content: center;">
  <img src="https://github.com/poropeza/rembg_cars/blob/main/examples/portada.png" width="600" />
</p>


### Requirements

* python 3.8 or newer

* torch and torchvision stable version (https://pytorch.org)

#### How to install torch/torchvision

Go to https://pytorch.org and scrool down to `INSTALL PYTORCH` section and follow the instructions.


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
- https://github.com/danielgatis/rembg


### License

Copyright (c) 2021 poropeza [Peter Oropeza](https://github.com/poropeza)

Licensed under [MIT License](./LICENSE.txt)
