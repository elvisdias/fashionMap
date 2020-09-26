# fashionMap

fashionMap is a study done trying technologys for clustering fashion images based on the clothes similarity. 

In order to analyse the images was used the neural network for image segmentation called [Mask R-CNN](https://github.com/matterport/Mask_RCNN). The model was applied to the [modanet](https://github.com/eBay/modanet) dataset and then upon the results was applied feature extraction to obtain a 2D t-SNE representation from the images, clustered by similarity. 

As a proof of concept it worked as expected, creating space for lots of future improvements.
Note: It was coded on colab notebooks to make use of its free GPUs, required by the algorithm. 

## Installation/Usage

Download 

```bash
pip install foobar
```

## Future Work

```python
import foobar

foobar.pluralize('word') # returns 'words'
foobar.pluralize('goose') # returns 'geese'
foobar.singularize('phenomena') # returns 'phenomenon'
```
