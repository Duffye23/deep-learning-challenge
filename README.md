# deep-learning-challenge

# Overview
The challenfe this time around is to determine whether companies applying for funding. The requirement was to create a Neural Network to work on the prediction. Like the previosu challenge, the data was standardized, and split into test and training data. This time though the model used was Neural Network.</br>

# Results
Any of the categorical data was converted to numeric with the help of the get_dummies() package so that it could be fed into our neural network. In this way, the categorical data was both dropped and considered with the model. The variable to target was the "IS_SUCCESSFUL" column of our data, which signified if a request for funding was approved or not. This was the only one we targeted as it is the single variable that was a byproduct of the other columns. It was dependent on the other features. This then means that the rest of the table was used as features to determine the result of the "IS_SUCCESSFUL" column. 

For the neural network, I decided to start off with 4 layers: 
![image](https://github.com/Duffye23/deep-learning-challenge/assets/58863493/f5d05878-e6d5-4e43-bdba-8896d720d7f7)
![image](https://github.com/Duffye23/deep-learning-challenge/assets/58863493/5d97bda3-5278-40dc-9320-eea30e5a93d5)
![image](https://github.com/Duffye23/deep-learning-challenge/assets/58863493/8862aed0-3048-481e-9fa6-88e78928ea05)</br>

I decided to start with 65 neurons as I had 43 features and wanted to have at least 1 neuron per feature. This did not lead to the target accuracy of 75% unfortunately but was far off at 72.8%.

For the first optimization, I decided to up the number of neurons to 86, double the number of features. The logic being that more neurons would help with the processing. Unfortunately this led to a slight dip in performance, at 72.7%
![image](https://github.com/Duffye23/deep-learning-challenge/assets/58863493/0c835c42-9d44-42b8-a6bb-dd571b6d01cf)</br>

The second optimization included the same double of neurons as well as an additional hidden layer, for more processing power again.
![image](https://github.com/Duffye23/deep-learning-challenge/assets/58863493/bf3a750f-4806-496b-a539-64b1d08f37da)</br>
Unfortunately, the model again was less accurate then its predecessor, this time coming in at 72.7%, slightly less if you push the decimal.
![image](https://github.com/Duffye23/deep-learning-challenge/assets/58863493/9e9c373e-bfbb-4135-b415-2e37d477c736)

For a final optimization, I decided to increase the number of epochs from 100 to 150, checking to see if more time training would help sharpen the model.
![image](https://github.com/Duffye23/deep-learning-challenge/assets/58863493/77ca9358-a4f7-410f-9e2b-a5d26a4576ea)</br>
![image](https://github.com/Duffye23/deep-learning-challenge/assets/58863493/d0d6333f-0cb9-4602-8e74-05ff88fde4cf)</br>

The model did imporve this time, past the original benchmark, but was once again short of the 75% goal at 73%
![image](https://github.com/Duffye23/deep-learning-challenge/assets/58863493/ac0fb849-896d-47a4-af37-aeaa84f42c87)</br>

# Summary
The model that I built never hit the goal of 75% accuracy. I think removing some features may help the model hone in a better prediction, or giving the model more horsepower and giving it a lot more layers and neurons. This however would require more processing power and would consume a lot more time which may not be feasible. If I could rerun this with a different model, I would towards a logistic regression model as the challenge is to predict a 0 or 1 for the target label, and the LRM (logistic Regression Model) would be better equipped to bin the label more accurately as it is more specifically built for this type of work.</br>

Sources:
Carleton Bootcamp Zoom recordings and lesson plan activities.









