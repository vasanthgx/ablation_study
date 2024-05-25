

![logo](https://github.com/vasanthgx/ablation_study/blob/main/images/logo.gif)


# Project Title


**Image Segmentaion with Breed Classification ML Project**
 <img src="https://github.com/Anmol-Baranwal/Cool-GIFs-For-GitHub/assets/74038190/b3fef2db-e671-4610-bb84-1d65533dc5fb" width="300" align='right'>

<br><br>






## Introduction

The fashion industry has seen a significant transformation with the integration of technology, and one such intersection is in the realm of image classification. The Fashion MNIST (FMNIST) dataset serves as a benchmark for evaluating machine learning and deep learning algorithms on complex visual data. This project explores the effectiveness of various neural network architectures using an ablation study to determine the optimal configuration for image classification tasks.


## Project Overview

This project aims to perform an ablation study on different Sequential Neural Network configurations to identify the best-performing model for the Fashion MNIST dataset. The study involves experimenting with varying numbers of hidden layers, units per layer, and dropout layers to observe their impact on model performance. Six different models are trained and evaluated based on their accuracy, total parameters, and overall efficiency.

## Key Features

- **Ablation Study**: Systematic evaluation of different neural network architectures.
- **Performance Metrics**: Comparison based on accuracy, number of parameters, and computational complexity.
- **Model Variants**: Includes models with different depths and complexities, ranging from simple to highly complex architectures.
- **Dropout Layers**: Inclusion of dropout layers in certain models to assess their impact on preventing overfitting.
- **Visualization**: Graphical representation of loss curves to understand the training dynamics of each model.
- **Tensor Board** : TensorBoard is employed as a crucial feature in this project to facilitate the comprehensive visualization and analysis of model performance. By integrating TensorBoard, we can effectively monitor the training process in real-time. Key logs captured include: Scalars, Images, Distributions , Graphs and Histograms.

### Implementation Details

The implementation involves the following steps:

1. **Data Preparation:**

Load the Fashion MNIST dataset.
Preprocess the data by normalizing the pixel values to a range of 0 to 1.

2. **Model Design:**

- Design six different Sequential Neural Network models with varying configurations:
	- Model 1: 3 hidden layers + dropout, 32 + 16 + 8 + 8 units.
	- Model 2: 3 hidden layers + dropout, 64 + 32 + 16 + 16 units.
	- Model 3: 1 hidden layer, 128 units.
	- Model 4: 3 hidden layers + dropout, 128 + 64 + 32 + 32 units.
	- Model 5: 2 hidden layers, 256 + 128 units.
	- Model 6: 5 hidden layers + dropout, 256 + 128 + 64 + 32 + 16 + 16 units.
	
3. **Training:**

- Train each model for 5 epochs.
- Use a consistent batch size and optimizer (e.g., Adam) across all models.
- Monitor the loss and accuracy during training.

4. **Evaluation:**

- Evaluate each model on the test set.
- Record accuracy, total parameters, and other relevant metrics.

5. Visualization:

- Plot loss curves for each model to visualize training and validation loss over epochs.
- Compare model performance based on the evaluation metrics.

### Dataset Details

[This dataset was obtained from this repository](https://www.robots.ox.ac.uk/~vgg/data/pets/)

The Fashion MNIST dataset is a collection of 70,000 grayscale images of 28x28 pixels, distributed into 10 categories representing different types of clothing and accessories. It is intended to serve as a more challenging alternative to the traditional MNIST dataset of handwritten digits.

- **Training Set:** 60,000 images
- **Test Set:** 10,000 images
- **Classes:**
	1. T-shirt/top
	2. Trouser
	3. Pullover
	4. Dress
	5. Coat
	6. Sandal
	7. Shirt
	8. Sneaker
	9. Bag
	10. Ankle boot
Each image is associated with a single label, and the goal is to classify the images into their respective categories. The dataset is pre-divided into a training set and a test set, facilitating straightforward evaluation of model performance.

By following this structured approach, the project effectively explores the impact of different neural network configurations on the FMNIST dataset, providing insights into the optimal design choices for image classification tasks.

### FMNIST Dataset

 ![alt text](https://github.com/vasanthgx/ablation_study/blob/main/images/fmnist.png)

### Analysis and Conclusion:

 ![alt text](https://github.com/vasanthgx/ablation_study/blob/main/images/ablation-1.png)
 
 ![alt text](https://github.com/vasanthgx/ablation_study/blob/main/images/ablation-2.png)
 
 ![alt text](https://github.com/vasanthgx/ablation_study/blob/main/images/ablation-3.png)

1. **Model Complexity and Performance:**

- The simplest model (Model 1) with fewer units and parameters performed the worst with 83.63% accuracy.

- Model 5, with moderate complexity (2 hidden layers with 256 and 128 units) and the highest accuracy (87.55%), indicates that increasing the number of units can significantly improve performance up to a certain point.

- Models with intermediate complexity (Models 2, 3, and 4) show that adding more hidden layers can improve accuracy, but the benefits diminish with too many layers and units (as seen in Model 4).
	
2. **Number of Parameters:**

- Models with higher parameters (Model 5 and Model 6) tend to perform better than simpler models. However, the performance gain diminishes as the model complexity increases beyond a certain threshold (Model 6 compared to Model 5).

3. **Dropout Layers:**

- Dropout layers are used in Models 1, 2, 4, and 6 to prevent overfitting. Models with dropout layers (2, 4, and 6) generally perform well, but the most complex model (Model 6) did not surpass Model 5 despite having dropout layers, suggesting a limit to the benefit of adding complexity.

4. **Optimal Model:**

- Model 5 appears to be the optimal configuration, balancing complexity and performance. It has the highest accuracy of 87.55% with a manageable number of parameters (235,146) and two hidden layers.

### Conclusion:

The study demonstrates that increasing the number of hidden layers and units generally improves the performance of neural networks on the FMNIST dataset up to a point. However, beyond a certain complexity, the gains in accuracy diminish. Dropout layers help in preventing overfitting and maintaining model performance. The optimal model found in this study (Model 5) suggests that a moderately complex architecture with sufficient units per layer provides the best performance. This finding highlights the importance of balancing model complexity and computational resources to achieve the best results.


	




## Key Takeaways

 1) **Architecture Selection** : The choice of architecture plays a crucial role in the success of the project. U-Net architecture is well-suited for image segmentation tasks, especially when precise delineation of objects or regions is required. On the other hand, ResNet-34 is a popular choice for image classification tasks due to its balance between depth and computational efficiency.
2) **Data Preparation and Augmentation**: Proper data preparation and augmentation are essential for training robust models. In image segmentation, labeled data with accurate pixel-level annotations are required, while in breed classification, labeled images with breed annotations are necessary. Augmentation techniques such as rotation, scaling, and flipping can help increase the diversity of the training data and improve the generalization of the models.
3) **Transfer Learning and Pre-trained Models**: Leveraging pre-trained models can significantly accelerate the training process and improve model performance, especially when dealing with limited training data. Transfer learning techniques, such as fine-tuning pre-trained models like ResNet-34 using FastAI or Timm libraries, allow the models to adapt to the specific characteristics of the dataset while retaining the knowledge learned from large-scale datasets.
4) **Evaluation Metrics and Performance Analysis**: Choosing appropriate evaluation metrics is crucial for assessing the performance of the models accurately. For image segmentation tasks, metrics such as Intersection over Union (IoU) or Dice Coefficient are commonly used to measure the overlap between predicted and ground truth masks. For breed classification, metrics like accuracy, precision, recall, and F1-score are typically used to evaluate classification performance.
5) **Deployment and Integration**: Once the models are trained and evaluated, deploying them into production environments requires careful consideration of factors such as scalability, latency, and integration with existing systems. FastAI and Timm libraries provide deployment options such as exporting models to ONNX format or integrating them into web applications using frameworks like Flask or FastAPI. Additionally, TensorFlow Serving can be used for serving TensorFlow models in production environments.


## How to Run

The code is built on Google Colab on an iPython Notebook. 

```bash
Simply download the repository, upload the notebook and dataset on colab, and hit play!
```


## Roadmap

The next steps would be 

- Incorporate chosen features into model development.
- Train the model and assess its performance through rigorous evaluation.
- Fine-tune the model if necessary for optimization.
- Analyze model predictions for insights into the problem domain.
- Deploy the model and monitor its performance, iterating as needed for continuous improvement.


## Libraries 

**Language:** Python

**Packages:** Sklearn, Matplotlib, fastai, mobilenetv2, pix2pix, timm


## FAQ

### 1) What is Otsu Thresholding and  its significance in Object Segmentaion ?

[Thresholding is used to create a binary image from a grayscale image .](https://scikit-image.org/docs/stable/auto_examples/segmentation/plot_thresholding.html)
[More Details](https://en.wikipedia.org/wiki/Otsu's_method)

Otsu thresholding, named after Nobuyuki Otsu, is a popular method used for automatic image thresholding. The goal of thresholding is to segment an image into two parts: foreground and background, or object and background, based on pixel intensity. Otsu's method calculates an optimal threshold value by maximizing the between-class variance of the pixel intensities.

Here's a simplified explanation of how it works:

1) Initially, Otsu's method considers all possible threshold values between the minimum and maximum intensity levels in the image.
2) For each potential threshold value, it divides the pixels into two classes: those with intensities below the threshold and those with intensities above the threshold.
3) Then, it calculates the variances of these two classes.
4) Otsu's method selects the threshold value that maximizes the between-class variance, meaning it chooses the threshold where the difference in intensity between the two classes is the most significant.


