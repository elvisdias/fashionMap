# fashionMap

fashionMap is a study done trying technologys for clustering fashion images based on the clothes similarity. 

In order to analyse the images was used the neural network for image segmentation called [Mask R-CNN](https://github.com/matterport/Mask_RCNN). The model was applied to the [modanet](https://github.com/eBay/modanet) dataset and then upon the results was applied feature extraction to obtain a 2D t-SNE representation from the images, clustered by similarity. 

This project was entirely conceptualize and put together by myself, altough I was happy to find very helpful content online to guide me through. As a proof of concept it worked as expected, creating space for lots of future improvements.

[Written project] (https://github.com/elvisdias/TCC). 

Note: It was coded on colab notebooks to make use of its free GPUs, required by the algorithm. 

## Setup 

### Installation 

1. Download the Modanet annotations for the images;
    - Try [here](https://github.com/cad0p/maskrcnn-modanet/releases/tag/v1.0.3), the repository was not giving the annotations last time checked.
2. Download the [Paperdoll](https://github.com/kyamagu/paperdoll) Dataset annotated images; 
    - The entire dataset is on a 40gb sql file downloadble [here](https://github.com/kyamagu/paperdoll/blob/master/data/chictopia/chictopia.sql.gz)
    - To help access it and obtain the images follow this [tutorial](https://github.com/kyamagu/paperdoll/blob/master/data/chictopia/usage.ipynb)
    - On my The file "Train Mask R-CNN on Modanet" file it does it all.
3. Download the Mask R-CNN model and config the annotations model to it;
    - The model is imported, overwriten and used as a library. 
    - If person segmentation is going to be used, the COCO dataset pre-trained model has to be download, the step is done when required.
4. Apply the generated images to the feature extraction model (pretrained VGG, e.g.) and t-SNE.
    - Nothing to setup locally.

### Usage

After setting up local files:
1. Train the model on "Train Mask R-CNN on Modanet" and save its weights;
2. Validate applying images to the segmentation files, which will generate and save new modified images locally;
3. Finally use these modified images on the t-SNE file.

## Snapshot 

<img src="https://github.com/elvisdias/fashionMap/blob/master/snapshots/t-sne.png"/>

<img src="https://github.com/elvisdias/fashionMap/blob/master/snapshots/rastfairy.PNG"/>

## Future Work

1. Study the same problem over DeepFashion [Dataset](https://github.com/switchablenorms/DeepFashion2), instead Modanet.
2. Go to the web, simmilarly to [Google's](https://experiments.withgoogle.com/business-of-fashion) implementation (published after I did this with same idea lol). 

## Colaboration

Feel free to contact me, pull request or modify it. 
