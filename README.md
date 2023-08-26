# Image Classification using Deep Learning (CNN version)
The project consists of classifying images of dogs using Convolutional Neural Network (CNN). I will be developing my own CNN architecture at first and then test other architectures already trained on ImageNet. I will be using Stanford Dogs Dataset http://vision.stanford.edu/aditya86/ImageNetDogs/ containing 20580 images of dogs distributed on 120 dog breeds.

![image](https://github.com/wiskandar-coder/Image-Classification-using-Deep-Learning-CNN-version/assets/64427335/e7d01161-4122-45e3-b300-19bdaa9fde2a)

- Pre-treatment and preparation for the modelisation in '1_notebook':
    - Put all images at the same resolution
    - Transforming all images to RGB
    - Image augmentation using random horizontal flip , random rotation in +-30 degrees, random translation in +-10% of the image resolution, random luminosity in +-25%
    - Normalization of the color values in each pixel
    - Dividing the images into 490 batches (42 images/batch)
    - Dividing the batches into 80% train, 10% validation, and 10% test
  
- Modelisation in '1_notebook'\
  I started with developing my own model
    - Developing my own CNN model using multiple convolutional 2D layers and MaxPooling, and finally GlobalAveragePooling + DropOut + Dense layers
    - Train the model on the image without augmentation, and then with image augmentation
    - Finding the best learning rate for Adam optimizer using keras_tuner
    - Using the optimum learning rate for the final train of the model with augmented images
    - Check the performance of the model using train and validation accuracy and loss on each step, and finally the test loss and accuracy on the final train

  Then I used transfer learning to compare with my own model
    - 
- Application in https://github.com/wiskandar-coder/Auto-Tagging-Stackoverflow-API
  - An app will serve as a test where the user enter the title and the body of the questions, and the application will suggest tags for the user.
  - The application is deployed in HEROKU; the link to the app and API: https://auto-tagging-stackoverflow.herokuapp.com/

A powerpoint presentation of the project can be shared under request.