The significance of Otsu thresholding in object segmentation lies in its ability to **automatically determine an optimal threshold value without requiring manual intervention**. This is particularly useful in scenarios where the image has varying lighting conditions or when the desired object has a distinct contrast with the background. By accurately separating the foreground object from the background based on intensity, **Otsu thresholding forms the foundation for many image processing tasks such as object detection, recognition, and tracking**. It simplifies the process and makes it more robust and adaptable to different types of images.







### 2) What are Neural Networks ?

Neural networks are a class of machine learning algorithms inspired by the structure and function of the human brain's biological neural networks. These artificial neural networks (ANNs) consist of interconnected nodes, called neurons, organized into layers. Each neuron receives input signals, performs a computation, and then passes the result to the neurons in the next layer.

Components of a neural network:

1) **Input Layer**: This layer receives the input data. Each neuron in this layer represents a feature of the input data.
2) **Hidden Layers**: These are intermediary layers between the input and output layers. Each neuron in a hidden layer takes input from the previous layer, performs a computation using weights and biases, applies an activation function, and passes the result to the neurons in the next layer. Deep neural networks have multiple hidden layers, hence the term "deep" learning.
3) **Output Layer**: This layer produces the final output of the network. The number of neurons in the output layer depends on the type of task the neural network is designed for. For example, in a binary classification task, there would typically be one neuron in the output layer, while in a multi-class classification task, there would be one neuron for each class.
4) **Weights and Biases**: Neural networks learn from data by adjusting the weights and biases associated with each neuron's connections. These parameters determine the strength of connections between neurons and affect the output of each neuron.
5) **Activation Functions**: Activation functions introduce non-linearities into the network, allowing it to learn complex patterns in the data. Common activation functions include ReLU (Rectified Linear Unit), Sigmoid, and Tanh.


