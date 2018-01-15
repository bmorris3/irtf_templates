# IRTF Template spectra of Main-Sequence G/K/M stars

This repo contains a small HDF5 archive of the [IRTF spectral templates for GKM
stars](http://irtfweb.ifa.hawaii.edu/~spex/IRTF_Spectral_Library/). You can 
quickly open a spectrum for an M2V star with the following code: 

```python
>>> from irtf import IRTFTemplate

>>> template = IRTFTemplate('M2V')

>>> template.wavelength, template.flux
(array([ 0.8084653 ,  0.80866754,  0.80886978, ...,  2.41769958,
         2.41823721,  2.41877508], dtype=float32),
 array([  5.30554073e-12,   5.27335640e-12,   5.22798948e-12, ...,
          6.60529791e-13,   6.70602679e-13,   6.88728968e-13], dtype=float32))
          
>>> template.header
{'(B-V)': 1.5700000000000001,
 '(B-V)ERR': 'NAN',
 '(B-V)_0': 1.55,
 'ABSFERR': 0.010610100000000001,
 'BITPIX': -32,
 'COMMENT': 'Finally, missing data are denoted as NaN.',
 'DATE': '2009-12-01',
 'E(B-V)': 0.0200001,
 ...
```

To modify or re-create the HDF5 archive, run the notebook `create_archive.ipynb`. 

#### References

* Cushing, M.C., Rayner, J.T, & Vacca, W.D. (2005, ApJ, 623, 1115) 
* Rayner, J.T., Cushing, M.C., & Vacca, W.D. (2009, ApJS, 185, 289) 
