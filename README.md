# FBRef-scrape-analysis
A first attempt at a project in building a model to predict the number of points a team will get in a 38 game professional football season. The data was obtained from FBRef using the pandas.read_html() method.

The following is a link to the article that shows how to web-scrape data from FBRef in this way and transform the data so that it is usable for analysis.

https://levelup.gitconnected.com/quickly-and-easily-scrape-fbref-using-just-pandas-773b294f86a0

The aim was to ascertain the variables that most impact the number of points that an elite level team will obtain in a single season in the Premier League, La Liga, and Serie A. Moreover, the aim was to build a model that will predict the number of points that a team will obtain in a season. A random forest regressor was used as it is easily trained has fewer underlying assumptions than some other models. Moreover, the importance of given variables can be measured with a radnom forest regressor using the feature_importances_ method in RandomForestRegressor from sklearn. The data obtained from the 22/23 season made up the test data whilst the data from 19-22 made up the training data. Earlier data could not be used as it was lacking certain key statistics such as expected goals or expected assists. 

The methods used in this project had some shortcomings. One being that to predict the number of points a team will get in a season, data from that season is required. In this case, the teams number of points will be known. The feature importance therefore matters more from this analysis. Furthermore, using points as opposed to points per match limits the amount of data that can be used to leagues where the same number of games are played. This meant excluding data from elite leagues such as the Bundesliga, Ligue 1, and the Eredivisie.

The key takeaways from this analysis are finding out what controllable variables impact the number of points a team will obtain. Prediction of points becomes difficult withouot simulating how a team may perform based on previous data. This involves predicting on non-real data giving highly unreliable results.