**Neural networks are trained using optimization algorithms such as gradient** and its variants, which adjust the weights and biases to minimize a loss function. During training, the network learns to make predictions by iteratively updating its parameters based on the comparison between its predictions and the ground truth labels in the training data.

Neural networks, especially deep neural networks, have shown remarkable performance in various tasks such as image recognition, natural language processing, speech recognition, and many more, making them a cornerstone of modern artificial intelligence and machine learning.




### 3) Can you explain Convolutional Neural Networks ?

Convolutional Neural Networks (CNNs) are a specialized type of neural network designed specifically for processing structured grid data, such as images. They are highly effective for tasks like image recognition, object detection, and image classification. CNNs are inspired by the organization of the animal visual cortex, where individual neurons respond to specific stimuli in a restricted region of the visual field.

Components and concepts in CNNs:

1) **Convolutional Layers**: The fundamental building blocks of CNNs are convolutional layers. Each convolutional layer consists of a set of learnable filters (also known as kernels or convolutional kernels). These filters slide or convolve across the input image, performing element-wise multiplication with the pixel values in the region they cover and then summing up the results to produce a feature map. This process captures spatial hierarchies of patterns in the input image.
2) **Pooling Layers**: Pooling layers are used to downsample the feature maps generated by convolutional layers. The most common pooling operation is max-pooling, which selects the maximum value from a region of the feature map. Pooling helps in reducing the spatial dimensions of the feature maps, making the network more computationally efficient and reducing overfitting by extracting the most salient features.
3) **Activation Functions**: Activation functions, such as ReLU (Rectified Linear Unit), are applied after convolutional and pooling operations to introduce non-linearity into the network. This allows the CNN to learn complex patterns and relationships in the data.
4) **Fully Connected Layers**: Towards the end of the CNN architecture, one or more fully connected layers are typically used to perform classification or regression tasks. These layers connect every neuron in one layer to every neuron in the next layer, allowing the network to learn high-level representations of the input data.
5) **Convolutional Neural Network Architecture**: CNN architectures vary depending on the specific task and dataset. Common architectures include LeNet, AlexNet, VGGNet, GoogLeNet (Inception), ResNet, and more. These architectures differ in terms of the number of layers, types of layers, and the arrangement of those layers.
6) **Training**: CNNs are trained using backpropagation and optimization algorithms like stochastic gradient descent (SGD) or its variants. During training, the network learns to adjust the weights of its filters and fully connected layers to minimize a predefined loss function, typically categorical cross-entropy for classification tasks.




