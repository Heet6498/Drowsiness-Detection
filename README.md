# Drowsiness-Detection

### Executive Summary
- Driving a vehicle or a motor when sleepy is known as drowsy driving and can influence anyone
behind the wheel. Drowsy driving increases the risk of accidents considerably, leading to a disturbing
number of casualties and fatalities every year.
- While statistics on driver drowsiness is not accurate, research shows it is disruptively common.
- Sleep at America Poll 2005 of the National Sleep Foundation found that 60% of adult drivers have been
driving during the drowsiness of the past year. CDC survey data showed that in the past month, one in
25 adults had fallen asleep behind the wheel.
- With these problems in mind, our group has decided to create a classification algorithm which
will detect sleepy or closed eye. The project requires a hardware which can be any camera installed in
the motor vehicle. This camera will be zooming in, focusing on the driver’s eyes. If the driver has sleepy
or closed eye for more than 5 seconds, the second hardware which is an alarm will ring, alerting the
user.

### Data

- The first step of all the deep learning or machine learning model is to collect and clean data and
to link it with dependent variables.
- I found multiple datasets with 10000 plus images for closed and open eyes. But for the feasibility
of the available machine, I have decided to take 80 percent of the data from the dataset that I
found on Kaggle.
- The dataset was uploaded by Prasad Patil on Kaggle. I have taken 7500 images for closed and
open images respectively.
- This a binary classification model. There are two classes or labels which are open eyes and
closed eyes.

### Approach:
- After taking the data, the next step was to determine the model on which the data can be
trained and used to make predictions.
- At the beginning, I decided to create my own Keras layer model, but this model had a lower
prediction rate.
- “MobileNets are small, low-latency, low-power models parameterized to meet the resource
constraints of a variety of use cases. They can be built upon for classification, detection, embeddings, and
segmentation.”
- I played around with a bunch of different layers and pretrained model. The model which gave
me the best prediction was the Pre-trained MobileNet model. This helped me to build light weight deep
learning model whilst giving out better results.

### Model Prediction

-  For checking the accuracy of the model, I used two methods.
1) First of all, I decided to use tensorfows built-in function called “model.predict”. It gave the
accuracy to be 76%. This gave out better prediction on unseen data, so I decided to select
this as my final word.
2) The second method was to use the model on unseen data. After training the model, I ran
26 unseen open and closed eye images on the model. The images were taken randomly
from google.The model predicted accurately on 23 images out of 26 images.

### Local Web app
The next step was to deploy the web app. I decided to deploy it locally which means I created a gui and connected it with a model using an API. 
I created the local web app using Flask.



