## NFL Big Data Bowl 2023: Expected Protection Time

## Deep Learning for DDI Prediction

**Project description:** Novel metric for evaluating offensive and deffensive linemen in the NFL using a gradient boosted survival model

**Details:** For the 2023 season the theme of the NFL's annual analytics competition was evaluating offensive and defensive linemen. This project aims to develop a new statistic, called Estimated Pass Time (EPT), for evaluating the performance of offensive and defensive lines in American football. The EPT metric is created using a variant of the Cox proportional hazards model, a widely used regression model in the medical field to study patient survival. In this project, the model is adapted to predict the time until the defense is able to end a pass play by sacking, hurrying, or forcing the quarterback to run. The gradient boosted Cox proportional hazards model is used to predict EPT, allowing for interactions between predictor variables, such as down and distance. The traditional pressure rate metric used in the NFL is limited, as it does not account for how long the offensive line maintained a clean pocket or other factors that can affect performance.

Data preperation for this project was very involved. Data provided by the NFL was in the form of raw player tracking data that had to be transformed until usable data for input in a modle. Ultimatley this data was used to train a variation on a Cox Proportional Hazard model that predicts whether a pass will be unpressured (0) or result in a sack or pressure (1), as well as the amount of time before the event occurs. The team and player performance were modeled separately, with features such as down, distance, time remaining, score, number of rushers, number of blockers, play action, and formation included. For team performance, two models were trained for every team in the league's offense and defense, while for player performance, a model was created for every single team. The modeling approach involved a CPH model, with parameters tuned to optimize performance. A minimum of 30 pass rush plays were required for a player to be included in the analysis. This methodology was limited to evaluating defenders as offensive linemen do not rotate regularly in the NFL.

<img src="images/PlayerEPT.png?raw=true"/>
<img src="images/TeamEPT.png?raw=true"/>
