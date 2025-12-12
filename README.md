# Machine Learning Final Project: Dog Breed Classification

## 1 Overview 
This project implements a dog-breed classification system using transfer learning on a pretrained EfficientNet-B3 model. By leveraging EfficientNet-B3’s ImageNet-trained weights, the system accelerates convergence and enhances fine-grained feature extraction, enabling it to distinguish subtle visual differences across breeds with far less data and training time than training a CNN from scratch. The pipeline includes preprocessing utilities for loading and augmenting images, a configurable training script with options for freezing or unfreezing layers, and tracking of accuracy and loss across epochs to evaluate convergence. Performance is measured on a held-out test set, with additional tools for generating predictions and inspecting misclassifications.

## 2 Dataset
This project uses the [Stanford Dogs Dataset](http://vision.stanford.edu/aditya86/ImageNetDogs/), which contains 20,580 images across 120 dog breeds, sourced from ImageNet. Each breed is provided as its own directory of images. The dataset is typically split into train, validation, and test subsets using a stratified split to preserve class balance. 

## 3 Setup and Execution
1. Open the notebook in Google Colab using the link below:

    <a href="https://colab.research.google.com/github/marlenaalvino/dog-breed-classifier/blob/main/dog_breed_classifier.ipynb" target="_parent"><img src="https://colab.research.google.com/assets/colab-badge.svg" alt="Open In Colab"/></a>
2. In Colab, switch to a GPU runtime (recommended: A100).
3. Clone the repository and move into the project directory:
    ```bash
    !git clone https://github.com/marlenaalvino/dog-breed-classifier.git
    %cd dog-breed-classifier
    ```
4. Download and extract the dataset:
    ```bash
    !pip install gdown
    !gdown --id "1EerxeopxXaRF0seUZwtsP1WqKUD0I0vp" -O dog_images.zip
    !unzip -q dog_images.zip
    ```
5. Run all the notebook cells in order to preprocess the data, train the model, and view the final results.

## 4 Results
The final EfficientNet-B3 model demonstrated strong performance on the dog-breed classification task. After training, the model reached a validation accuracy of 89.08% with a corresponding validation loss of 1.113, indicating stable convergence and effective feature transfer from the pretrained backbone.

On the held-out test set, the model achieved an overall accuracy of 88.41% and a test loss of 0.6017. Top-5 accuracy reached 98.82%, showing that the correct breed was almost always included among the highest-confidence predictions even when the top-1 prediction was incorrect.

For additional results—including training history, confusion matrices, and per-breed accuracy—see the `dog_breed_classifier.ipynb` notebook. The best and final model weights are available as well, linked [here](https://drive.google.com/drive/folders/1E6r-n5nr4F89QVay8LwD8JmvweXsm0wh?usp=drive_link).

## 5 References
- [Dog Breed Classification with Deep Learning](https://www.kaggle.com/code/crowwick/dog-breed-classification-with-deep-learning/notebook) by Miguel Vásquez
- [Dog Breed Classification using InceptionV3 CNN Model on Stanford Dogs Dataset](https://github.com/ayushdabra/stanford-dogs-dataset-classification/tree/master) by Ayush Dabra