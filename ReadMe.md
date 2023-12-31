# Deep-Learning

This analysis uses a neural network model to select applicants for funding with the best chance of success in their ventures.
The subject data set is contained in a CSV and comprises more than 34,000 organizations that have received funding from the example VC (named Alphabet Soup) over the years.

Data Preprocessing
* The target variable is a simple yes or no whether the project was successful contained in the column IS_SUCCESSFUL
* Features are:
   * APPLICATION_TYPE—Alphabet Soup application type
   * AFFILIATION—Affiliated sector of industry
   * CLASSIFICATION—Government organization classification
   * USE_CASE—Use case for funding
   * ORGANIZATION—Organization type
   * STATUS—Active status
   * INCOME_AMT—Income classification
   * SPECIAL_CONSIDERATIONS—Special considerations for application
   * ASK_AMT—Funding amount requested
   * IS_SUCCESSFUL—Was the money used effectively
* Two variables were removed.
    * EIN (id)
    * NAME

Compiling, Training, and Evaluating the Model
 * The neural net was attempted with varying layers neuron counts and activtion functions.
 * Model success was measured using the accuracy quotient. 
 * Attempts were made, essentially at random, to combine 1 to 5 layers using 1 to 30 'neurons' and activation functions 'relu', 'tanh' and 'sigmoid'. The intent was to home in on any patterns and produce a more accurate model. In practice this proved unsuccessful as there was no material improvement from ~73% accuracy in any combination making it difficult to divine a pattern.
 * An optimization attempt was made using keras_tuner was attempted however between the large number of parameters and increasingly lengthy epochs, it quickly became infeasible to properly test via brute force combinations.

Summary: 
 * Overall the deep learning model was roughly 73% accurate meaning other methods may be substantially more effective.
 * A rigourous examination of the data, likely including principal component analysis would likely yeild better results or perhaps reveal a more focused optimization strategy.
 * Determining pricipal components would likely assist in pruning the original dataset to focus on the more consequential features. 
