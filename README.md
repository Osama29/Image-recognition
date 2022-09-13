# Image-Recognition

## Introduction
Garbage classification is an important and common issues for human life especially in
the topic of protect the natural world. The process of recognise and classify the
garbage by human will take a long terms and high labour costs, to solve the problem
Machine Vision System (MVS) is introduced.

Machine Vision system is a technology that enables a computing device to inspect,
evaluate and identify a still or moving image of an object (Techopedia, 2021) . The
accuracy of the system is based on how well the system can recognised the object. To
recognise the object, feature extraction and processing are useful; however, it is
challenging for the machine vision systems to recognise objects in images with little
effort, so a few algorithms such as Artificial Neural Network and Convolutional
Neural Network are introduced to overcome the problem.

In this laboratory exercise, Convolutional Neural Network (CNN) is introduced and
used on the topic of garbage classification. Convolutional Neural Network (CNN) is a
network architecture for deep learning which learns directly from data, eliminating the
need for manual feature extraction (MathWorks, 2020) . CNN can produce high
accurate recognition results and easier to train it for a new recognition task in the
machine vision system. The system is building to recognise the images of garbage in
dataset and classify them into 6 types, which are glass, plastic, cardboard, metal,
paper, and general waste.

## Objective
The objectives of this laboratory exercise are to understand and apply the techniques
in machine vision particularly feature representation and analyse the applications of
machine vision in real life problem.

## Proposed Method and Methodology
As stated above, among the discussion Convolutional Neural Network (CNN)
is chosen in solve the garbage classification problem. In deep learning, CNN is a class
of deep neural network which commonly applied to analyze visual image (Ramuka,
2021) . The deep neural network is interest in using the hidden layer in the neural
network to recognize the features. There are 3 different layers that constitute in CNN,
which are convolution layer, pooling layer, and fully connected layer. Complexity of
the neural network is dependent on the number of layers included in a built CNN
model. Furthermore, the number of layers of CNN also affect the accuracy of
predictions of the model. The diagram below is showing the concept of deep learning
neural network for pattern recognition:

![1](https://user-images.githubusercontent.com/53341547/189937408-6168757c-8f32-43f3-8fbe-ae7e034dbbc0.png)

First, the convolution layer is used to extract the features from the input image
and uses feature detector also known as filter to produce output feature map. This
layer performs a dot product between 2 matrices, the matrices are the restricted
portion of the receptive field and convolutional mask; kernel mask is used in this
experiment. The kernel mask is smaller than the image, but it is more in-depth. For
example, when undergoing the forward pass process, the kernel slides across the
height and width of the receptive region of the image. A two-dimensional
representation of the image is produced and known as an activation map that gives the
response of the kernel at each spatial portion of the image (Mishra, 2020) . In the
algorithm build, Kernel size of 3 shows that there will be a 3x3 = 9 output features
reflected since size of kernel shows the number of features reflected after 2D
convolution. This sliding size of the kernel is called a stride, to calculate the size of
output volume the formula in Figure 2 is used.

![2](https://user-images.githubusercontent.com/53341547/189937865-fa39932d-000b-4006-ae82-b831ef081c4c.png)

When the filter does not perfectly fit the input image, a zero-padding process is
undergoing, it sets all elements that fall outside the input matrix becomes zero,
producing a large or equally sized output (IBM Cloud Education, 2020). There are 3
types of padding, which are valid padding, it dropped the last convolution if
dimensions do not align; same padding, it ensures the equality of size between output
and input layers; and full padding, it add zeros to the border of input to enlarge size
the output layer. In the algorithm built, same padding was used. Besides that, process
called Rectified Linear Unit (ReLU) is introduced for a non-linear operation in CNN
to ensure the network can analyze the input in real world data which have nonnegative
linear values.

Next, the pooling layer also called subsampling is helping to reduce the spatial
size of the representation by decreases the required amount of computation and
weights but retains the important information. There are several types of pooling: (1)
Max pooling, it takes the largest element from the rectified feature map;(2) Average
pooling, it calculates the average value within the receptive field and send to the
output array; and (3) Sum pooling, it sums all the elements from the rectified feature
map and send to the output array. Figure 3 is the example of max pooling.

