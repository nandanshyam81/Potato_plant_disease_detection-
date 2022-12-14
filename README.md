**Plant disease detection**

Agriculture is the largest source of livelihoods in India. More than 70% of its rural households primarily depend on agriculture. So, identification of the plant disease is important in order to prevent from major losses. It is a very tedious task to identify plant diseases manually as it requires tremendous amount of effort, many labour and majorly a lot of time. So, I made a model using CNN with the help of tensorflow and keras.Model will be trained on certain amount of data and then will be tested.

> The images have been loaded in batches , it is done so because if we load all images at a time, the training speed of model will become very less as we are using a lot of memory in CPU which becomes very inefficient.

> The entire dataset has been divided into three parts namely train dataset, test dataset and validation dataset.Training data is the set of the data on which the actual training takes place.Validation split helps to improve the model performance by fine-tuning the model after each epoch and the test set informs us about the final accuracy of the model after completing the training phase.

> Input data pipeline (tf.data) pipleline was used. The concept behind tf.data piple is ETL (Extract, Transform and Load)

> One feature of tf.data API that personally fascinates me is the prefetch functionality. What it does is, during model execution(forward and backward propagation),it drives the CPU to prepare the next batch of our dataset to be fed into our model immediately after traning on the previous batch.This allows us to fully utilize our hardware and rescue our GPU from data stravtion.

> Image preprocessing was performed where the images were resized and rescaled.

> Data augmentation technique was used which is the process of artificially increasing the amount of data by generating new data points from points from existing data.Usually deep learning models require very huge amounts of data, practically collecting that huge amounts of data is very complex as it consumes lot of time and money.So, data augmentation has been done by random flip and random rotation.

![image](https://user-images.githubusercontent.com/109072424/207683040-24f409d5-89a5-41a3-b831-458ef6d7f05a.png)

> The convolutional layers are the initial layers to pull out features from the image.It maintains the relationship between pixels by learning features using a small input data sequence.It is a mathematical term that takes two inputs, an image matrix and a kernel or filter.Kernel is a filter that is used to extractt the features from the images.

> ReLU is used in the CNN model over the other activation functions because it improves the neural networks by speeding up training.Also, the computation step of a ReLU is easy as all negative elements are set to 0.0 and no exponentials,no  multiplication or division operations are involved.

> The pooling layer is another building block of a CNN and plays a vital role in pre-processing an image. In the pre-process,the image size shrinks by redcuing the size of the image.When the picture is shrunk, the pixel density is also reduced, the downscaled image is obtained from the previous layers.

> The final layer of the CNN model was the output layer where Softmax activation function was used. It was used over the other famous functions like Sigmoid function because Sigmoid function is more useful when we are doing only binary classification. As more than two classes were involved softmax function was used, which gives output as a probability value i.e. between 0 and 1. The highest value indicates the output would be from the particular neuron through which we can tell which class it belongs.


