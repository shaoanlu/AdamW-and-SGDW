# AdamW-and-SGDW
[Fixing Weight Decay Regularization in Adam](https://arxiv.org/abs/1711.05101)  
 Ilya Loshchilov, Frank Hutter

### [WIP Alert]

This repository is still work in progress.  
 The functionanity of AdamW and SGDW have not been fully checked. The implementation could be wrong.

## Usage

Please see [demo_mnist.ipynb](https://github.com/shaoanlu/AdamW-and-SGDW/blob/master/demo_mnist.ipynb).

```python
from AdamW import AdamW
from SGDW import SGDW

# weight_decay: float >= 0. The parameter for decoupled weight decay.
AdamW(lr=0.001, beta_1=0.9, beta_2=0.999, weight_decay=1e-4, epsilon=1e-8, decay=0.)
SGDW(lr=0.01, momentum=0., decay=0., weight_decay=1e-4, nesterov=False)
```
