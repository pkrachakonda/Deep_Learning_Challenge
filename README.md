# Deep_Learning_Challenge

### Objctive:
 Objective of this of challenge is to developed to develop a nerual networl model 


# Results
- Data Preprocessing:
  - The target variable to determine the effectiveness of the funds disbursed is "IS_SUCCESSFUL". This variable reflects whether the financial aid has been utilized efficiently or not.
  - The following variables are classified as feature variables: APPLICATION_TYPE, AFFILIATION, CLASSIFICATION, USE_CASE, ORGANIZATION, STATUS, INCOME_AMT, SPECIAL_CONSIDERATIONS, and ASK_AMT.
  - EIN and NAME were removed because they are neither targets nor features.
 
- Compiling, Training, and Evaluating the Model:
  - According to [`AlphabetSoupCharity.ipynb`](https://github.com/lakigit/deep-learning-challenge/blob/main/Starter_Code/AlphabetSoupCharity.ipynb)
    - The number of input features is directly proportional to the length of X_train. The model architecture comprises two hidden layers with 80 and 30 neurons, respectively. The rectified linear unit (ReLU) activation function is employed for both hidden layers, while the sigmoid activation function is used for the output layer.
![image](https://github.com/lakigit/deep-learning-challenge/assets/138610916/034b0566-39f2-4a26-ac00-76a27e469365)
    - Evaluate the model using the test data
      
      `268/268 - 0s - loss: 0.5553 - accuracy: 0.7245 - 466ms/epoch - 2ms/step`\
      `Loss: 0.5552864670753479, Accuracy: 0.7245481014251709`

      1. **Epochs and Timing**:
        - It looks like the training process involves 268 epochs.
        - The training time for each epoch is 466 milliseconds, and the time taken for each step (or batch) is 2 milliseconds.

      2. **Model Performance**:
        - The loss after training is 0.5553.
        - The accuracy achieved on the dataset is 72.45%.
      
      3. **Conclusion**:
        - The model's accuracy is approximately 72.45%, suggesting that it correctly predicted the target outcome for about 72.45% of the instances in the dataset.
        - The loss value (0.5553) is a measure of how well the model is performing, with lower values indicating better performance. This loss value is used to optimize the model during training.
     
  - As per the analysis presented in the [`AlphabetSoupCharity_Optimisation.ipynb`](https://github.com/lakigit/deep-learning-challenge/blob/main/Starter_Code/AlphabetSoupCharity_Optimisation.ipynb) file, the objective is to optimize the model in order to achieve an accuracy rate exceeding 75%.
      - **Attempt 01: Add More Neurons to Hidden Layers**\
        The deep learning model comprises two hidden layers, with 100 and 90 neurons, respectively. The activation function employed in both these layers is "rectified linear unit" (ReLU), whereas the output layer uses the "sigmoid" activation function.
![image](https://github.com/lakigit/deep-learning-challenge/assets/138610916/8ab4bf94-06ec-43f5-b0af-b5f4566f737a)

        `268/268 - 1s - loss: 0.5607 - accuracy: 0.7243 - 781ms/epoch - 3ms/step`\
        `Loss: 0.5606803894042969, Accuracy: 0.7243148684501648`

        Notwithstanding, the incorporation of the aforementioned technique does not significantly enhance the precision of the model.

      - **Attempt 02: Add More Hidden Layers**\
        In this step, a neural network model is constructed, consisting of three hidden layers. Each layer contains 100, 50, and 20 neurons, respectively. The activation functions employed in these layers are "relu," "tanh," and "sigmoid," respectively, while the output layer employs the "sigmoid" activation function. This model is designed to optimize the neural network's performance in terms of accuracy and efficiency.\
![image](https://github.com/lakigit/deep-learning-challenge/assets/138610916/cb3016a3-6949-4722-9ce3-c8d3f7183ffa)

        `268/268 - 1s - loss: 0.5590 - accuracy: 0.7256 - 738ms/epoch - 3ms/step`\
        `Loss: 0.5589935779571533, Accuracy: 0.7255976796150208`

        There is no significant difference in accuracy in this case.

    - **Attempt 03: Changing Binning**\
      In this section, an attempt was made to increase the number of bins. Specifically, additional bins were added for both "APPLICATION_TYPE" and "CLASSIFICATION". Furthermore, the model was augmented by adding three hidden layers, each of which contained 30, 80, and 100 neurons, respectively. Additionally, the activations for these layers were "relu", "tanh", and "sigmoid".\
![image](https://github.com/lakigit/deep-learning-challenge/assets/138610916/8071ecef-310e-4c04-9729-59d2e42ef32b)

        `268/268 - 1s - loss: 0.5632 - accuracy: 0.7261 - 714ms/epoch - 3ms/step`\
        `Loss: 0.5631876587867737, Accuracy: 0.726064145565033`

        While there is only a marginal improvement in the accuracy of the final model, it is still superior compared to the other models.  