CNNs have revolutionized the field of computer vision and have achieved state-of-the-art performance on various image-related tasks, including image classification, object detection, image segmentation, and more. They have also been adapted for other types of structured data, such as time-series data and 1D signal processing.

### 4) What is Pix2Pix?

Pix2Pix is a type of conditional generative adversarial network (GAN) architecture that learns a mapping from an input image to an output image. Specifically, it is designed for image-to-image translation tasks, where the goal is to generate a corresponding output image based on a given input image. Pix2Pix was introduced by Phillip Isola et al. in their 2016 paper titled "Image-to-Image Translation with Conditional Adversarial Networks."

Overview of how Pix2Pix works:

1) **Conditional GAN Framework**: Pix2Pix extends the basic GAN framework by introducing a conditional setting. In a traditional GAN, the generator network takes random noise as input and generates fake images, while the discriminator network distinguishes between real and fake images. In Pix2Pix, both the generator and discriminator networks receive not only the generated/fake images but also the corresponding input images as conditional inputs.
2) **Generator Network**: The generator network in Pix2Pix takes an input image and produces an output image that is transformed in some way based on the input. This transformation could involve changing the style, color, texture, or any other characteristics of the input image. The generator typically consists of an encoder-decoder architecture, with convolutional layers for feature extraction and upsampling layers for increasing the resolution of the output image.
3) **Discriminator Network**: The discriminator network in Pix2Pix evaluates pairs of images (input image, corresponding output image) and distinguishes between real pairs (input-output pairs from the training dataset) and fake pairs (input image, generated output image pairs). The discriminator is trained to differentiate between real and fake pairs, while the generator is trained to fool the discriminator by generating realistic output images.
4) **Training Objective**: Pix2Pix uses an adversarial loss, computed by the discriminator, to encourage the generator to produce output images that are indistinguishable from real images. Additionally, Pix2Pix also employs a pixel-wise L1 loss between the generated output image and the ground truth output image to ensure that the generated images are visually similar to the target images.
5) **Applications**: Pix2Pix can be applied to various image-to-image translation tasks, such as converting sketches to color images, generating satellite images from map images, converting day-time images to night-time images, and more.

