# Introduction

In this read.me file I have layed out my thinking process and methodologies when analyzing big data with R. The guiding questions and deliverables are a standart for any analysis I perform, but the methodologies sometimes differ, respectively to what programming languages and frameworks I use.

## Ask
### Guiding questions
● What is the problem I am trying to solve?  

The amount of annual memberships is too low  

● How can my insights help with data-driven decision making at the company?  

By reaching a data-driven decision that directly impacts the aforementioned prolem, the company can increase it's annual members  

_Deliverable: A clear statement of the business task_

**How do annual members and casual riders use Cyclistic bikes differently?**  

## Prepare  

### Guiding questions   

● Where is my data located?  

The data is located at a [database](https://divvy-tripdata.s3.amazonaws.com/index.html) provided by Motivate International Inc. 

● How is the data organized?  

The data is organized sequentially by date order.   

● Are there issues with bias or credibility in this data? Is the data ROCCC(reliable, original, comprehensive, current, and cited)?  

I am assuming there are no credibility or bias issues with the data, due to it being directly recommended by Google professionals inside the Google Data Analytics Professional Certificate course. The data seems reliable according to it's organized internal structure, original according to the actual existance of the company providing the data, comprehensive because of it's understandable and methodological internal structure, current according to the data being ordered sequentially from years 2004-2020, it is not cited because it's internal rather than external data.   

● How am I addressing licensing, privacy, security, and accessibility?  

The data has been made available by Motivate International Inc. [under this license](https://www.divvybikes.com/data-license-agreement)   

● How does it help you answer your question?  

The dataset holds all the information that the company is permitted to acquire from customers, so it's highly likely that what I would need is inside it. If it's not I would consult myself with the stakeholders and consider one of three options:  

1. Wait until new data is collected  
2. Create data with the available datasets  
3. Use third-party data  

● Are there any problems with the data?  

There are problems with data such as being incosistent with one another, and some calculations which I need are not inside the data (e.g number of rides taken per customer type). Those problems are taken care of in the R script.  

● Determine the credibility of the data.  

I assume that the data is credible due to it being recommended by Google Data Analytics Professional Certificate course and provided by Motivate International Inc. 

_Deliverable: A description of all data sources used  

**The data used is contained in the following zip files inside this [database](https://divvy-tripdata.s3.amazonaws.com/index.html)**  

- Divvy_Trips_2019_Q2.zip  
- Divvy_Trips_2019_Q3.zip  
- Divvy_Trips_2019_Q4.zip  
- Divvy_Trips_2020_Q1.zip  

## Process  

### Guiding questions  

● What tools am I choosing and why?  

I'm choosing to prepare and analyze the data with RStudio, because BigQuery, Google Spreadsheets and Excel cannot load half of the data files due to their size.  

● What steps have I taken to ensure that the data is clean?  

My whole cleaning process is described in the script.R file step-by-step.

● How can I verify that the data is clean and ready to analyze?

By inspecting it with common functions:

colnames             #List of column names  
nrow                 #How many rows are in data frame?  
dim                  #Dimensions of the data frame?  
head                 #See the first 6 rows of data frame.  Also tail  
str                  #See list of columns and data types (numeric, character, etc)  
summary              #Statistical summary of data. Mainly for numerics  


● Have I documented my cleaning process so that I can review and share those results?  

Yes. It's documented as comments in the script file.  

_Deliverable: Documentation of any cleaning or manipulation of data_  

**Documentation can be found insie the script file**

## Analyze  

### Guiding questions  
● How should I organize the data to perform analysis on it?

All the data tables should be merged into one big data frame and any incosistent data across the tables reformed so that it matches the most recent dataset which is Q1 2020.

● Has the data been properly formatted?

Yes. The step taken to format the data can be found on row 119,120 and 121 in the R script.

● Has any of my hypotheses about the data been contradicted?

I was surprised by the average duration of trip sorted by type of customers. In the case that my hypotheses have been contradicted I carefully examine all the steps taken again to ensure that no mistakes have been made.  

● What trends or relationships did I find in the data?  

Trend Number 1: The number of rides for the annual members throughout the whole year is higher.  

The visuals to support this trend:

![num_of_rides_v](https://github.com/VladStoyanoff/Data_Analysis_Project/blob/main/VIsuals/num_of_rides_v.png)

Trend Number 2: The average duration of trip time in seconds for casual members is higher.  

The visuals to support this trend:

![avg_trip_time_v](https://github.com/VladStoyanoff/Data_Analysis_Project/blob/main/VIsuals/avg_trip_time_v.png)

_Deliverable: A summary of my analysis_

**Annual members ride more often, but for shorter period of time. Conversely casual members ride rarer, but for longer periods of time.**

## Share   

### Guiding questions  

● Were you I able to answer the task at hand?  

Yes.  

● How do your findings relate to your original question?  

With this data, now further analysis can take place where the company can assess the decisions that must be made to increase the annual members.  

● Who is the audience which would hear those findings?  

My audience in this case, would be the stakeholders, most likely CMO or CEO of the company.  

● Can data visualization help me share the findings?  

Visualizations can help the stakeholders undestand my findings better.  

_Deliverable: Supporting visualizations and key findings through visuals and potentially a presentation_

**The visuals are shared in this read me file a couple of paragraphs above this line**

## Act  

### Guiding questions  
● What is my final conclusion based on the analysis?

The final conclusion is that annual members use the bikes more often. Additionally, the casual members don't use the bikes as often, but use them for prolonged periods of time.

● How could my team and business apply those insights?

These insights could be taken into account when deciding how to increase the annual members of the company. One way they could be applied is to give casual members a discount for the annual membership if they have more than 1 bike ride per week with longer duration time than a certain threshold that would make sense financially for the company.

● Is there additional data I could use to expand on my findings?

I belive that if we had data that showcases how often members and casual riders took bike rides, this would help us further with the business problem.

**Deliverable: My top three recommendations based on the analysis**  

1. Give casual members that have a bike ride longer than a certain threshold a discount for the annual membership;  
2. Increase the price for bike rides per minute used;  
3. Develop a ranking system In this ranked system, the winners would be monthly chosen, and they would be declared winners if they pass that threshold of bike usage per month.  
