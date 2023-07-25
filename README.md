# Tree Counting

Counting trees from drone images used to to take many hours of manual work. Now, thanks to AI, it can be achieved in just a few minutes.

## Dataset

Here we use the Yosemite dataset which is a benchmark dataset used for performing tree counting using areial images.

The study area is a 2262.5m x 4525.1m rectangular area (19200 x 38400 pixels in image). We have labeled the position of each individual tree in the study area. There are totally 98,949 individual trees labeled.

For more information, click [here](https://github.com/nightonion/yosemite-tree-dataset).

## Crowd Counting

Here we aim to adopt the method of generally used crowd counting method of individuals, and extrapolate its use in the domain of tree counting using areial images.

## Approach

The dataset is created by segmenting the given huge image into 800 images each of size 960x960px. For which we expect to do either a 80:20 or a 70:30 train:test split.

The given massive image is, for simplicity, coverted into a grey scale image and thereafter the segmentation is to be done.

The following steps are taken:.
  1) Here we use the `magick` CLI to convert the massive image into its corresponding greyscale.
  2) Then, we use the `split-image` package in pypi to split the image into 800 subimages comprising of the train-test data.
  
 **NOTE:** *Here we tend NOT to use python packages like `sk-image` and `PIL` to cobvert to greyscale since the image is way too large for it to process.*
