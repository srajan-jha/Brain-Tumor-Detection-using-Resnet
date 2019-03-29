# Brain Tumor Detection using Resnet

## Preface

- The notebook was set up in Google Colaboratory Platform hence it starts with setting up the connection Google Drive upon which the image dataset was uploaded.
- The choice of the model and pre-processing of image is done after reading few research papers dealing with similar problem field.
- Access the folder containing the dataset and other related resources here : https://drive.google.com/open?id=106GuFx47zeSi0H-vvN1D69LY0MIC1aSI

## Methodology

- Data Located and split into train and test folders randomly
- Labels extracted from filenames in both the folders
- Train-test labels as well as inputs converted into Numpy Arrays
- CNN (ResNet) Model set up with loss function, optimizer, etc.
- Finally, model is trained with the processed images and scores are generated

## Insights

- **Label Extractor Method**
   - Function is utilized to extract the labels from the given file names from train and test directories.
   - These labels are stored in numpy arrays and saved in disk for future uses.
   - Similarly, train and test images are also converted into np arrays and saved into disk.

-  **Model Architecture**
    - Resnet-50 is used as the task included images and it’s the state-of-the-art CNN model.
    - For binary classification, the final layer is changed into a sigmoid unit. 
    - Loss function and optimizers are also set accordingly.

- **Preprocessing Images**
   - Rescaling, Horizontal flip and ZCA whitening is done via keras preprocessing module.

# Conclusion

- The model is trained and saved into disk with a training accuracy of 90% and test accuracy of ~ 87% .
- The Model did *overfit*, dropout or other regularising techniques could be used to avoid it.
- Also, I overlooked the *imbalance of the dataset* while training the model which yielded poor performance when printing the confusion matrix. 
 
