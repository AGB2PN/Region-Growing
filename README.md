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

  


## Special thanks

as an astonomy researcher I needed this method to study extended dust shells of ppn.  I origionally got this idea from 

Please read [CONTRIBUTING.md](https://gist.github.com/PurpleBooth/b24679402957c63ec426) 

## Versioning

We use [SemVer](http://semver.org/) for versioning. For the versions available, see the [tags on this repository](https://github.com/your/project/tags). 

## Authors

* **Billie Thompson** - *Initial work* - [PurpleBooth](https://github.com/PurpleBooth)

See also the list of [contributors](https://github.com/your/project/contributors) who participated in this project.

## License

This project is licensed under the MIT License - see the [LICENSE.md](LICENSE.md) file for details

## Acknowledgments

* Hat tip to anyone whose code was used
* Inspiration
* etc 
