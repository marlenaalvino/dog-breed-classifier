# Machine Learning Final Project: Dog Breed Classification

## 1 Overview 
TODO

## 2 Dataset
The [Stanford Dogs Dataset](http://vision.stanford.edu/aditya86/ImageNetDogs/)

## 3 Setup and Execution
1. Open `main.ipynb` in Google Colab using the link below.
2. Select a GPU runtime (Recommended: A100).
3. Download the dataset into your Colab environment by running the following commands in a cell:
    ```bash
    !pip install gdown
    !gdown --id "1EerxeopxXaRF0seUZwtsP1WqKUD0I0vp" -O dog_images.zip
    !unzip -q dog_images.zip
    ```
4. Update `ORIGINAL_DATA_PATH` and `SPLIT_DATA_PATH` to reference the dataset’s `raw` and `processed` directories as needed.
5. Run the notebook cells in order to preprocess the data, train the model, and view results.

## 4 Results


## 5 References
- [Dog Breed Classification with Deep Learning](https://www.kaggle.com/code/crowwick/dog-breed-classification-with-deep-learning/notebook) by Miguel Vásquez
- [Dog Breed Classification using InceptionV3 CNN Model on Stanford Dogs Dataset](https://github.com/ayushdabra/stanford-dogs-dataset-classification/tree/master) by Ayush Dabra
- 
