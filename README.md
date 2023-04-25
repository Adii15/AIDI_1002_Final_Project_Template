# AIDI_1002_Final_Project_Template

## Requirements
- Python 3.6+
- PyTorch
- TensorFlow
- efficientnet_pytorch
- PIL
- opencv-python
One can pip install all the above requirements

## Code Description
### Code Snippet 1
The first code snippet loads the EfficientNet models and applies them to classify an image. The preprocess_image function preprocesses the image by decoding it using TensorFlow, cropping it to the center and resizing it to the desired image size. The preprocessed image is then normalized using the mean and standard deviation of the ImageNet dataset. The EfficientNet.from_pretrained method is used to load the pre-trained EfficientNet models, and the input image is fed into the model to obtain the predictions. The top 5 predicted classes are printed along with their corresponding probabilities.

### Code Snippet 2
The second code snippet performs saliency detection on an image using the EfficientNet model. The transforms.Compose method is used to apply the necessary transformations to the image, which includes resizing and normalization. The pre-trained EfficientNet models are loaded using the models.efficientnet_bX(weights='EfficientNet_BX_Weights.DEFAULT') method. The image tensor is then passed through each of the models, and the gradients of the output with respect to the input image are computed using backpropagation. The gradients are then normalized and resized to match the original image size, and are used to perform saliency detection on the input image.

## Usage
To use these code snippets, simply copy the code and modify the file paths to your specific image and weight locations. The code can be executed in a Python environment or saved as a Python script and run from the command line.

Note: The EfficientNet model weights need to be downloaded and placed in the correct directory for the second code snippet to work using the pip install command.
