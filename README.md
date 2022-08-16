# Under-the-Hood-
Submission for Task 4 for Programming Club IITK secretary recruitments.

LOGISTIC NEURAL NETWORK WITH SINGLE HIDDEN LAYER

- This code can classify data into two categories [0 or 1] based on training data. 
  It can take variable no. of inputs for each test case and have variable hidden layer size.
- Python 3.10 and numpy library has been used.
- One can use their own dataset by replacing the hardcoded datasets given in the code.

APPROACH:
1. First we define the neural network's structure i.e the number of input units, hidden units etc.
2. Then we initialize the model's parameters i.e the weights(random values) and biases(0).
3. In the final loop that does the calculation we:
   1. Implement forward propogation:
   	  The weights are dotted to each parameter of one input test case and the bias then added to it and then a actiavtion function applied to it at each level.
	    The tanh() actiavtion function used between the input and the hidden layer normalizes the values between [-1,1] (this function has been used here because 
	    it works better than the sigmoid function. The sigmoid function has been used between the hidden layer and the output because it normalizes the output between    
      [0,1] and we require a binary output.
   2. Compute Loss:
    	The obtained value is compared to the actual output value and the loss/cost function evaluated (cross entropy used here)
   3. Update parameters (gradient descent)
    	As we have to minimize the cost we use multivariable calculus to build differential equations between each weight, bias and the cost.
      We then update the weights and biases by gradient descent by hardcoding a learning rate.
	    Then the loop goes onto the next iteration.
4. The final outputs of forward propogation represent our predictions which are then rounded off to either 0 or 1 (based on >=0.5)
   which we can then compare to the actual outputs.
