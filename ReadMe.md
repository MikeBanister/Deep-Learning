Overview of the analysis: Explain the purpose of this analysis.

Results: Using bulleted lists and images to support your answers, address the following questions:

    Data Preprocessing
        *   The target variable is a simple yes or no whether the project was successful contained in the column 
            IS_SUCCESSFUL
        *   Features are:
            APPLICATION_TYPE        
            AFFILIATION
            CLASSIFICATION
            USE_CASE
            ORGANIZATION
            STATUS
            INCOME_AMT
            SPECIAL_CONSIDERATIONS
            ASK_AMT
        *   Two variables were removed.
            EIN
            NAME
    Compiling, Training, and Evaluating the Model
        *   The neural net was attempted with varying layers neuron counts and activtion functions.
        *   Model success was measured using the accuracy quotient. 
        *   Attempts were made, essentially at random, to combine 1 to 5 layers using 1 to 30 'neurons' and activation functions 'relu', 'tanh' and 'sigmoid'. The intent was to home in on any patterns and produce a more accurate model. In practice this proved unsuccessful as there was no material improvement from ~73% accuracy in any combination making it difficult to divine a pattern.
        *   An optimization attempt was made using keras_tuner was attempted however between the large number of parameters and increasingly lengthy epochs, it quickly became infeasible to properly test via brute force combinations.
Summary: 
    *   Overall the deep learning model was roughly 73% accurate meaning other methods may be substantially more effective.
    *   A rigourous examination of the data, likely including principal component analysis would likely yeild better results or perhaps reveal a more focused optimization strategy.
    *   Determining pricipal components would likely assist in pruning the original dataset to focus on the more consequential features. 
