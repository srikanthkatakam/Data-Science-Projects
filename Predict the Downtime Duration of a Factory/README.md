# Predicting the Downtime Duration of a Factory

### Problem Description:

IAn electric car manufacturing company, 'Kesla', with several factories is seeing exponential growth in demand due to the sudden increase of subsidies for EVs in the country.

The car manufacturer, however, is not able to handle the demand and has tasked a team of DataScience consultants to identify potential areas to quickly increase the efficiency without operational changes.
	
The team of Data Science consultants saw that without changing any of the data that is being collected, a predictive model can be built that predicts the downtime of a factory, thereby allowing the few engineers present in the engineering team to very quickly most important factories that would cause the most significant downtime.
	
The Cheif Data Scientists have now curated a dataset, where we have several variables that it believes impact the `downtime_duration`. They have tracked three different downtime durations.
	
The three classes of ` downtime_duration `

0 - Low downtime (15 minutes to 1 hour)

1 - Downtime that lasts anywhere between 1 hour and 24 hours

2 - for long downtimes that can last from 24 hours to sometimes even several days
   
### About Data:

There are 7 CSV files provided to us, they are described below:

- `train_data.csv :` It has a unique event id for each observation of the downtime_duration in a particular factory_number

- `test_data.csv :` Similar to the train dataset, we are provided with an id and a factory_number , we are expected to predict the outage_duration for each of the records

- `assembly_line_info.csv :` For each of the event id s mentioned in the `train_data.csv` and `test_data.csv` files and also some additional id s there is a record of the assembly_line_type that is stored in the dataset. There are 10 different types of assembly lines that are observed in the dataset. There can be multiple assembly lines in a single factory, for the factory to be running all the assembly lines must be functioning.

- `issue_info.csv :` For each of the event id s mentioned in the `train_data.csv` and `test_data.csv` files and also some additional id s there is a record of the issue_type that is stored in the dataset. There are 5 different issue_type 's recorded in the dataset. These are classified as an issue by an onsite engineer.

- `log_report_type_data.csv :` For each event id there are log_report_type and volume columns are recorded. log_report_type is a type of the recorded report as reported by a technical team member who is working on the assembly line. Workers are allowed to report specific types of issues using a mobile application. volume is the volume of cars handled by the assembly line in custom company specific units.

- `car_variant_data.csv :` For each of the event id s mentioned in the `train_data.csv` and `test_data.csv` files and also some additional id s there is a record of the car_variant_type that is being put together on the assembly line.

**Evaluation Metric:**

The evaluation metric used for this hackathon would be the **F1 Macro Average**
