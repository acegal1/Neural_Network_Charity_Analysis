# Neural_Network_Charity_Analysis
Neural networks (also known as artificial neural networks, or ANN) are a set of algorithms that are modeled after the human brain. They are an advanced form of machine learning that recognizes patterns and features in input data and provides a clear quantitative output. 

The purpose of this project is to use a binary classifer a model of neural network to analyze and predict whether charity applicants will be successful if funded. Task is to develop a model that will accurately predict if the prospective organizations seeking funding are sound investments.

The following methods for the analysis will be used:

- Compare the differences between the traditional machine learning classification and regression models and the neural network models.
- Implement neural network models using TensorFlow.
- Preprocess and construct datasets for neural network models.
- Compare the differences between neural network models and deep neural networks.
- Implement deep neural network models using TensorFlow.

# Resources
TensorFlow platform (library) in Python
Jupyter Notebook
kaggle charity_data.csv which contains 34,299 organizations that have received funding from Alphabet Soup over the years.

# Results

## Data Preprocessing
1. What variable(s) are considered the target(s) for your model?
	The "IS_SUCCESSFUL" column is the target and is marked as successful if organization was successfully funded by AlphabetSoup. This variable is 	then 	considered as the target for our deep learning neural network.

2. What variable(s) are considered to be the features for your model?
	The column "IS_SUCCESSFU"L contains interger 0 or 1 with 0 refering the charity donation was not used effectively and 1 to Yes it was used 	successfully. 

3. What variable(s) are neither targets nor features, and should be removed from the input data?
	The columns "EIN" and "NAME" are identification information and can be removed from the input data to improve code efficiency.

## Compiling, Training, and Evaluating the Model
4. How many neurons, layers, and activation functions did you select for your neural network model, and why?
	This deep-learning neural network model is made of two hidden layers with 8 and 5 neurons respectively. The input data has 43 input features and 25,724 samples. The output layer is made of a unique neuron as it is a binary 	classification. To speed up the training process, we are using the activation function ReLU for the hidden layers. As our output is a binary classification, Sigmoid is used on the output layer.
	For the compilation, the optimizer is adam and the loss function is binary_crossentropy.

5. Were you able to achieve the target model performance?
	The target for the model was 75%, but first run using the Renu function for both 1 and 2 hidden layers produced accuracy of 72%. 

	![ReLu](https://github.com/acegal1/Neural_Network_Charity_Analysis/blob/main/images/renu.png)


6. What steps did you take to try and increase model performance?
	To increase the performance of the model, I applied a different activation function (tanh) which did increase the accuracy to 73%. 

	![Tanh](https://github.com/acegal1/Neural_Network_Charity_Analysis/blob/main/images/tanh.png)

	Final run increased the number of Epochs from 100 to 300 for the training regimen. Then added third hidden layer with all using the relu functions. It's recommended if your model still requires optimizations and tweaking to meet desired performance, you can increase the number of epochs, or training iterations. As the number of epochs increases, so does the amount of information provided to each neuron. By providing each neuron more information from the input data, the neurons are more likely to apply more effective weight coefficients. Still only achieved 73%. 

	![Epochs](https://github.com/acegal1/Neural_Network_Charity_Analysis/blob/main/images/epochs.png) 

# Summary
The deep learning neural network model did not reach the target of 75% accuracy and I would 75% still not be considered average in performance. At this point I thought of implementing a different machine learning model such as Random Forest Classifier to combine a multitude of decision trees to generate a classified output and evaluate its performance against our deep learning model.  