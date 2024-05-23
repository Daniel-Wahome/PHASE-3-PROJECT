<a name="br1"></a> 

Analysis and Modeling of

Car Crash Data in Chicago

By: Daniel Wahome



<a name="br2"></a> 

INTRODUCTION

CHICAGO is the most populous city in the U.S. state of Illinois and in the Midwestern United States. With a population of

2,746,388, as of the 2020 census, it is the third-most populous city in the United States after New York City and Los Angeles.

As the seat of Cook County, the second-most populous county in the U.S., Chicago is the center of the Chicago

metropolitan area, often colloquially called "Chicagoland" and home to 9.6 million residents.


BUSSINESS UNDERSTANDING

The City of Chicago has implemented E-Crash a reporting tool for car accidents that happen within the City of Chicago, but

with all this recorded data they have not been able to make strides in minimizing accidents on the streets of Chicago city.

With the data recorded through the E-Crash system and use of machine learning principles, I can find primary contributory

causes of car accidents and recommend solutions based on interpretation of results.

This will in turn help keep the citizens of Chicago safe through preventative measures therefore reduced car crashes, help

in implementation of city planning principles to reduces the crashes and limit the amount of resources the City of Chicago

utilises to solve these cases



OBJECTIVE:

Build a classifier to predict the primary contributory cause of a car accident, given information about the car, the people in

the car, the road conditions and other various factors included in the data set



<a name="br3"></a> 

◦ **DATA UNDERSTANDING**

◦ The data source is the Traffic Crashes - Crashes dataset form the Chicago Data Portal and this data is suited to this task as it

collected by the Chicago Police Department officers who are skilled about law enforcement and also that the citizens can

contest the content of the data recorded and amendments made upon confirmation

◦ The data collected contains multiple characteristics like: speed limit, weather conditions, lighting conditions, crash type among

many other characterizes that help paint a picture of how the car crash occurred. this data is suitable for our project as it

provides comprehensive and relevant information needed to predict the primary contributory cause of car accidents, which

aligns with our business objective to improve traffic safety.


◦ **TARGET VARIABLE**

◦ MOST\_SEVERE\_INJURY: This seems to be the target variable.

◦ It likely describes the most severe injury sustained in the crash.

