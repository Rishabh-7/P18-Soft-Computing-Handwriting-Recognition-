# P18 Soft Computing Project (Handwriting Recognition)

# Requirements

* Python 3.5 +
* Scikit-Learn (latest version)
* Numpy (+ mkl for Windows)
* Matplotlib

# Usage

**1.** Download the four MNIST dataset files from this link:

```
http://yann.lecun.com/exdb/mnist/
```

**2.** Unzip and place the files in the dataset folder inside the MNIST_Dataset_Loader folder under each ML Algorithm folder i.e :

```
KNN
|_ MNIST_Dataset_Loader
   |_ dataset
      |_ train-images-idx3-ubyte
      |_ train-labels-idx1-ubyte
      |_ t10k-images-idx3-ubyte
      |_ t10k-labels-idx1-ubyte
```

Do this for SVM and RFC folders and you should be good to go.

**3.** To run the code, navigate to one of the directories for which you want to run the code using command prompt:

```
cd 1. K Nearest Neighbors/
```

and then run the file "knn.py" as follows:

```
python knn.py
```

or 

```
python3 knn.py
```

This will run the code and all the print statements will be logged into the "summary.log" file.

**NOTE: If you want to see the output to print on the Command prompt, just comment out line 16, 17, 18, 106 and 107 and hence you will get all the prints on the screen.**

Alternatively, you can also use PyCharm to run the code and run the ".py" file in there.

Repeat the steps for SVM and RFC code.

**4.** To run the CNN code, you don't need to provide in the MNIST dataset as it'll be downloaded automatically.

Just run the file as :

```
python CNN_MNIST.py
```

or

```
python3 CNN_MNIST.py
```

and it should run fine. 

**5.** If you want to save the CNN model weights after training, run the code with the following arguments:

```
python CNN_MNIST.py --save_model 1 --save_weights cnn_weights.hdf5
```

or 

```
python3 CNN_MNIST.py --save_model 1 --save_weights cnn_weights.hdf5
```

and it should save the model weights in the same directory.

**6.** To load the saved model weights and avoid the training time again, use the following command:

```
python CNN_MNIST.py --load_model 1 --save_weights cnn_weights.hdf5
```

or

```
python3 CNN_MNIST.py --load_model 1 --save_weights cnn_weights.hdf5
```

and it should load the model and show the Outputs.

## Accuracy using Machine Learning Algorithms:

i)	 K Nearest Neighbors: 96.67%

ii)	 SVM:	97.91%

iii) Random Forest Classifier:	96.82%


## Accuracy using Deep Neural Networks:

i)	Three Layer Convolutional Neural Network using Tensorflow:	99.70%

ii)	Three Layer Convolutional Neural Network using Keras and Theano: 98.75%


Anurag’s, Simran’s and Rishabh’s  analysis on different models: 
 

1. Larger  image size in case of Simran’s and Rishabh’s model makes the image shaper and easier to classify.
2. Simran’s and Rishabh’s model has better hyperparameters, i.e more no. of hidden layers and more no. of neurons in each layer.
3. Better choice of activation function (ReLU and Swish) for hidden layers makes the gradient descent function converge faster and thus makes training of larger sized neural network feasible. 
4. Softmax function performs better than the sigmoid layer in the output layer because the sum of probabilities outputted by the output layer units is 1 incase of softmax. Hence, for multiclass classification(i.e when no. of output classes are more than 2) Softmax activation function is preferred over Sigmoid activation function.

```    
