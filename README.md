# Softmax-Regression-and-Handwritten-Digit-Recognition---ML
	Epoch - 30, Hidden Layers - 30, eta (Learning Rate) = 3.0
Experiment No. 	Accuracy
1.	9482/10000
2.	9493/10000
3	9511/10000

Median Performance – Accuracy = 9493/10000 = 94.93%

	Epoch - 30, Hidden Units -30, eta (Learning Rate η) = 5.0
Performance – Accuracy = 9482(Correct predictions)/10000 = 94.82%

	Epoch - 50, Hidden Units -30, eta (Learning Rate η) = 5.0
Performance – Accuracy = 9509(Correct predictions)/10000 = 95.09%

	Epoch - 50, Hidden Units -50, eta (Learning Rate η) = 5.0
Performance – Accuracy = 9603(Correct predictions)/10000 = 96.03%

	Epoch - 50, Hidden Units -100, eta (Learning Rate η) = 5.0
Performance – Accuracy = 9685(Correct predictions)/10000 = 96.85%

	Epoch - 50, Hidden Units -500, eta (Learning Rate η) = 5.0
Performance – Accuracy = 7313(Correct predictions)/10000 = 73.13%



Through the experiment, what is the best configuration? What did you learn? 
During my experimentation with different hyper-parameters, I found out the best result (highest prediction accuracy) is obtained when we train this neural network for 50 Epochs, have 100 hidden units and set the gradient descent learning rate (η) to 5.0. I made an observation that the prediction accuracy (test accuracy) or number of correct predictions out of totals number of instances in test dataset increases with increase in the complexity and number of hidden units for this particular example.
But we cannot keep on increasing the complexity of the network and expect it to perform better always. Overly complex networks may overfit on the training data and might not give better accuracy on testing dataset. I observed this result in my last experiment when I increased the number of hidden units to 500 while keeping the number of epochs and learning same as the last one and observed that instead of the training accuracy being increased, it decreased to 7313/10000.  
Another observation I made was that the learning rate (η) (3.0 or 5.0) is very high as the testing accuracy when observed during each epoch of the learning process does not keep on increasing during each passing epoch. Somewhere during the learning process the testing accuracy first increases and in the next epoch it decreases to a lower value. My understanding is that this is happening because of learning rate being very high and the model experiences overshoot somewhere in the process and this results in poor accuracy in one particular step (epoch) as compared to its previous step (epoch). However, the model still manages to converge by the end of the learning process and gives out the maximum accuracy in the final epoch, since it overshoots only once when the η is set to either 3.0 or 5.0. No overshoot is observed when we set η to 0.1 but then the model does not converge complete in 30 or 50 epochs to give out the best accuracy.     

Any idea to further improve the prediction rate? 
To further improve the prediction rate (testing accuracy) we can do one or more of the following steps – 
    
1. Add or increase the number of hidden Layers – The current network has only one hidden layer adding one or more hidden layers can help us to improve the prediction accuracy. 
2. We can change the activation function – We can change the activation function for either one layer or all layer from sigmoid to ReLU.
3. Better Weights Initialization – Here in this case we randomly initialize all the weights and as this is a complex network architecture the gradient descent algorithm might not be able to converge to globally optimal solution and may converge to some local minima solution. If we can make a good initial guess of the weights, we can improve the performance of this neural network. 
4. Gaining more training data – Obtaining more labeled and normalized data can help us train the model better and hence obtain better prediction rate (testing accuracy.)



 
