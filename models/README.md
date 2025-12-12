# Machine Learning Final Project: Dog Breed Classification

## 1 Overview 
TODO

## 2 Dataset
This project uses the [Stanford Dogs Dataset](http://vision.stanford.edu/aditya86/ImageNetDogs/), which contains 20,580 images across 120 dog breeds, sourced from ImageNet. Each breed is provided as its own directory of images. The dataset should be split into train, validation, and test subsets using a stratified split to preserve class balance. 

## 3 Setup and Execution
1. Open `main.ipynb` in Google Colab using the link below.
    ## TODO
2. Select a GPU runtime (Recommended: A100).
3. Clone this repository to your Colab environment and move into it by running the following commands in a cell:
    ```bash
    !git clone https://github.com/marlenaalvino/dog-breed-classifier.git
    %cd dog-breed-classifier
    ```
4. Download the dataset into your Colab environment by running the following commands in a cell:
    ```bash
    !pip install gdown
    !gdown --id "1EerxeopxXaRF0seUZwtsP1WqKUD0I0vp" -O dog_images.zip
    !unzip -q dog_images.zip
    ```
5. Update `ORIGINAL_DATA_PATH` and `SPLIT_DATA_PATH` to reference the dataset’s `raw` and `processed` directories as needed.
6. Run the notebook cells in order to preprocess the data, train the model, and view results.

## 4 Results


## 5 References
- [Dog Breed Classification with Deep Learning](https://www.kaggle.com/code/crowwick/dog-breed-classification-with-deep-learning/notebook) by Miguel Vásquez
- [Dog Breed Classification using InceptionV3 CNN Model on Stanford Dogs Dataset](https://github.com/ayushdabra/stanford-dogs-dataset-classification/tree/master) by Ayush Dabra
- 
