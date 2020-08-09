https://docs.google.com/presentation/d/1bM5py4octPuK3XWkf6qRXiPPPMVDfFheMMgmXNxk3J0/edit?usp=sharing




## Problem Statment: 

A. Problem Statement: With a nationwide overdose death toll reaching 2,846,305 In 2018, the rise in opioid overdoses have led experts to label this crisis an epidemic formally. Data maintained by the CDC and other nonprofit organizations have made it easier to analyze how different areas of the United States are being affected by this crisis, and how they may be affected in the future.  With the use of Gradient Boosting Tree models utilizing decision trees with the tf. Estimator API; I hope to accurately predict an overdose death rate based on several variables such as State, Race, Gender, and whether there was an increase in cases from the year prior. I will use existing data from 1999- 2016 as a training set and existing data from 2017 as my testing data. With these sources, I will be able to see how accurate my algorithm is at predicting the overdose rates in the United States, as well as predict the demographics of our population most at risk.

## B. Method: 

I began this undertaking by adopting parts of the Boosted Tree models and the tf.estimators  portion of a different model to make the predictions I hoped to ascertain accurately.

![Capture_Final](https://github.com/Acejv21/Ace_Code/blob/master/Capture_Final.PNG?raw=true)

Once my models was coded correctly, I was able to import my discrete data set from the CDC database. This data set contained 7722 rows and 18 columns.With in this data set there was information regaurding Race, Gender, State ,Census Regions, Population, Deaths, and  statistical information. Next, I cleaned the data set using wrangling methods that utilized for loops to scrub and extract the particulars of the data I was interested in analyzing. 

![Capture_Final_2.](https://github.com/Acejv21/Ace_Code/blob/master/Capture_Final_2.PNG?raw=true)

This section proved the most difficult, as the CDC data was incomplete and required a lot of cleaning and restructuring. I managed to get the data set to the point where I could begin to perform descriptive analytics, but not quite to the point where I could make predictions.  

##  Data Sources:

Data Sources: CDC: https://wonder.cdc.gov/controller/datarequest/  https://www.cdc.gov/drugoverdose/maps/rxrate-maps.html HCUP: https://www.hcup-us.ahrq.gov/db/nation/nis/nisdbdocumentation.jsp HHS: https://healthdata.ov/ Data World: https://data.world/datasets/opioids Opioid & Health Indicators Database: https://opioid.amfar.org/

## C. 

The Gradient Boosting Tree models did work very well for accomplishing the desired outcome as other data scientists who had the opportunity to maximize their data for such models returned impressive results. I do think that based on how my code was set up, I would have had some slight overfitting when making predictions by race because I had limited amounts of training data at the time of running my model.

![Figure_1_FP.png](https://github.com/Acejv21/Ace_Code/blob/master/Figure_1_FP.png?raw=true)

The above histogram is a result that demonstrates there are 5,496 occurrences of cases that resulted in as many as 500 deaths in a census region.  
 
## D.

Finally, I will explain what can be accomplished when the data-set was properly scrubbed and implemented into the model. Other data scientists were able to demonstrate prediction maps that showed where the most likely suffer high overdoses that end in death within the United States

![Capture.PNG](https://github.com/Acejv21/Ace_Code/blob/master/Capture.PNG?raw=true)

They were also able to answer my original question, “Who might be at a higher risk?” For example, they were able to analyze whether Men or Women were more affected by the epidemic.

![sex%20graph.PNG](https://github.com/Acejv21/Ace_Code/blob/master/sex%20graph.PNG?raw=true)

After seeing the success of their Data Scientist’s models, I am eager to continue to work on mine until I achieve even more accurate models than the models I have seen on the CDC website. After seeing the success of their Data Scientist’s models, I am eager to continue to work on mine until I achieve even more accurate models than the models I have seen on the CDC website. This summer has been a real eye-opener as to what we can achieve with data science.
