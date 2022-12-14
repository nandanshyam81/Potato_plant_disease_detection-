**Plant disease detection**

Agriculture is the largest source of livelihoods in India. More than 70% of its rural households primarily depend on agriculture. So, identification of the plant disease is important in order to prevent from major losses. It is a very tedious task to identify plant diseases manually as it requires tremendous amount of effort, many labour and majorly a lot of time. So, I made a model using CNN with the help of tensorflow and keras.Model will be trained on certain amount of data and then will be tested.

> The images have been loaded in batches , it is done so because if we load all images at a time, the training speed of model will become very less as we are using a lot of memory in CPU which becomes very inefficient.

> The entire dataset has been divided into three parts namely train dataset, test dataset and validation dataset.Training data is the set of the data on which the actual training takes place.Validation split helps to improve the model performance by fine-tuning the model after each epoch and the test set informs us about the final accuracy of the model after completing the training phase.

> Input data pipeline (tf.data) pipleline was used. The concept behind tf.data piple is ETL (Extract, Transform and Load)

> One feature of tf.data API that personally fascinates me is the prefetch functionality. What it does is, during model execution(forward and backward propagation),it drives the CPU to prepare the next batch of our dataset to be fed into our model immediately after traning on the previous batch.This allows us to fully utilize our hardware and rescue our GPU from data stravtion.

> Image preprocessing was performed where the images were resized and rescaled.

> Data augmentation technique was used which is the process of artificially increasing the amount of data by generating new data points from points from existing data.Usually deep learning models require very huge amounts of data, practically collecting that huge amounts of data is very complex as it consumes lot of time and money.So, data augmentation has been done by random flip and random rotation.

![image](https://user-images.githubusercontent.com/109072424/207683040-24f409d5-89a5-41a3-b831-458ef6d7f05a.png)


