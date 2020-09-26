# fashionMap

fashionMap is a study done trying technologys for clustering fashion images based on the clothes similarity. 

In order to analyse the images was used the neural network for image segmentation called [Mask R-CNN](https://github.com/matterport/Mask_RCNN). The model was applied to the [modanet](https://github.com/eBay/modanet) dataset and then upon the results was applied feature extraction to obtain a 2D t-SNE representation from the images, clustered by similarity. 

As a proof of concept it worked as expected, creating space for lots of future improvements.

Note: It was coded on colab notebooks to make use of its free GPUs, required by the algorithm. 

## Setup

### Installation

1. Download the Modanet annotations for the images;
    - Try [here](https://github.com/cad0p/maskrcnn-modanet/releases/tag/v1.0.3), the repository was not giving the annotations last time checked.
2. Download the [Paperdoll](https://github.com/kyamagu/paperdoll) Dataset annotated images; 
    - The entire dataset is on a 40gb sql file downloadble [here](https://github.com/kyamagu/paperdoll/blob/master/data/chictopia/chictopia.sql.gz)
    - To help access it and obtain the images follow this [tutorial](https://github.com/kyamagu/paperdoll/blob/master/data/chictopia/usage.ipynb)
3. Download the Mask R-CNN model and config the annotations model to it;
    - The model is imported, overwriten and used as a library. 
4. Apply the generated images to the feature extraction model (pretrained VGG, e.g.) and t-SNE.
    - Nothing to setup locally.

```bash
pip install foobar
```
## Snapshots 


## Future Work

```python
import foobar

foobar.pluralize('word') # returns 'words'
foobar.pluralize('goose') # returns 'geese'
foobar.singularize('phenomena') # returns 'phenomenon'
```
