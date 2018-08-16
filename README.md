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

grow_region(img,seed,threshold)

*parameters

**things

```
Give an example
```

## Deployment

Add additional notes about how to deploy this on a live system

## Built With

* [Dropwizard](http://www.dropwizard.io/1.0.2/docs/) - The web framework used
* [Maven](https://maven.apache.org/) - Dependency Management
* [ROME](https://rometools.github.io/rome/) - Used to generate RSS Feeds

## Contributing

Please read [CONTRIBUTING.md](https://gist.github.com/PurpleBooth/b24679402957c63ec426) for details on our code of conduct, and the process for submitting pull requests to us.

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
