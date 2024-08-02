Sports Celebrity Image Classification

Overview

The "Sports Celebrity Image Classification" project aims to classify images of sports celebrities using machine learning techniques. The workflow includes face and eye detection, feature extraction using wavelet transforms, and classification using a Support Vector Machine (SVM) model.


Data Collection

The images of sports celebrities used in this project were scraped from the web using the Fatkun Batch Download Image extension. This tool allowed for the efficient gathering of a diverse set of images, which were then processed and used for training the classification model.


Preprocessing

Face and Eye Detection:

We utilized OpenCV's Haar cascades to detect faces and eyes in the images. Images with at least two eyes detected are retained for further processing.

For more information on Haar cascades, refer to the OpenCV documentation.

Face Cropping:

Detected facial regions are cropped from the images for focused analysis.

Feature Extraction:

Wavelet Transform: We applied the wavelet transform to extract features such as edges and facial characteristics. This enhances the model's ability to identify distinct features in the images.

Model Training

Data Preparation:

The dataset includes both raw images and wavelet-transformed images. These are combined and used to train the classifier.

Model Selection and Training:

We employed an SVM with an RBF kernel, fine-tuned using GridSearchCV to find the best parameters.

Other models, including Random Forest and Logistic Regression, were also evaluated, with SVM showing the best performance.

Performance Evaluation:

The SVM model achieved an accuracy of approximately 95% on the test set.
A confusion matrix was generated to evaluate the model's performance, visualized using a heatmap.

Model Saving
The trained SVM model and the class dictionary have been saved for future use. The model can be used to classify new images, and the class dictionary maps the predicted classes to celebrity names.


Conclusion

This project demonstrates an end-to-end pipeline for image classification, from data preprocessing to model training and evaluation. The use of wavelet transforms and SVM for classification proved effective in achieving high accuracy. Future work may include expanding the dataset, refining preprocessing steps, or exploring other classification algorithms.