Overall, Pix2Pix has demonstrated impressive results in a wide range of image translation tasks, making it a powerful tool for image synthesis and manipulation.

### 5) What is U-Net arhitecture ?

U-Net is a popular convolutional neural network architecture designed for semantic segmentation tasks, particularly in medical image analysis, where precise pixel-level segmentation is required. It was introduced by Olaf Ronneberger, Philipp Fischer, and Thomas Brox in their [2015 paper titled](https://arxiv.org/abs/1505.04597) **"U-Net: Convolutional Networks for Biomedical Image Segmentation."**

The U-Net architecture is characterized by its symmetric encoder-decoder structure, which enables the network to capture both local and global features while preserving spatial information. Here's an overview of its key components:

1) **Encoder Path**: The encoder path is composed of multiple convolutional blocks followed by max-pooling layers. These convolutional blocks perform feature extraction, gradually reducing the spatial dimensions of the input image while increasing the number of feature channels. Each convolutional block typically consists of convolutional layers, activation functions (such as ReLU), and optionally batch normalization to stabilize training.
2) **Decoder Path**: The decoder path mirrors the encoder path but in reverse. It consists of up-sampling layers (often transposed convolutions or bilinear upsampling) followed by concatenation with feature maps from the corresponding encoder path. These concatenated feature maps are then passed through convolutional blocks, which gradually increase the spatial dimensions while decreasing the number of feature channels. The goal of the decoder path is to recover the spatial details lost during the encoding stage.
3) **Skip Connections**: One of the key innovations of U-Net is the extensive use of skip connections between the encoder and decoder paths. These skip connections directly connect feature maps from the encoder to the corresponding decoder layers at the same spatial resolution. By providing high-resolution feature maps from earlier layers to later layers, skip connections help the network preserve fine-grained details and improve segmentation accuracy.
4) **Final Layer**: The final layer of the U-Net architecture typically consists of a 1x1 convolutional layer followed by a softmax activation function. This layer generates the segmentation mask by predicting the probability of each pixel belonging to the target classes. The output mask has the same spatial dimensions as the input image, with each pixel assigned a class label or probability score.
5) **Loss Function**: U-Net is trained using a pixel-wise loss function, such as cross-entropy loss or Dice loss, which measures the discrepancy between the predicted segmentation mask and the ground truth mask. The network parameters are optimized using gradient descent-based algorithms, such as Adam or stochastic gradient descent (SGD).

U-Net has become a popular choice for various medical image segmentation tasks, including organ segmentation, tumor detection, cell segmentation, and more. Its symmetric architecture, skip connections, and pixel-wise loss function make it well-suited for tasks requiring precise and detailed segmentation of structures within images.


## Acknowledgements


 - [Tensorflow datasets](https://www.tensorflow.org/datasets/overview)
 - [Image Segmentaion](https://www.tensorflow.org/tutorials/images/segmentation)
 - [Gradio crash course](https://www.youtube.com/watch?v=eE7CamOE-PA&list=LL&index=2)
 - [TensorFlow tutorials](https://www.youtube.com/playlist?list=PLQY2H8rRoyvwWuPiWnuTDBHe7I0fMSsfO)


## Contact

If you have any feedback/are interested in collaborating, please reach out to me at vasanth_1627@gmail.com


## License

[![MIT License](https://img.shields.io/badge/License-MIT-green.svg)](https://choosealicense.com/licenses/mit/)

