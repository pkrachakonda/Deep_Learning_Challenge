# Deep_Learning_Challenge

## Objective:
 Objective of this of challenge is to develop a binary classified neural network model, which could be used in optimisation of financial risks.

## Datasets
Charity datasets provided as part of challenge.

## Model
A Sequential tensorflow binary classified neural model is used for this challenge.

# Results
 ### [Model Version 01](https://github.com/pkrachakonda/Deep_Learning_Challenge/blob/main/AlphabetSoupCharity_Version_01.ipynb)

- Data Preprocessing:
  - As per instruction both, EIN and NAME were removed because they are neither targets nor features.
  - The target/label variable used in the analysis is *"IS_SUCCESSFUL"*, a variable used to reflect whether the financial aid has been utilized efficiently or not.
  - Remaining variables of datasets are classified as feature variables: APPLICATION_TYPE, AFFILIATION, CLASSIFICATION, USE_CASE, ORGANIZATION, STATUS, INCOME_AMT, SPECIAL_CONSIDERATIONS, and ASK_AMT. 
 
- Compiling, Training, and Evaluating the Model:
    - Around 80 and 30 neurons are used for First and Second layers and a single neuron for output layer ([Model Version 01](https://github.com/pkrachakonda/Deep_Learning_Challenge/blob/main/AlphabetSoupCharity_Version_01.ipynb)) .
       
       ![Model 01 Summary](https://github.com/pkrachakonda/Deep_Learning_Challenge/assets/20739237/7cedfed2-66b5-4491-99d5-094282dde881)

    - The rectified linear unit (ReLU) activation function is employed for both hidden layers, while the sigmoid activation function is used for the output layer.
    - Probabilistic loss function  *binary_crossentropy* and *adamax* optimizer was used.

    - Evaluate the model using the test data
      1. **Epochs and Timing**:
        - It looks like the training process involves 100 epochs.
        - The training time for each epoch is 340 milliseconds, and the time taken for each step (or batch) is 1 milliseconds.

      2. **Model Performance**:
        - The loss after training is 0.5545.
        - The accuracy achieved on the dataset is 72.85%.
     
          ![image](https://github.com/pkrachakonda/Deep_Learning_Challenge/assets/20739237/a19a2b71-96c7-4bed-80a1-76bac60c77d2)

 - **Conclusion**:
        - The model's accuracy is approximately 72.85%, suggesting that it correctly predicted the target outcome for about 72.85% of the instances in the dataset.
        - The loss value (0.5545) is a measure of how well the model is performing, with lower values indicating better performance. This loss value is used to optimize the model during training.

## Optimisation
  - In order to achieved an accuracy of 75%, an attempts were made.

  - **Attempt 01: Add More Hidden Layers**\
      [Model Version 02](https://github.com/pkrachakonda/Deep_Learning_Challenge/blob/main/AlphabetSoupCharity_Version_02.ipynb)

     As part of this step hidden layer numbers were increased from two to four and *tanh* was selected as activation function. 

    ![image](https://github.com/pkrachakonda/Deep_Learning_Challenge/assets/20739237/99c302bd-4bb8-4128-9edb-a8bac9ec3b2a)

      Model Summary:

      ![image](https://github.com/pkrachakonda/Deep_Learning_Challenge/assets/20739237/d20ae561-2abe-4754-843f-750cac67ed36)

      However, accuracy has remained same, indicating that addition of deep layers does not effect the accuracy.
   
      ![image](https://github.com/pkrachakonda/Deep_Learning_Challenge/assets/20739237/6cf18dc9-cac3-48a9-9c91-f76de8becb2b)

 - **Attempt 02: Dropping Features from Analysis**\
     [Model Version 03](https://github.com/pkrachakonda/Deep_Learning_Challenge/blob/main/AlphabetSoupCharity_Version_03.ipynb)

     In this step, some of the features "STATUS", "SPECIAL_CONSIDERATIONS_Y" were dropped from the Model V02, to examine the effect of these features on accuarcy.

     ![image](https://github.com/pkrachakonda/Deep_Learning_Challenge/assets/20739237/2b0bf4f1-3751-4ec9-a7d5-a151c43f709e)


     ![image](https://github.com/pkrachakonda/Deep_Learning_Challenge/assets/20739237/b6db5c9c-30b5-41c1-a254-2e4e67f17dce)

     Model Summary:

     ![image](https://github.com/pkrachakonda/Deep_Learning_Challenge/assets/20739237/36d3d768-6cdc-4f9f-8876-2cc67f17151f)

     There is no significant difference in accuracy w.r.t. to base case.
   
     ![image](https://github.com/pkrachakonda/Deep_Learning_Challenge/assets/20739237/238ee816-f552-4049-b726-416ad30f74b0)

- **Attempt 03: Changing Binning**\
  [Model Version V04](https://github.com/pkrachakonda/Deep_Learning_Challenge/blob/main/AlphabetSoupCharity_Version_04.ipynb)
  
    In this section, an attempt was made to increase the number of bins. Specifically, additional bins were added for both "APPLICATION_TYPE" and "CLASSIFICATION" to Model version V02.\

    Model Summary:\
    ![image](https://github.com/pkrachakonda/Deep_Learning_Challenge/assets/20739237/b3450349-d8f2-4056-b060-038dd7385bde)
 
   ![image](https://github.com/pkrachakonda/Deep_Learning_Challenge/assets/20739237/9729dbbf-21dc-4c0d-b347-d80062d4242c)

  While there is only a marginal improvement in the accuracy of the final model, it is still superior compared to the other models.

  
