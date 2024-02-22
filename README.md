# EVA V2 - Session 5 - Assignment - Modular Github Code
## First Neural Network for MNIST with CNN, FFN and maxpool blockx

## Modular Code
- Divide the code into 3 main files
    - model.py: *This file holds the model related details*
    - utils.py: *This file holds the utility functions that might be commonly required*
    - S5.ipynb: *Main Notebook file that has the variables, configuration parameters and actual calls

### S5.ipynb
- This is the main notebook file that is used for training the model and checking the outputs
- It also displays the Accuracy and loss curves for training and test across the epochs
- It utilizes the model.py and utils.py as mentioned below for doing the work
- You can run this file directly in Colab using Run all
- ***Recommended to use a GPU for running this file***
- ***2024-02: No need to install anything as per the current Colab verion***

### model.py
- Contains the Model definition

### utils.py
- Planned to put utils like common functions to be used
- Contains the train and test functions and GetCorrectPredCount and drawLossAccuracyPlots
- train
    - Model training method to do forward and backward pass
    - Also to calculate the accuracy
    - Return the loss and accuracy
- test
    - Model validation method to do inference
    - Also to calculate the accuracy
    - Return the loss and accuracy
- GetCorrectPredCount: Gives the count of correct preditions
- drawLossAccuracyPlots: Draws the curves for training and test accuracy and losses

#### Model definition
| Layer (type) | Output Shape | Param # |
|-------|----------|---------------|
| Conv2d-1 | [-1, 32, 26, 26] |     320  |
| Conv2d-2 | [-1, 64, 24, 24] |  18,496  |
| Conv2d-3 | [-1, 128, 10, 10]|   73,856 |
| Conv2d-4 | [-1, 256, 8, 8]  |295,168   |
| Linear-5 |         [-1, 50] | 204,850  |
| Linear-6 |         [-1, 10] |     510  |

<details>
<summary>Params</summary>
  
  - Total params: 593,200
  - Trainable params: 593,200
  - Non-trainable params: 0
</details>

<details>
<summary>Size</summary>
  
  - Input size (MB): 0.00
  - Forward/backward pass size (MB): 0.67
  - Params size (MB): 2.26
  - Estimated Total Size (MB): 2.94
</details>

Any forms of contribution and suggestion are very welcomed!

# News🔥

2024/02/24 - Model outputs
The optimum number of epochs as per this are 1, 3 and 7. To be chosen based on the accuracy and infrastructure cost parameters

![image](https://github.com/ChintanShahDS/S5/assets/94432132/1dc14fd7-1135-42dd-8360-eebe31d322a3)


<details>
  <summary> More update logs. </summary>
2024/02/20 - Code modularized and ran in Colab

2024/02/22 - Checkin to Github and README.md created
</details>

# Features
