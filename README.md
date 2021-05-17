# Neural Networks for Digit Recognition

### **Summary and Problem Definition**

Image processing solutions have taken the financial industry by storm. Uploading a check can be done in seconds, with account balances adjusting at unprecedented speeds. Undertaking computer vision models requires a critical eye where model validity and size are diligently assessed. Models can become exceedingly complex, so initial testing of character recognition will be implemented on the MNIST dataset for classifying handwritten numbers.

### **Methods**

A defined project structure alleviates many concerns regarding the validity of the work being done. This project follows a typical end-to-end machine learning (ML) pipeline with 7 key steps. First the big picture is observed, then the data is procured, insights and perspective are found during data discovery, the data is prepared for ML models, models are selected and trained, fine-tuned, and finally the solution is presented. These steps will be condensed into the next four sections, where analysis will focus on processing time and test set accuracy.

#### *Research Design*

The data we are examining is well-defined and contains no null values. It is simple to work with and preprocessing is minimal. Within the MNIST dataset, there are handwritten digits that are less legible than others.  Data augmentations lessen the strength of outliers. Pictures are randomly adjusted in specified ways.

#### *Measurement*

Assessing the quality of our models is key to creating reproducible, scalable results. We focus on time and test set accuracy. The dataset is divided into groups consisting of training, validation, and test sets. The groups are shuffled in batches for cross-validation, and multiple epochs lower the variation of final results. The models are assessed by test set accuracy and timed processes.

#### *Statistical Methods*

The accuracy of each model is tested through both batch accuracy and validation set accuracy. Afterwards processing time and test set accuracy are measured. Neural networks with dense layers are compared to convolutional neural networks with dense layers for the same problem.

#### *Traditional and Machine Learning Methods*

Two approaches to modeling are assessed: primitive neural networks (NN) and convolutional neural networks (CNN). Four NN settings are compared with varying amounts hidden layers and neurons per layer. Hidden layer and neuron sizes create tradeoffs in accuracy and duration. These NN models create a graph of input layers, hidden layers, and 10 classification outputs corresponding to digits 0-9. The hidden layers are optimized with gradient descent through a learning rate and minimized loss function.

### **Overview of Programming Methods**

Data is processed and split into training, validation, and test sets. An individual digit is visualized, then a group for a general picture. Two levels on two experiment factors (2 layers vs 5 layers) are assessed. Four individual models are created with results summarized by time and accuracy. Afterwards, a CNN is created and compared to preliminary results. Data is standardized, resized before model training. Data is augmented to limit overfitting. Prediction results are output into a CSV file for assessment. Finally, methods are submitted to Kaggle under the MNIST digit recognizer challenge.

### **Results and Recommendations**

Convolutional neural networks perform admirably at digit recognition problems. Our model could be generalized to character recognition by adding new data. Image augmentation enhances results by limiting overfitting but adds extra time. Ultimately, the 2 layer 300, 100 neuron model yields the best results. 3 epochs take approximately 1 hour to generate with peak accuracy of 0.9987 (0.9955 on Kaggle) on the final epoch. Before augmentation, the model takes roughly half the time while maintaining accuracy over 99%. Therefore, if augmentation isn’t required, then it should be used sparingly. 
