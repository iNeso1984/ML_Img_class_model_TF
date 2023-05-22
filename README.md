
# Image Classification with TensorFlow

This project demonstrates a simple image classification model using TensorFlow. The model is trained to classify images as either cyanobacteria or salmonella. It can serve as a starting point for developing image classification models on larger datasets.

![cyanobacteria](https://cdn.myportfolio.com/4bebed9a-4022-46fc-83ca-66924fac1685/bee279e3-5d75-4935-84b9-8b1aca8c4d42_rw_1920.png?h=375a6b6f54e99c31987899389963f9d1)

## Dataset

The dataset used for training and evaluation consists of a small set of labeled images of cyanobacteria and salmonella.

Note: You will need at least 100 images of each organism. Lower quality images will produce inaccurate results. 

## Getting Started

#### To run the image classification model, follow these steps:

1. Clone this repository to your local machine:
<br>


2. Prepare your dataset as described in the Dataset section and ensure the folder structure matches the expected format.

3. Install the required dependencies. It is recommended to create a virtual environment for this project:
- pip install virtualenv
virtualenv myenv

- source myenv/bin/activate (Linux/Mac)
- myenv\Scripts\activate (Windows)
- pip install -r requirements.txt


## Training and Using the Model


1. Training the Model:

    - The model is trained using the `fit` function with the `train` dataset for 20 epochs.
    - The validation dataset `val` is used for monitoring the model's performance during training.
    - A TensorBoard callback is set up to log the training progress and visualize it later.

2. Visualizing Training Progress:

    - Two plots are generated to visualize the training progress: one for loss and another for accuracy.
    - The loss plot shows the training and validation loss over the epochs.
    - The accuracy plot shows the training and validation accuracy over the epochs.

3. Making Predictions:

    - The model is used to make predictions on test data.
    - Each batch in the test dataset is iterated, and the model predicts the output for the input data.
    - Additional evaluation metrics, such as precision, recall, and accuracy, are updated based on the predictions.

4. Classifying New Images:

    - To classify a new image, it needs to be preprocessed and passed through the model.
    - The image is preprocessed by resizing it and dividing by 255 to normalize the pixel values.
    - The processed image is then expanded to match the input shape of the model.
    - The model predicts the class probabilities for the image and compares it to a threshold (0.5).
    - If the predicted probability is above the threshold, the image is classified as "Salmonella".
    - Otherwise, it is classified as "Cyanobacteria".

## Next Steps

This basic image classification model can be improved and expanded in several ways. Here are some suggestions for further development:

- Collect a larger and more diverse dataset to train the model on.
- Experiment with different CNN architectures, such as VGG, ResNet, or Inception, to improve classification accuracy.
- Fine-tune the model on pre-trained weights from models trained on larger datasets, such as ImageNet.
- Incorporate data augmentation techniques to increase the variability of the training data.
- Deploy the model as a web application



