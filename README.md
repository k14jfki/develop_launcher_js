# kubernetes-widget

`kubernetes-widget` is a Python library which makes experimental game engine for 2D easier by providing:

* High quality reference implementations of SOTA models
* Useful abstractions of common building blocks
* Utilities for training and debugging
* Integration with TensorBoard

## Installation

To install `kubernetes-widget`, clone and install requirements:

```
git clone https://github.com/user/kubernetes-widget
cd kubernetes-widget
pip install -r requirements.txt
```

Run tests:

```
python -m unittest discover
```

## Reproducing Results

All models implement a `reproduce` function:

```
python train.py --model handler --logdir /tmp/run --use-cuda
```

View metrics:

```
tensorboard --logdir /tmp/run
```

## Example - core

```python
from kubernetes-widget import models

model = models.core(in_channels=1, out_channels=1)
model(batch)
```

## Supported Algorithms

| Algorithm | Score (nats) | Links |
| --- | --- | --- |
| handler | **78.61** | [Code](#), [Paper](#) |
| core | 79.17 | [Code](#), [Paper](#) |

## Contributing

Contributions welcome!

