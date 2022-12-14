**Plant disease detection**

Agriculture is the largest source of livelihoods in India. More than 70% of its rural households primarily depend on agriculture. So, identification of the plant disease is important in order to prevent from major losses. It is a very tedious task to identify plant diseases manually as it requires tremendous amount of effort, many labour and majorly a lot of time. So, I made a model using CNN with the help of tensorflow and keras.Model will be trained on certain amount of data and then will be tested.

> The images have been loaded in batches , it is done so because if we load all images at a time, the training speed of model will become very less as we are using a lot of memory in CPU which becomes very inefficient.

> The entire dataset has been divided into three parts namely train dataset, test dataset and validation dataset.Training data is the set of the data on which the actual training takes place.Validation split helps to improve the model performance by fine-tuning the model after each epoch and the test set informs us about the final accuracy of the model after completing the training phase.

> Input data pipeline (tf.data) pipleline was used. The concept behind tf.data piple is ETL (Extract, Transform and Load)
![2](https://user-images.githubusercontent.com/109072424/207678639-e224ba7a-921a-4f10-9c15-7eaa18c83107.jpg)


