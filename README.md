# Handwritten-Digit-recognition
The goal of this Repo is to use Deepl learning to categorize photos from the Handwritten Digit recognition Dataset. There are 42K of Pictures in the Handwritten Digit recognition collection, which includes 10 classes from 0 to 9. 
this dataset contains images of HandWritten belonging to 10 different Classes.

## About Dataset:
The data files train.csv and test.csv contain gray-scale images of hand-drawn digits, from zero through nine.
Each image is 28 pixels in height and 28 pixels in width, for a total of 784 pixels in total. Each pixel has a single pixel-value associated with it, indicating the lightness or darkness of that pixel, with higher numbers meaning darker. This pixel-value is an integer between 0 and 255, inclusive.
The training data set, (train.csv), has 785 columns. The first column, called "label", is the digit that was drawn by the user. The rest of the columns contain the pixel-values of the associated image.
Each pixel column in the training set has a name like pixelx, where x is an integer between 0 and 783, inclusive. To locate this pixel on the image, suppose that we have decomposed x as x = i * 28 + j, where i and j are integers between 0 and 27, inclusive. Then pixelx is located on row i and column j of a 28 x 28 matrix, (indexing by zero).
For example, pixel31 indicates the pixel that is in the fourth column from the left, and the second row from the top, as in the ascii-diagram below.

## Goal
The goal in this competition is to take an image of a handwritten single digit, and determine what that digit is.
For every in the test set, should predict the correct label.

## Installation Instructions:
- I have provided a Txt file that contains all the libraries that you need to run the notebook the file name is **"requirements.txt"** and also provides **"conda.yaml"** these two files for the final model.
- If you want to use mlflow and see the experiment tracking I did, you can use this command in cmd after activating the environment **"mlflow server --backend-store-uri sqlite:///mlflow.db --default-artifact-root ./artifacts --host 0.0.0.0 --port 5000"** before this you should download the database and the artifacts file.
- just download the dataset from this **[Dataset](https://www.kaggle.com/datasets/abdallahalidev/plantvillage-dataset)** then download the repo and here you are ready to run the code or you can use the model.h5 instead of all the steps.

## Usage Guide:
- I used the train dataset from the file **train.csv** to get the pixels of the images and convert thrm to float32.
  
 ![dataframe](https://github.com/Bassem-2000/Images/blob/main/dataframe.png?raw=true)
 
- after that, I used ImageDataGenerator from keras to load the data by applying some data augmentation to the training dataset here is the snippet
  
 ![ImageDataGenerator](https://github.com/Bassem-2000/Images/blob/main/ImageDataGenerator.png?raw=true)

## Model Architecture:
- I used the a simple Architecture by Vanila CNN and my  final model and architecture are done by applying some neurons in last part here is the snippet for the model summary
  
 ![Architecture](https://github.com/Bassem-2000/Images/blob/main/Architecture.png?raw=true)


## Evaluation:
- I used Two approaches to test the performance of the architecture and the model like accuracy and loss. here are the final model performance:
  
 ![Accuracy](https://github.com/Bassem-2000/Images/blob/main/accuracy.png?raw=true)
 ![Loss](https://github.com/Bassem-2000/Images/blob/main/Loss.png?raw=true)


## Example:
- I test the model with a random image and visualize it here you can see the image with the prediction:

 ![Example](https://github.com/Bassem-2000/Images/blob/main/Example.png?raw=true)


## Contact:

[<img alt="alt_text" width="30px" src="https://cdn2.iconfinder.com/data/icons/social-media-2285/512/1_Whatsapp2_colored_svg-512.png" />](https://wa.me/+201006491306)
&nbsp;&nbsp;
[<img alt="alt_text" width="30px" src="https://cdn2.iconfinder.com/data/icons/social-media-2285/512/1_Linkedin_unofficial_colored_svg-512.png" />](https://www.linkedin.com/in/bassem-ahmed-ahmed/)
&nbsp;&nbsp;
[<img alt="alt_text" width="30px" src="https://cdn4.iconfinder.com/data/icons/social-media-logos-6/512/112-gmail_email_mail-256.png" />](mailto:bassemahmed.am@gmail.com)
&nbsp;&nbsp;
[<img alt="alt_text" width="30px" src="https://cdn2.iconfinder.com/data/icons/social-media-2285/512/1_Facebook2_colored_svg-512.png" />](https://www.facebook.com/bassem.ahmed.7712/)

Can you please provide me with feedback on how I can improve myself and any ideas to improve the model, I am eager to receive any advice that can help me develop my skills.

&nbsp;&nbsp;
**Wish you a nice day :)**