The data set has 48 columns namely: ['CRASH\_DATE', 'POSTED\_SPEED\_LIMIT', 'TRAFFIC\_CONTROL\_DEVICE',

'DEVICE\_CONDITION', 'WEATHER\_CONDITION', 'LIGHTING\_CONDITION’, 'FIRST\_CRASH\_TYPE', 'TRAFFICWAY\_TYPE',

'LANE\_CNT', 'ALIGNMENT’, 'ROADWAY\_SURFACE\_COND', 'ROAD\_DEFECT', 'REPORT\_TYPE',

'CRASH\_TYPE','INTERSECTION\_RELATED\_I', 'NOT\_RIGHT\_OF\_WAY\_I', 'HIT\_AND\_RUN\_I’,'DAMAGE',

'PRIM\_CONTRIBUTORY\_CAUSE', 'SEC\_CONTRIBUTORY\_CAUSE','STREET\_NAME', 'NUM\_UNITS', 'MOST\_SEVERE\_INJURY',

'INJURIES\_TOTAL','INJURIES\_FATAL', 'INJURIES\_INCAPACITATING','INJURIES\_NON\_INCAPACITATING',

'INJURIES\_REPORTED\_NOT\_EVIDENT','INJURIES\_NO\_INDICATION', 'INJURIES\_UNKNOWN', 'CRASH\_HOUR',

'CRASH\_DAY\_OF\_WEEK', 'CRASH\_MONTH’

The data set has 835407 entries



<a name="br4"></a> 

◦ DATA CLEANING

◦ Various methods were used to do data cleaning

◦ Unnecessary columns were dropped

◦ Change if data types to for proper analysis

◦ Missing values and duplicates handled appropriately and data visualized


EDA

Through EDA this is what I was able to find

it seems that there might be a cause for most accidents to average around 11

pm on the 4th day of the week in July which also happens to be around

The 4th of July celebrations,

we can also see that the most of the injuries are non-fatal

this shows that most accidents happen: during the day with

clear weather, with traffic signals present, the roads are in

good condition and dry accidents happen due to the driver

hitting a fixed object and ending up with minimal injury but

the car needing to be towed most damage ends up being at

1500 usd most accidents happen at cicero drive,

a mainstream, bustling and liberal part of chicago home

to large latinx community



<a name="br5"></a> 

◦ VISUALIZATION OF DISTRIBUTIONS



<a name="br6"></a> 

◦ univariate, bivariate and multivariate anaylsis was done, after eda was complete here are the summary of findings

◦ TIME Patterns: Most accidents occur during the day, especially between 6 AM and 6 PM. Additionally, crashes predominantly

happen from Monday to Saturday, with March to October witnessing the highest frequency of accidents.

◦ Weather and Road Conditions: Clear weather conditions contribute to the majority of accidents, followed closely by rainy

weather. The roads are typically in good condition and dry at the time of the crash.

◦ Location and Traffic Control: The majority of accidents occur in mainstream areas like Cicero Drive, where traffic signals are

present. However, crashes also happen in locations with no traffic controls, indicating potential non-compliance with traffic

regulations.

◦ Primary Contributory Causes: Primary contributory causes for accidents are often undetermined, followed by failure to yield the

right of way and careless driving.

◦ Severity of Injuries: The most common type of injury reported is no indication of injury, indicating that many accidents result in

minor damage. Fatal injuries are less common, with most crashes resulting in non-incapacitating injuries.

◦ Time of Day and Crash Types: Accidents occurring during the day are more likely to involve rear-end collisions and pedestrians,

while nighttime accidents have a similar distribution of fatalities. Hit-and-run scenarios are more prevalent in fatal crashes.

◦ Seasonal Trends: There appears to be a spike in accidents around July, coinciding with the 4th of July celebrations. Despite the

increase in accidents, most injuries during this time are non-fatal.

◦ Overall, the data suggests that most accidents in Chicago occur during daylight hours, under clear weather conditions, at

locations with traffic signals. While many accidents result in minimal damage, there is a notable spike in crashes around July,

potentially due to holiday celebrations. Understanding these patterns can aid in the development of targeted interventions to

reduce the frequency and severity of accidents in the city.



<a name="br7"></a> 

◦ **MODELLING**

◦ PREPROCESS ANE NCODING WERE DONE HERE ARE THE RESULTS FROM MODELLING

THE FIRST REGRESSION MODEL OVERFITTED WHEN IT CAME TO ACCURACY WITH 100% ACCURACY AND HAD A VALIDATION

SCORE OF 72%

THE SECOND CONFUSION MATRIX GAVE A BETTER PREDICTION WHEN IT COMES TO MORE NON FATAL CRASHES

HAPENNING AT 85% BUT NOT ON HOW TO GREATLY REDUCE FATAL ONES AT 74% OVERALL

THE THIRD REGRESSION MODEL TARGETING THE RLSHP BETWEEN CRASH TYPE AND WEATHER CONDITIONS THE ACCURACY

WAS REALLY LOW AT 29% THEREFOR NOT MUCH COULD BE PREDICTED FROM IT

THE FOURTH MODEL A DECION TREE TARGETING THE RLSHP BETWEEN CRASH TYPE AND WEATHER CONDITIONS, THIS ONE

WAS BALE TO GIVE US BETTER RESULTS SHOWING THAT THE PREDCTION FOR THE CRASH TYPE IS VERY ACCURATE AND

HIGH AT 96%

THE MODEL THAT PRODUCED CONSISTENT RESULTS WAS THE CONFUSION MATRIX AND THE DECISION TREE, I PRESUME

LOGISTIC REGRESSIOON WASN'T BEST FIT BECAUSE IT IS BEST SUITED FOR BINARY CATEWGORIES

BETWEEN THE CONFUSION MATRIX GAVE A MORE ACCURATE DEPICTION OF THE RELATIONSHIP BETWEEN THE TARGET

AND FEATURE VARIABLES



<a name="br8"></a> 

**TO CH ICAG O POLICE DEPARTMENT**

Most of the accidents that the city of chicago experiences do not lead to fatal accidents, actually most of them the citizens are ok

or with minor injuries

The intensity of injury is greatly affected by a lot of factors like

Timerelated (sunday and monday tend to have the least accidents)

Accidents occurring during the day are more likely to involve rear-end collisions

and pedestrians, while nighttime accidents have a similar distribution of fatalities.

Hit-and-run scenarios are more prevalent in fatal crashes

Weather related- most crashes happen when the weather is clear and rainy

Location based - most accidents happen on cicero drive having the highest count

Cause - most are identified to undetermined which closely related to the unharmed passangers in the injury category

Season- there is an identifiable crash on the 4th of july maybe infuence by 4th of july celebration



<a name="br9"></a> 

◦ **LIMITATIONS**

◦ ABSENCE OF CROSS VALIDATION AND REGULARIZING CLASS IMBALANCE

◦ ABSENCE OF FEATURE ENGINEERING THOUGH THE DATA HELD GRANULAR DATA

◦ NOT BINNING MY VARIABLES FOR FURTHER ANALYSIS

◦ **CONCLUSION**

◦ Through our detailed analysis and modeling of car crash data in Chicago, we've uncovered important insights into what

contributes to accidents. By acting on these findings with targeted interventions, we can significantly cut down on the number

and severity of car crashes. This means safer roads, fewer injuries, and a reduction in the financial burden that accidents place on

our community. Ultimately, these steps will make Chicago a safer place for everyone.

