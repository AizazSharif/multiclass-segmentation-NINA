## Steps to approach this problem:

1. Understand the data: Sentinel-2 image tiles and land cover masks are read using rioxarray library.
2. Plot the data as images (already done by the interviewer).
3. Understand the dimensions of input and output for multiclass segmentation.
4. Create dictionaries for images and masks.
5. Add a jaccard_score function.
6. Create a deep neural netowrk model. For the given problem, we can start with base U-net model using tensorflow. It can also be done in PyTorch.
7. Run unet_model.summary() and solve the errors within hidden layers, input layer, or output layer.
8. Use tf.data.Dataset for now to add images and masks together for training and validation.
9. Compile using unet_model.compile and add jaccard_score as your metric.
10. Run unet_model.fit to train your model with certain epochs.
11. Plot the results using val_scene directory. 


## Issues faced during the tasks:
1. Understanding the data type: The images ands masks are provided as xarray using rioxarray library. Having more knowledge about the library functions can help in preprocessing data.
2. Errors in building Unet model: There were usual model building errors, this time due to uneven width and height dimensions which wasted a lot of time.
3. Decision about cropping images: For the sake of time, I decided to crop the images to a fixed dimension size (6,240,240) to compile the model successfully.   

## Future Consideration:
1. Look into image transformation process: Check whether we require steps such as data normalization, resizing, etc.
2. Create a Unet multiclass segmentation model that can accept uneven width and height inputs.
3. Avoid data cropping and consider the original dimensions for training and validating your results.
   
