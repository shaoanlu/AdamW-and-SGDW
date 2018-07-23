# AdamW-and-SGDW
[Fixing Weight Decay Regularization in Adam](https://arxiv.org/abs/1711.05101)  
 Ilya Loshchilov, Frank Hutter

### [WIP Alert]

This repository is still work in progress.  
 The functionanity of AdamW and SGDW have not been fully checked. The implementation could be wrong.

## Usage

Please have a look at [demo_fashion_mnist.ipynb](https://github.com/shaoanlu/AdamW-and-SGDW/blob/master/demo_fashion_mnist.ipynb).

```python
from AdamW import AdamW
from SGDW import SGDW

# Suggested weight decay factor from the paper: w = w_norm * (b/B/T)**0.5
# b: batch size
# B: total number of training points per epoch
# T: total number of epochs
# w_norm: designed weight decay factor (w is the normalized one).

# weight_decay: float >= 0. The parameter for decoupled weight decay.
AdamW(lr=0.001, beta_1=0.9, beta_2=0.999, weight_decay=1e-4, epsilon=1e-8, decay=0.)
SGDW(lr=0.01, momentum=0., decay=0., weight_decay=1e-4, nesterov=False)
```
