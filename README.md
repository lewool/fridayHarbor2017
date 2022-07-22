# fridayHarbor2017

This code imports the Brain Observatory stimulus set of natural images, and decomposes them based on a preset bank of Gabor filters. Once decomposed, the convolved images are clustered using HCA or K-means clustering into "similar" groups. These groupings inform a new index by which to order the image indices for the representational similarity matrices (RSMs).
As an alternative, the convolved images are clustered based on 'relevant pixels'—that is, the areas of the images that are 'seen' by the population receptive field. This produces a new image index for each experiment, by which the RSMs can be shuffled.
If the new indexing order is somehow more informative that the arbitrary starting order, one would expect to see more 'clumping' in the RSM (similar to how neuron correlation 'clumps' in the static-grating RSMs over similar SFs, orientations, etc.

I originally had envisioned this project using independent component analysis (ICA) to derive the filter bank first, then cluster based on those filters. I simplified this (mostly for the sake of time) by generating my own filter bank based on the static gratings used during imaging already, but the ICA code is included here for posterity.
