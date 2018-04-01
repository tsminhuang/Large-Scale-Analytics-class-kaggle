# Salary prediction using linear regression

## Setup

1. Install Anaconda3 and using the following command to install Keras 

    ```
    # CPU version
    conda install -c anaconda keras
    
    # GPU version
    conda install -c anaconda keras-gpu
    ```

2. Using jupyter notebook to run the ipython notebook code

## Implementation

1. Feature selection: 

    Select all columns features except id and salary. 
    
    Using one hot encoding to expand all features.
2. Feature scaling:
    
    Since the selected features are the categorical type, there is no need to do feature scaling.
    However, I scaled the prediction target **salary**. 
    
3. Some features may be redundant or useless such as department code and department name could be redundant. I choose using Lasso (L1 penalty) to get the sparse solution.

4. I used scikit-learn Lasso with $\lambda = 0.001 $, the same value as in Keras implementation. 
