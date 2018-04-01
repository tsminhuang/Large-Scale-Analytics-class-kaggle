# Movie Rating Predictor

## Setup

1. Install Anaconda3 and using the following command to install scipy

    ```
    conda install scipy
    
    ```

2. Using the jupyter notebook to run the ipython notebook code

## Implementation

There are several methods such as collaborator filter; the content-based method can be used in rating predictor. However, there are some issues we need to take into consideration.

Both training and testing set is tiny. The training data may not reflect the distribution of testing set.

1. Matrix factorization: 

    In this assignment, I choose state-of-art matrix factorization to predict missing user rating. 

2. Biases correction:

    The original matrix factorization method tried to factorize the rating matrix to two components: 
    1. user factor 
    2. item factor
    
    However, this approach does not consider user behavior and item information. 
    For example, some critical users may rating movie than average, and some movies may have the better quality than average. Hence, we can also introduce biases correction: global mean rating bias, user bias, and item bias to incorporate the user and item interactions in the model.

3. Nonnegative constrain: 
    
    Although, there are several ways to solve this matrix factorization problem such as stochastic gradient descent, or alternating least squares. However, it is intuition give the assumption that user factor and item factor should be positive. In this assignment, I used Broyden–Fletcher–Goldfarb–Shanno (BFGS) solver in scipy to solve the matrix factorization cost function.
