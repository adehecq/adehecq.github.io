---
layout: post
title: GeoRaster package for Python released
share: false
---

GeoRaster, a Python package which hugely simplifies the process of working with geographic rasters, is now available as a stable package on [conda-forge](http://conda-forge.github.io/) and [PyPI](http://www.pypi.org) with a GPLv3 licence. It provides high-level wrapping of the [GDAL](http://www.gdal.org) library, removing a lot of the complexity traditionally associated with importing GDAL-compatible datasets into Python. I actively maintain and develop the package, which also includes significant contributions from [Andrew Tedstone](https://atedstone.github.io).

If you already use [Anaconda](https://www.continuum.io/downloads) or [Miniconda](https://conda.io/miniconda.html) then you can easily try the package out on the command line:

```bash
conda create -n georaster_test
source activate georaster_test
conda install -c conda-forge python=3.5 ipython matplotlib georaster 
```

Then in an iPython shell:

```python
import georaster
import matplotlib.pyplot as plt
im = georaster.SingleBandRaster('myimage.tif')
plt.figure()
plt.imshow(im.r)
```

There's already plenty of [documentation available](http://georaster.readthedocs.io/en/latest/) to help you get started, and I'll be adding to this over the coming months. I've also got some extra functionality planned - keep an eye on the [GitHub wiki](https://github.com/atedstone/georaster/wiki) for more details.





