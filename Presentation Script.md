# Wine_Not Script

## Aeden Ghebreselassie

When we started this project, we figured Wine Not jump right into data about wine! We wanted to answer the question: can a wine be predicted as red or white based off properties or characteristics of the wine, such as sugars and sulfates? There are two popular ideas within the wine world that we wanted to check in our data. The first is that red wines have higher sulfate levels than white wines. The second idea is that white wines have more residual sugar than red wines. We also wanted to find out if there were any other correlations we could notice within the data.

It was difficult to find data on wine characteristics. Wine producers do not want to give away any information about how they make their wines and the chemical qualities that make their wines unique. Because of this, we settled on two datasets easily found on Kaggle that featured wine from the Vinho Verde region of Portugal. I say two datasets because they were originally separated into red wines and white wines with 13 columns of wine properties in each. We were able to combine the data into 1 dataset using our SQL database.

When we looked at the dataset, we noticed that there were many more white wines than reds. This makes sense when you understand the wine region. In the Vinho Verde region, mostly white wines are produced. Some sources even say that it makes up 85% of the wine production. The climate makes it difficult for red grapes to ripen, and even the whites are harvested young, hence the name Vinho Verde or “green” grapes.

Today, you will hear about our machine learning model which predicts whether the wines are red or white based on their properties which become our independent variables. We will then show you the data visually to make it easy to understand. And finally, we will give you some future applications of this dataset. I will now hand it over to Daryl to start us off with the machine learning model.


## Daryl Davison

Thanks Aeden. Machine learning seems like a confusing topic, but I’m going to give you just an overview. We utilized a process called supervised logistic regression. The name and how the process works doesn’t necessarily matter to you, but the reason will. We were able to take this model and predict whether a wine will be red or white based on the 13 wine characteristics that my colleague Aeden mentioned were considered independent variables. Using all the characteristics, our model was 98.6% accurate, meaning that it was incredibly accurate at predicting the color of the wine. If we were to take the same 13 characteristics from a completely new wine and input them into our model, it would have almost a 99% chance of predicting the wine color correctly.

In addition, we wanted to find out if all 13 wine characteristics were necessary to keep a high level of accuracy in the prediction. To do this, we did some trial and error and found that we could reduce the number of variables to 4 and still have 90% accuracy. These four variables were volatile acidity, free sulfur dioxide, total sulfur dioxide, and sulphates. If we were able to get more information about many, many different wines, this would be important because it would allow our model to be run quickly and still maintain a high level of accuracy in the prediction.

In addition to the model’s prediction, we produced this heat map which shows the relationship between each of the different wine characteristics. The darker the blue color, the greater the relationship in a positive direction. For example, you can see in the top row that wine type is positively related to volatile acidity. This means that red wines tend to have a higher volatile acidity than white wines. In contrast, the closer the color is to white, the greater the relationship in a negative direction. For example, in the second to last row toward the middle, we see that alcohol is negatively related to density. This means that as the alcohol increases, the density of the wine decreases. Marcus will talk next in more detail about the relationships between the variables and show you some visualizations that highlight specific wine characteristics, in addition to showing a few that give you the option of selecting which relationships you want to see when we give you the link to the site after this presentation.


## Marcus Gillis

Our original two questions were whether red wines had more sulphates than white wines and if white wines had more residual sugar than red wines. We were able to use a program called Tableau to graph our wines and showcase their characteristics in relation to each wine type. You may notice that this graphic seems to have the same number of white wine data points as red. As mentioned earlier, in our original dataset, and in the region of Vinho Verde in general, there are a lot more white wines than red wines. To produce clearer visualizations, we created a random sample of white wines to mirror the number of red wines we had.

This first graph shows the sulphates along the bottom and the number of wines that have each sulphate level as the height of the point. The color of the point indicates the color of the wine. You can tell that the red wines do tend to have higher sulphate levels than the white wines, though not all the time. This was confirmed in the heat map Daryl showed you with a slightly positive relationship.

This next graph shows the residual sugar level along the bottom and the number of wines that have each residual sugar level as the height of the point. The white wines seem to have the higher residual sugar levels than the red wines. This was also confirmed in the heat map with a slightly negative relationship.

We also have other graphs that can be manipulated to see the relationships between the two variables. If you are interested, we can provide this link so you can see any relationships you want after this presentation. I’ll show you one now as an example of the possibilities. If we go to the first tab at the top which says “Alcohol” and click on it and then filter on the right to show “Residual Sugar,” you can see the points on this graph representing each individual wine with their respective alcohol and residual sugar levels. You can see there are many with low residual sugar levels and lower alcohol levels which both make sense since Vinho Verde grapes are harvested young. They don’t have a chance to ripen longer and produce higher alcohol or sugar levels.

If you have any questions on how to get the most information out of these graphs, please let us know and we can show you after the presentation. I will now pass it to my colleague Hallie to talk a bit about the future possibilities or applications of this dataset.



## Hallie Powell

Each wine region, and even vineyard, in the world gives characteristics to the wines that are very different. We would love to find more information and expand to other regions to confirm that our predictions, and the wine assumptions about sulphate and residual sugar levels, are accurate. However, it is very difficult to find this information. We were not even able to scrape data from different wine websites because they were blocked.

One idea we had was to create a website to find more information about the wines by encouraging winemakers to input the chemical makeup of their wines anonymously to keep their proprietary information confidential but allow them to help the wine world by providing the data.

There is also a potential future use by expanding to include prices of wines. We could see if there is a correlation between certain chemical characteristics of the wines and the price at which they sell. This comes with its own set of problems. Wine distributors do not like to let anyone except those in their direct sales circles know how much the wines cost at wholesale prices. There is a significant markup from the wholesale price to the price paid for a bottle of wine and an even greater markup when purchased at a restaurant. We would need to keep this information confidential, if we could gain access to it.

It would also be interesting to create a flavor profile machine learning model to predict wine type based on taste. Just like a master sommelier can taste a wine and know the year, region, and grape, we could create a dataset based on tastes and other influencing factors and predict the same way the sommelier does.

All of these ideas would require more data than is currently available, but if we could find data or compile it, the possibilities are vast and fascinating.


## Lara Kuzmanoff

This is where you come in. We have these great ideas, but we need your help. We would like to ask you for funding to create an app to help people choose their next favorite wine. 

Have you ever felt lost when choosing a wine to drink? Have you ever thought you liked a wine but couldn’t put your finger on what you liked about it? Our app would allow a user to input the wine they’re drinking into their profile and rate whether they liked or didn’t like it. The app looks at the characteristics of the wines in their profile and the user can then ask the app to give suggestions of new wines to try based on the wines they’ve already liked.

The possibilities are endless. If we were able compile information about the tastes, prices, and chemical characteristics of a variety of wines, we could give a user even more options and information. It would be enticing for wineries and distributors to give us the information,
because the app could advertise for their wines. It would give more people a chance to try wines they have never heard of before. The wine world would benefit greatly from this.

We hope you have enjoyed our presentation and would love to talk to you more in the future about our partnership on this app. Please let us know if you have any questions at this time.
