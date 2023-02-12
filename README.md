# Terry Stops Traffic
Data science end of phase 3 project - Moringa school


## Overview
Terry Stops are stops made by police officers on the basis of reasonable suspicion. The perceived race of the subject can be a factor in police officers' decision to stop and frisk a person. It is important to note, however, that race should not be used as the sole reason for a Terry Stop, as this could be discriminatory and violate a person's constitutional rights.

The investigative detention doctrine first announced in Terry v. Ohio and amplified over the past fifty years has been much analyzed, praised, and criticized from a number of perspectives. 

The use of perceived race in Terry Stops has been a source of contention, sparking debate about racial profiling and the possibility of racial bias in policing. It is critical for law enforcement agencies to train their officers to make stops based on reasonable suspicion rather than solely on a warrant.

The workbook will be set up using the CRISP-DM data science process framework as layed out below:

![the process](https://user-images.githubusercontent.com/115970348/217210012-25f65237-d691-46ab-9516-d2f80d119a87.png)


## 1. Business Understanding

The business understanding of the problem is to create a predictive model that will assist law enforcement agencies in making informed decisions during Terry Stops. The classifier can help officers determine the likelihood of an arrest by using information about various factors such as the presence of weapons, the time of day of the call, and the gender and race of both the officer and the subject. This can improve the efficiency and fairness of law enforcement actions, potentially reducing the number of false arrests and incidents of police misconduct.

However, the use of gender and race data raises significant ethical concerns, as these factors can be used to perpetuate bias and discrimination. As a result, it is critical to approach this problem.

## 2. Data Understanding

This data represents records of police reported stops under Terry v. Ohio, 392 U.S. 1 (1968). Each row represents a unique stop.
Data provided by City of Seattle and Dataset Owner spd2internetData
There are 54.9K rows and 23 Columns.

[source link](http://www.seattle.gov/police)

This data represents records of police reported stops under Terry v. Ohio, 392 U.S. 1 (1968).Each row represents a unique stop.
Each record contains perceived demographics of the subject, as reported by the officer making the stop and officer demographics as reported to the Seattle Police Department, for employment purposes.
Where available, data elements from the associated Computer Aided Dispatch (CAD) event (e.g. Call Type, Initial Call Type, Final Call Type) are included.

### Featues
* Subject Age Group - Subject Age Group (10 year increments) as reported by the officer.
* Subject ID - Key, generated daily, identifying unique subjects in the dataset using a character to character match of first name and last name. "Null" values indicate an "anonymous" or "unidentified" subject. Subjects of a Terry Stop are not required to present identification.
* GO / SC Num - General Offense or Street Check number, relating the Terry Stop to the parent report. This field may have a one to many relationship in the data.
* Terry Stop ID - Key identifying unique Terry Stop reports.
* Stop Resolution - Resolution of the stop as reported by the officer.
* Weapon Type - Type of weapon, if any, identified during a search or frisk of the subject. Indicates "None" if no weapons was found.
* Officer ID - Key identifying unique officers in the dataset.
* Officer YOB - Year of birth, as reported by the officer.
* Officer Gender - Gender of the officer, as reported by the officer.
* Officer Race - Race of the officer, as reported by the officer.
* Subject Perceived Race - Perceived race of the subject, as reported by the officer.
* Subject Perceived Gender - Perceived gender of the subject, as reported by the officer.
* Reported Date - Date the report was filed in the Records Management System (RMS). Not necessarily the date the stop occurred but generally within 1 day.
* Reported Time - Time the stop was reported in the Records Management System (RMS). Not the time the stop occurred but generally within 10 hours.
* Initial Call Type - Initial classification of the call as assigned by 911.
* Final Call Type - Final classification of the call as assigned by the primary officer closing the event.
* Call Type - How the call was received by the communication center.
* Officer Squad - Functional squad assignment (not budget) of the officer as reported by the Data Analytics Platform (DAP).
* Arrest Flag - Indicator of whether a "physical arrest" was made, of the subject, during the Terry Stop. Does not necessarily reflect a report of an arrest in the Records Management System (RMS).
* Frisk Flag - Indicator of whether a "frisk" was conducted, by the officer, of the subject, during the Terry Stop.
* Precinct - Precinct of the address associated with the underlying Computer Aided Dispatch (CAD) event. Not necessarily where the Terry Stop occurred.
* Sector - Sector of the address associated with the underlying Computer Aided Dispatch (CAD) event. Not necessarily where the Terry Stop occurred.
* Beat - Beat of the address associated with the underlying Computer Aided Dispatch (CAD) event. Not necessarily where the Terry Stop occurred.


### Objectives
To create a classifier that can predict the outcome of a Terry Stop (whether or not an arrest was made) based on various factors such as the presence of weapons, the time of day of the call, and possibly the gender and race of both the officer and the subject. 

### Project Plan
 1.Data Preparation - Loading Libraries - Loading data - Descriptive Exploration - Data Cleaning - Exploratory Descriptive Analysis (EDA) - Pre-processing Data

 2.Modelling - Train test split - Models- Evaluation

 3.Conclusion

 4.Recommendation


## Modelling
Logistic Regression - baseline
Random Forest Classifier
Suport Vector Machine

## Evaluation
recall
f1 score
precision
accuracy

## Conclsion
In conclusion, the results of this project indicate that machine learning models can be effectively used to analyze Terry stop data to determine resolution arrests. The model has successfully identified the most important features for making predictions, which can provide valuable insights for policymakers and law enforcement agencies. However, it's important to keep in mind that this is just one part of the overall analysis and further investigation may be required to gain a more comprehensive understanding of the data.


## Repository Guide
##### CSV Files:

The raw data files which obtained by DataDriven can be found ;

[public source](http://www.seattle.gov/police)

##### Notebook:

github repo

##### Presentation
[Non-technical](https://www.canva.com/design/DAFXfhgl6m8/Iub4k4xCMvJpaY10pTTnUg/edit?utm_content=DAFXfhgl6m8&utm_campaign=designshare&utm_medium=link2&utm_source=sharebutton)

Presentation can be found from here in .pdf format ;

##### Data Report
[google docs](https://docs.google.com/document/d/122T2lqs0ynaAP4yY1iK_dvZzpJIRp1AzstU48Gdjy_Q/edit?usp=sharing)
canva


