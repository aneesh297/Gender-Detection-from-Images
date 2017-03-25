# Gender-Detection

## Dataset
- Images and Meta Data : https://data.vision.ee.ethz.ch/cvl/rrothe/imdb-wiki/static/wiki.tar.gz

- Cropped Images : https://data.vision.ee.ethz.ch/cvl/rrothe/imdb-wiki/static/wiki_crop.tar

## Data Preprocessing
- Few of the Images were corrupted and hence had to be removed from the dataset.
- Face Detection Algorithm (Cascade Classifier) is used to check if an image is valid or not.
- If a face is detected in the Image, Collect the required details (Full path and Gender) of the Image.
- Store the required data in a different .csv file.

## Framework/Library used
- Keras with Theano backend.
- OpenCV2 for Image Processing Algorithms.
- Pandas and NumPy for .csv and mathematical computations.

### Keras
- Is a Deep Learning Library which supports Theano and TensorFlow at backend.
- Keras is easier to install compared to other frameworks and had a better Documentation.
- https://keras.io/

## Data Model
- VGG-16 data model is used for training and testing.
- Such a data model contains a 16 layer network.
- Weights of the VGG16 Model used from : https://drive.google.com/file/d/0Bz7KyqmuGsilT0J5dmRCM0ROVHc/view?usp=sharing

## Results and Outcome
- A live video captures an image if a face detected in the frame.
- The cropped image (face) is sent to the pipeline where the a prediction is made with already saved model which is loaded globally.
- An additional layer (Sigmoid) is added at the flatten layer of the model.
- The Prediction lies between 0-1.
- Values near to 0 signifies Female. Values near 1 signifies Male.
- A Cross Validation Accuracy of 91.30% is achieved on the Dataset trained.

## Team Members
- Mohit Reddy (mohitreddy1996)
- Ambareesh Prakash (AeroDeath)
- Vilas M Bhat (vilas897)
- Aneesh Aithal (aneesh297)
- Somnath Sarkar (somnathsarkar)