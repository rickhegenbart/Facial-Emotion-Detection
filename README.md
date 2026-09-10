# Facial-Emotion-Detection

> **MIT Professional Certificate in AI & Data Science**
>
> This project was completed as part of the MIT Professional Certificate in AI & Data Science program.
>
> [View the complete four-project certificate portfolio](https://github.com/users/rickhegenbart/projects/2)
>
Project Overview

This project uses deep learning and computer vision to classify facial emotions from image data. The goal was to build, train, and evaluate models that can identify facial expressions across four emotion categories:
Happy
Neutral
Sad
Surprise
The project compares custom grayscale convolutional neural networks against frozen pretrained transfer learning models to determine which approach performs better on low-resolution facial emotion images.
Objective
The main objective of this project was to evaluate whether task-specific custom CNN models trained on 48×48 grayscale images could outperform pretrained transfer learning models trained on RGB image inputs.
The project focused on answering the following question:
Can a custom grayscale CNN effectively classify facial emotions from low-resolution facial images, and how does it compare to frozen pretrained models such as VGG16, ResNet50V2, and EfficientNetB0?
Dataset
The dataset contains facial emotion images organized into training, validation, and test folders. Each image belongs to one of four emotion classes:
happy
neutral
sad
surprise
The dataset was split into:
train/
validation/
test/
This structure allowed the models to be trained, validated during development, and evaluated on unseen test data.
Tools and Libraries
This project was completed using Python and deep learning libraries, including:
Python
TensorFlow
Keras
NumPy
Pandas
Matplotlib
Seaborn
Scikit-learn
PIL
Google Colab
Modeling Approach
Two main modeling approaches were tested:
1. Custom Grayscale CNN Models
Custom convolutional neural networks were trained using 48×48 grayscale images. These models were designed specifically for the facial emotion classification task.
The custom CNN workflow included:
Image preprocessing
Data augmentation
Convolutional layers
Max pooling layers
Batch normalization
Dropout regularization
Dense classification layers
Early stopping
Model evaluation
Multiple CNN architectures were tested, including:
Baseline CNN
Second CNN
Complex CNN
The Complex CNN was the strongest custom model.
2. Transfer Learning Models
Frozen pretrained transfer learning models were also tested using 224×224 RGB image inputs.
The transfer learning models included:
VGG16
ResNet50V2
EfficientNetB0
These models used pretrained ImageNet weights, but their base layers were frozen during training. Only the classification head was trained on the facial emotion dataset.
Evaluation Methods
Model performance was evaluated using:
Training accuracy
Validation accuracy
Training loss
Validation loss
Test accuracy
Confusion matrix
Classification report
Precision
Recall
F1-score
This evaluation approach helped compare not only overall accuracy, but also how well each model performed across the four emotion classes.
Key Results
The custom grayscale CNN models performed better than the frozen pretrained transfer learning models.
The best-performing model was the Complex CNN, which achieved approximately:
81% test accuracy
The results showed that a task-specific grayscale CNN was better suited for this dataset than frozen pretrained RGB models.
Key Findings
The project produced several important findings:
The custom CNN models improved as the architecture became deeper and more regularized.
The Complex CNN achieved the strongest overall performance.
The surprise class was the easiest emotion for the model to classify.
The happy class also performed relatively well.
The neutral and sad classes were more difficult to separate because their visual differences were more subtle.
Frozen transfer learning models underperformed compared to the custom grayscale CNNs.
Low-resolution grayscale images still contained useful facial emotion signals when paired with an appropriate CNN architecture.
Why This Project Matters
Facial emotion detection is an important computer vision task with applications in:
Human-computer interaction
Behavioral analytics
Mental health technology
User experience research
Assistive technology
Social signal processing
This project demonstrates that model choice and preprocessing strategy matter. A smaller task-specific CNN can sometimes outperform larger pretrained models when the dataset, image format, and task requirements are better aligned.
Project Structure
facial-emotion-detection/
│
├── data/
│   ├── train/
│   ├── validation/
│   └── test/
│
├── notebooks/
│   └── facial_emotion_detection.ipynb
│
├── images/
│   ├── learning_curves.png
│   ├── confusion_matrix.png
│   └── sample_predictions.png
│
├── README.md
├── requirements.txt
└── .gitignore
How to Run the Project
1. Clone the repository
git clone https://github.com/your-username/facial-emotion-detection.git
2. Open the project folder
cd facial-emotion-detection
3. Install required packages
pip install -r requirements.txt
4. Open the notebook
You can run the project in Jupyter Notebook or Google Colab.
jupyter notebook
Then open:
notebooks/facial_emotion_detection.ipynb
Requirements
Example `requirements.txt`:
tensorflow
keras
numpy
pandas
matplotlib
seaborn
scikit-learn
pillow
Limitations
This project has several limitations:
The transfer learning models were frozen and not fine-tuned.
The dataset contained only four emotion classes.
Some emotion classes were more visually similar than others.
The model struggled more with subtle emotions such as neutral and sad.
Additional error analysis on misclassified images could improve interpretation.
Precision-recall curves and ROC analysis were not included.
Future Improvements
Future versions of this project could include:
Fine-tuning pretrained transfer learning models
Testing additional CNN architectures
Adding more emotion classes
Using a larger and more balanced dataset
Performing misclassification analysis
Testing the model on real-world webcam images
Deploying the model as a simple web application
Adding Grad-CAM or explainability visualizations
Conclusion
This project showed that a custom grayscale CNN can perform strongly on facial emotion detection when the model architecture is designed for the image format and classification task. The best Complex CNN model achieved approximately 81% test accuracy and outperformed frozen pretrained transfer learning models.
Overall, the project highlights the importance of matching the modeling approach to the dataset. Larger pretrained models are not always the best choice, especially when working with low-resolution grayscale images and a focused classification problem.
