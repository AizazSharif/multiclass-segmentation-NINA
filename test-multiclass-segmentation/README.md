# Task:

Within **2 hours** please attempt to build, train and test a deep learning model that can segment Sentinel-2 image tiles into a 6-class land cover map. Specifically please do the following:
1. train your model only on images and masks in the *tra_scene/* and *tra_truth/* directory.
2. evaluate your model only on images and masks in the *val_scene/* and *val_truth/* directory
3. during evaluation, please use the [jaccard_score](https://scikit-learn.org/stable/modules/generated/sklearn.metrics.jaccard_score.html) function. Calculate it per class, and the average score across all classes.
4. use your best model to make inference over the first image in the *val_scene/* directory. Plot the resulting segmentation alongside the true land cover mask.
5. navigate back to the Microsoft Form we send you and submit a link to the GitHub repo where you have saved your code along with the following:
    - a jpeg image (e.g. screenshot or graph) showing the highest jaccard_score (averaged over all classes)
    - a jpeg figure showing the resulting segmentation map (point 4 above)

The Sentinel-2 image tiles and land cover masks have been made available in this repository along with a short Python notebook to get you started. 

When we talk about land cover, we mean physical land types, such as vegetation (ex. grass, bushes, trees, crops), built structures, bare ground, water, etc. We map and monitor land cover so that we can account for the availability and changes in the quality or quantity of nature.

If you encounter a problem with the Micosoft Form, please send your code and outputs to roald.vang@nina.no as soon as you are finished. We will calculate the time taken as the difference between when you opened the Microsoft Forms link and clicked "Submit", or between when you opened the forms link and when Roald Vang receives your email. If you are over-time, this will count against you in the evaluation of your work. So do as much as you can witin 4 hours and don't stress if you cannot complete all the points listed above!

### Repository Structure

```bash
test-multiclass-segmentation/
├── dset-s2-grunnkart/
│   ├── tra_scene
|   ├── tra_truth
|   ├── val_scene
│   └── val_truth
├── multiclass_segmentation.ipynb
└── README.md
