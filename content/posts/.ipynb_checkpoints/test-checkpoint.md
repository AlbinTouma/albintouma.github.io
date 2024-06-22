---
jupyter:
  jupytext:
    formats: ipynb,md
    text_representation:
      extension: .md
      format_name: markdown
      format_version: '1.3'
      jupytext_version: 1.16.2
  kernelspec:
    display_name: Python 3 (ipykernel)
    language: python
    name: python3
---

---
title: hello
draft: false
---


# Testing ipynb to md

```python
x = 2
print(x)
```

```python
import numpy as np


num_bars = 10
x = np.random.seed(0)
v = np.random.randint(1, 100, size=num_bars)
labels = [f'Label {i}' for i in range(num_bars)]

v

```
