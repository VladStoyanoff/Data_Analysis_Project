# Data_Analysis_Project

## Ask
### Guiding questions
● What is the problem you are trying to solve?  

The amount of annual memberships is too low  

● How can your insights drive business decisions?  

By reaching a data-driven decision that directly impacts the aforementioned prolem, the company can increase it's annual members  

_Deliverable: A clear statement of the business task_

**How do annual members and casual riders use Cyclistic bikes differently?**  

## Prepare   
### Guiding questions  

● Where is your data located?  

The data is located at a [database](https://divvy-tripdata.s3.amazonaws.com/index.html) provided by Motivate International Inc. 

● How is the data organized?  

The data is organized sequentially by date order    

● Are there issues with bias or credibility in this data? Does your data ROCCC(reliable, original, comprehensive, current, and cited)?  

I am assuming there are no credibility or bias issues with the data, due to it being directly recommneded by Google. The data seems reliable due to it's organized internal structure, original due to the actual existance of the company Divvy, comprehensive due to it's neat and understandable internal structure, current due to the data being ordered sequentially from years 2004-2020, it is not cited because it's internal rather than external data   

● How are you addressing licensing, privacy, security, and accessibility - The data has been made available by
Motivate International Inc. [under this license](https://www.divvybikes.com/data-license-agreement)   

● How did you verify the data’s integrity?  

● How does it help you answer your question?  

The dataset is helpful for answering the question because to be able to reach a data-driven decision I would need to know ---  

● Are there any problems with the data?  

---  

● Determine the credibility of the data.  

I assume that the data is credible due to it being recommended by Google and provided by Motivate International Inc. 

_Deliverable: A description of all data sources used  

The data used can be found in the data folder in this repository  

## Process  

### Guiding questions  

● What tools are you choosing and why?  

I'm choosing to prepare and analyze the data with RStudio, because BigQuery, Google Spreadsheets and Excel cannot load half of the data files due to their size.  

● What steps have you taken to ensure that your data is clean?  

My whole cleaning process is described in the script.R file step-by-step.

● How can you verify that your data is clean and ready to analyze?

By inspecting it with common functions:

colnames             #List of column names  
nrow                 #How many rows are in data frame?  
dim                  #Dimensions of the data frame?  
head                 #See the first 6 rows of data frame.  Also tail  
str                  #See list of columns and data types (numeric, character, etc)  
summary              #Statistical summary of data. Mainly for numerics  


● Have you documented your cleaning process so you can review and share those results?  

Yes. It's documented as comments in the script file.  

_Deliverable: Documentation of any cleaning or manipulation of data_  


## Analyze  

### Guiding questions  
● How should you organize your data to perform analysis on it?

All the data tables should be merged into one big data frame and any incosistent data across the tables reformed so that it matches the most recent dataset which is Q1 2020.

● Has your data been properly formatted?

Yes. The steps taken can be seen in the script.

● What surprises did you discover in the data?

I was surprised by the average duration of trip sorted by type of customers.   

● What trends or relationships did you find in the data?

Trend Number 1: The number of rides for the annual members throughout the whole year is higher 

The visuals to support this trend:

![num_of_rides_v](https://github.com/VladStoyanoff/Data_Analysis_Project/blob/main/Screenshots/num_of_rides_v.png)

Trend Number 2: The average duration of trip time in seconds for casual members is higher

The visuals to support this trend:

![avg_trip_time_v](https://github.com/VladStoyanoff/Data_Analysis_Project/blob/main/Screenshots/avg_trip_time_v.png)

Key tasks

_Deliverable: A summary of your analysis_
