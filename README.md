Chest X-ray Pneumonia Detection  
. Introduction  
I chose the Chest X-ray Pneumonia dataset because medical image analysis is a critical 
application of deep learning that can assist doctors in making faster and more accurate 
diagnoses. The goal is to build a system that can automatically distinguish between normal 
lungs and lungs affected by pneumonia from X-ray images.  
. Dataset Description  
The dataset contains X-ray images. For the training phase, I used images categorized 
into two classes: 'NORMAL' and 'PNEUMONIA'.  
• NORMAL: images  
• PNEUMONIA: imagesSince the classes are imbalanced (Pneumonia cases are 
significantly higher), the F-score was chosen as the primary metric for evaluation to 
ensure the model doesn't just predict the majority class.  
. Models Used  
I trained three traditional machine learning models using flattened pixel data (x 
grayscale images):  
. Logistic Regression: Achieved an F-score of It performed surprisingly well, finding a 
strong linear separation between classes.  
. Random Forest: Achieved an F-score of It was very good at recall but slightly less 
precise than Logistic Regression.  
. KNN (K-Nearest Neighbors): Achieved an F-score of It was the weakest among the three, 
as it struggled with the high dimensionality of raw pixel data.  
. Neural Network  
I built a Deep Neural Network (ANN) using Keras. The architecture included: 
• An Input layer for the , flattened pixels.  
• Two Dense layers ( and  neurons) with ReLU activation.  
• A Dropout layer (.) to prevent overfitting by randomly disabling neurons during training. 
• An Output layer with a Sigmoid activation for binary classification.I also used Early 
Stopping to stop training when the validation loss stopped improving.  
. Results & Comparison  
The Neural Network achieved an F-score of which is better than KNN and similar to Random 
Forest. However, Logistic Regression remained the top performer in this specific flattened-pixel 
scenario. While the Neural Network is more complex, it showed great stability and low overfitting 
due to the Dropout layer. For this size of dataset and flattened input, the extra complexity of the 
ANN didn't significantly outperform the linear efficiency of Logistic Regression.  
. What I Learned  
I learned that more complex models are not always better for every type of data representation. 
While Neural Networks are powerful, traditional models like Logistic Regression can be very 
effective if the data is prepared correctly. I also learned the importance of Dropout and Early 
Stopping in preventing a model from simply memorizing the training data, ensuring it performs 
well on new, unseen images. ٍ
ٍ
Student: Banah Al-Harbi 
Teacher: Raghad Al-Shammari
