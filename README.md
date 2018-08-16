# Region Growing

an extension of astropy that allows the user to define a region within fits data based on certain bundary conditions.  Sometimes you need a way to define a region given certain conditions such as the outer extremities of a dust shell around a star and this package helps you create those boundarys. These region growing images exist for rgb images but not for 2d arrays comonly found in fits files.



## Getting Started

move the module to the directory you're working with and import it like you would any other module

### Prerequisites

numpy

```
pip install numpy
```


### Example Tutorial
```
import RegionGrow
import astropy
from astropy.io import fits
import numpy

data=fits.getdata("......fits")  # a 2d array of a fits image

seed=(x,y)  #x and y are the pixel indicies where you want to start the grow from
threshold=.54 #the grow will not include anything below this threshold

grownregion=RegionGrow.region_growing(data,seed,threshold)

print(grownregion)


```

### method used

```
grow_region(img,seed,threshold)
```
Parameters:

  img-(2d array of floats from fits data) image to be grown with the threshold
  
  seed-(tuple) starting pixel (x,y) to grow region from
  
  threshold-(float) boundary condition to indicate where to stop the growing
  
Returns:

  growndata-2d array with every pixel not included in grow is set to zero

  


## Special Thanks

as an astonomy researcher I needed this method to study extended dust shells of ppn.  I origionally got this idea from 
[this stackoverflow thread.](https://stackoverflow.com/questions/43923648/region-growing-python)  It was origionally for rgb images but I changed it to handle astronomy data


## Authors

* **Andrew Torres**


## Acknowledgments

* Hat tip to anyone whose code was used
* My Mom
