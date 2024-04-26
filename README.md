# brain-tumor-classification

Brain tumors are a major global health concern that require early and precise diagnosis in order to effectively treat. This work offers a novel method for classifying brain tumors using deep learning methods. Deep Learning is a new machine learning field that gained a lot of interest over the past few years. It was widely applied to several applications and proven to be a powerful machine learning tool for many of the complex problem. In this paper we used Deep Neural Network classifier which is one of the DL architectures for classifying a dataset MRIs into 4 classes e.g. normal, glioma, meningioma and pituitary tumors. Magnetic resonance imaging (MRI) and computed tomography (CT) scans are two of the many medical imaging modalities included in the dataset used for training and evaluation. The classifier was combined with the grayscaling and denoising after which VGG-16 model is built and the evaluation of the performance was quite good over all the performance measures.

# OBJECTIVE
The objective of brain tumor classification is to accurately predict the type of tumor. This classification is essential for developing personalized treatment plans. Different types of brain tumors respond differently to treatment, and an accurate classification helps medical professionals tailor treatment plans to each patient’s unique needs. Additionally, early detection through accurate classification can lead to higher treatment success rates and improved patient outcomes. Brain tumors can be accurately classified, aiding doctors in choosing the best course of treatment, such as surgery, radiation therapy, or chemotherapy. Furthermore, research efforts aim to address challenges related to variations in tumor location, shape, and size, ultimately improving the accuracy of brain tumor classification.

# METHODOLOGY
Our proposed methodology based on the DNN learning architecture for classification where the classifier is identifying the brain tumors in brain MRIs. The proposed methodology for classifying the brain tumors in brain MRIs is as follows: 

Step 1: Brain MRIs Dataset acquisition
Step 2: Convert into Grayscale
Step 3: Denoise using Gaussian Filter
Step 4: Creating Augmented Image
Step 5: Classification using VGG16
Step 6: Evaluation 

# 1.	Data Acquisition 
According to the World Health Organization (WHO) classification system to identify brain tumors, there are more than 120 types of brain tumors which differ in origin, location, size characteristics of the tumor tissues[15,16]. In this paper we were concerning with three types of malignant tumors which are:
a)	Glioma: A primary malignant brain tumors that are classified as Grade IV and developed from star-shaped cells, called astrocytes that support nerve cells. It usually starts in the cerebrum.
b)	Meningioma: Meningioma tumors arise from the meninges, the protective membranes surrounding the brain and spinal cord..
c)	Pituitary: A pituitary tumor is an abnormal growth or mass that develops in the pituitary gland, a small gland located at the base of the brain..
d)	No tumor: Normal brain mri.

![image](https://github.com/remona19/brain-tumor-classification/assets/147992703/6c4b89e2-5826-4ebc-897a-69415a02584a)
(a)

![image](https://github.com/remona19/brain-tumor-classification/assets/147992703/bc73bfc3-4464-46bc-9c22-610bdb3aa77d)
(b)

![image](https://github.com/remona19/brain-tumor-classification/assets/147992703/f3d98a0c-c7c1-419e-ad18-e9014e02bbb5)
(c)

![image](https://github.com/remona19/brain-tumor-classification/assets/147992703/ddbcec31-d12a-449f-bb9b-6c9bf0d5d9a0)
(d)

   
The dataset consists of 3000 training data and 1500 testing data of real human brain MRIs with normal and abnormal images which are glioblastoma, pituitary, meningioma tumors and no tumor collected from Kaggle. All the brain MRIs was in axial plane, T2-weighted and 256 x 256 pixel. A sample of the dataset is illustrated in the above figure.

# 2.	Grayscale
In a brain tumor dataset, "grayscale" typically refers to medical imaging data, such as MRI or CT scans, where the images are represented in shades of gray to highlight differences in tissue density. A brief description of the grayscale images in the dataset.Grayscale images in a brain tumor dataset depict the internal structures of the brain in varying shades of gray, with lighter shades representing areas of higher density and darker shades indicating lower density. These images provide detailed information about the size, location, and characteristics of the tumor, as well as its relationship to surrounding brain tissue. Researchers and healthcare professionals use grayscale images to visualize and analyze the tumor's features, aiding in diagnosis, treatment planning, and monitoring of the patient's condition over time.


# 3.	Denoising using Gaussian Filter
A filter is defined by its kernel. When we apply a filter to an image, the result is the convolution between the kernel and the original image. The kernel of a Gaussian filter is a 2d Gaussian function. When such a kernel is convolved with an image, it creates a blurring effect. This is because each pixel is now assigned with a weighted sum of itself and its neighbouring pixels. Any discontinuities in the neighbourhood are thereby averaged out. Denoising brain tumor dataset using a Gaussian filter is a common technique to remove noise and enhance the quality of medical images, such as MRI scans. adjust the kernel size and sigma value based on the characteristics of your brain tumor images and the level of noise present in the data. Additionally, always validate the effectiveness of the denoising process through visual inspection and quantitative analysis before proceeding with further analysis or interpretation of the data.
 
# 4.	Augmented Images
Data augmentation is a popular technique which helps improve generalization capabilities of deep neural networks, and can be perceived as implicit regularization. It plays a pivotal role in scenarios in which the amount of high-quality ground-truth data is limited, and acquiring new examples is costly and time-consuming. This is a very common problem in medical image analysis, especially tumor delineation. e verify which data augmentation approaches were exploited and what was their impact on the abilities of underlying supervised learners. Finally, we highlight the most promising research directions to follow in order to synthesize high-quality artificial brain-tumor examples which can boost the generalization abilities of deep models.

# 5.	Classification
After the features are extracted and selected, the classification step using VGG-16 is performed on the resulted feature vector. Classification is performed by using VGG-16 for training and testing. VGG16 is a deep convolutional neural network model used for image classification tasks. The network is composed of 16 layers of artificial neurons, which each work to process image information incrementally and improve the accuracy of its predictions.
Instead of having a large number of hyper-parameters, VGG16 uses convolution layers with a 3x3 filter and a stride 1 that are in the same padding and maxpool layer of 2x2 filter of stride 2. It follows this arrangement of convolution and max pool layers consistently throughout the whole architecture. In the end it has two fully connected layers, followed by a softmax for output. In VGG16, ‘VGG’ refers to the Visual Geometry Group of the University of Oxford, while the ‘16’ refers to the network’s 16 layers that have weights. This network is a pretty large network, and it has about 138 million parameters.
Image enhancement boosts network performance by purposely creating more training data from original data. The input image of the VGG 16 Network had a size of 224. Thus, the training dataset was used to resize our data and make it more suitable for the process of classification. It is a procedure that is used throughout DL to aid in the creation of samples. It also optimizes the network’s efficiency for a relatively small dataset. The images were altered to add variance to account for the dataset’s small size. As a result, image extensions were used to increase the variability within our constrained dataset by collecting Keras Image Data Generator when training. 


