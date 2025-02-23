# Road accident prediction for carsharing company
## Task statement
Business needs to create a system that could assess the risk of an accident along a selected route. Risk is understood as the probability of an accident with any damage to the vehicle. As soon as the driver has booked a car, got behind the wheel and selected a route, the system should assess the risk level. If the risk level is high, the driver will see a warning and recommendations for the route. The idea of ​​creating such a system is at the stage of preliminary discussion and development. There is no clear algorithm for work and similar solutions on the market yet. **The current task is to understand whether it is possible to predict accidents based on historical data of one of the regions.**
## Project plan:
1. Uploading training data from SQL database;

2. Testing hypotheses:

2.1 The probability of a driver causing an accident depends on the type of checkpoint and the type of road - the hypothesis was confirmed, drivers of cars with manual transmission are more likely to cause accidents on ramps and highways;

2.2 The probability of a driver causing an accident depends on the combination of the car body and the condition of the road surface - the hypothesis was confirmed, coupes and minivans have the worst ratio of driver culpability relative to the total number of accidents. At the same time, the worst values ​​for these body types are achieved on road sections with bulk materials or floods.

3. Building a model for assessing the risk of an accident:

3.1 Compiling the final set of features for models;

3.2 Performing data preprocessing;

3.3 A secondary selection of features for the model based on statistical analysis;

3.4 Application of hyperparameter selection.

## Results
In order to identify the most significant factors, 3 models were built: linear regression, decision tree and random forest. Model metrics:
LinReg - precision = 0.61
RandomTree - precision = 0.62
RandomForest - precision = 0.64

## Recommendations for business

1. Optimize vehicle usage based on age
Monitoring vehicle condition: Older vehicles have an increased risk of accidents. It is recommended to tighten vehicle condition monitoring as they age, and possibly impose strict mileage and age limits on vehicles in the service.
Fleet renewal: Regularly updating the fleet based on vehicle age will reduce the risk of accidents and potential maintenance costs. It can also improve the user experience by providing new, reliable vehicles.
2. Consider the time of day when planning routes and issuing vehicles
Avoiding accident hours: Time factors, especially evening and night time, have a significant impact on the likelihood of accidents. If possible, limit service access during periods of increased accident risk (e.g. late evening and night) or warn drivers of the increased risk.
Adjust insurance rates: Set higher insurance rates for driving during accident-prone hours to compensate for the increased likelihood of accidents during these times.
3. Train and increase requirements for manual transmission drivers
Driver training: Since driving a car with a manual transmission requires more attention and skill, it is recommended to conduct additional training for drivers who prefer such cars or introduce mandatory requirements for their skill level.
Choice of cars: When possible, it is better to give priority to cars with an automatic transmission, especially for less experienced drivers, as this reduces the likelihood of accidents.
4. Road Conditions
Route selection based on road conditions and traffic management: Wet roads and roads without traffic lights or signs increase the likelihood of accidents. It is recommended to take these factors into account when choosing routes and vehicle placement zones.
Inform drivers about road conditions: Providing information about road conditions (e.g. wet roads after rain) will help drivers choose routes more consciously and drive more carefully.
5. Weather Conditions
Weather warnings: Although rain and cloud cover have not been shown to significantly affect the likelihood of accidents in the models, it is recommended to inform drivers about adverse weather conditions and remind them to exercise caution in such conditions.
Weather data monitoring: In the future, the company may consider integrating real-time weather data to more accurately predict the risk of accidents and promptly inform drivers.
6. Provide safety enhancement measures for sedans
Enhanced measures for sedans: Sedans have been shown to be more likely to be involved in accidents. It may be worth reconsidering their use, such as providing additional insurance or choosing less risky routes for them.
Specific requirements for use: In cases where sedans predominate in the fleet, consider implementing additional measures to monitor them, such as regular maintenance or restrictions on the time of use.
7. Additional safety measures
Installing monitoring equipment: Safety sensors and cameras can help collect data on road conditions, weather conditions, time of day, and driver activity, which will improve the accuracy of the model’s predictions and allow for more effective risk management.
Developing a dynamic pricing system: Increasing the rental price based on risk factors (e.g. time of day, vehicle age, weather conditions) can help offset potential losses from accidents and encourage safer driver behavior.
