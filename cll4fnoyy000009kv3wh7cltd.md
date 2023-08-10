---
title: "Data Alchemy: Turning Raw Information into Real Gold"
datePublished: Thu Aug 10 2023 00:40:39 GMT+0000 (Coordinated Universal Time)
cuid: cll4fnoyy000009kv3wh7cltd
slug: data-alchemy-turning-raw-information-into-real-gold
cover: https://cdn.hashnode.com/res/hashnode/image/stock/unsplash/oyXis2kALVg/upload/0028fbb00dc6a082492dd58fdb6431f9.jpeg
tags: coursera, tableau, data-analytics, google-data-analytics, data-analytics-course

---

With a sense of accomplishment, I find myself at the culmination of a fulfilling journey - one that has allowed me to navigate the intricate realm of data analytics. As the final pieces of my first-ever data analytics case study fall into place, I am filled with both excitement and a deep sense of satisfaction. This venture has been more than a mere exploration of numbers; it has been a revelation of insights and a testament to the power that data holds when subjected to meticulous examination.

Upon completing my [Google Data Analytics Course](https://www.linkedin.com/feed/update/urn:li:activity:7092504169810468864/), I found it imperative for me to put the skills I have just learned into practice by working on a project. Hence, I decided to work with the Cyclistic Case Study. Join me in reliving the moments as I reflect on the steps I took while working on my case study!

---

## Cyclistic Case Study

### About the Company

In 2016, Cyclistic launched a successful bike-sharing offering. Since then, the program has grown to a fleet of 5,824 bicycles that are geotracked and locked into a network of 692 stations across Chicago. The bikes can be unlocked from one station and returned to any other station in the system anytime -- Google Data Analytics Professional Certificate.

### Services Offered

* Single Ride Passes
    
* Full Day Passes
    
* Annual Memberships
    

### Customer Segment

1. Customers who purchase single-ride or full-day passes are referred to as ***Casual Riders***.
    
2. Customers who purchase annual memberships are ***Cyclistic Members***.
    

### Finance Analyst's Speculation

* Annual Members are much more profitable than casual riders.
    
* According to Moreno, the company's director of marketing, maximizing the number of annual members will be key to the company's future success.
    

---

## Case Study Deliverables

* A clear statement of the business task
    
* A description of all data sources used
    
* Documentation of any cleaning or manipulation of data
    
* A summary of the analysis
    
* Supporting visualizations and key findings
    
* Top 3 Recommendations based on analysis
    

---

## **Ask Phase**

| **Guiding Questions** | **Answers** |
| --- | --- |
| What is the problem I am trying to solve? | Profit maximization for Cyclistic by turning casual riders into annual members |
| How can my insights drive business decisions? | Understanding the difference between the riding patterns of Cyclistic's customer audience could potentially lead to actionable steps and drive marketing campaigns that easily convert casual riders into annual members |

### Deliverable: Concise and Clear Statement of the Business Task

<div data-node-type="callout">
<div data-node-type="callout-emoji">💡</div>
<div data-node-type="callout-text">Analyze and vary the bike usage patterns for both casual riders and annual members.</div>
</div>

---

## **Prepare Phase**

| **Guiding Questions** | **Answers** |
| --- | --- |
| Where is the data located? | The riding data has been provided by Motivate International Inc. and is stored on Amazon Web Service (AWS); a reputable cloud provider. |
| How is the data organized? | Comma Separated Files Proper naming convention followed except for the case of September 2022All data files have the same number of columns and all column names are exactly the same. All columns are of the right data types. |
| Are there issues with bias or credibility in the data? | The data being used for analysis is time-relevant as it is of the immediate past 12 months. The data is from a primary source as it was collected in real-time by the company itself using its app. There is not much information on how exactly the data were extracted. Hence, it is difficult to comment on whether there is bias in the data collection process. The percentage of missing data in each data frame is generally low, with most columns having a fraction of 0.0% indicating that the data is quite complete. However, columns like ***start\_station\_name***, ***start\_station\_id***, ***end\_station\_name***, and ***end\_station\_id*** have percentages of their missing data ranging from about 13% to 17%. The data entry format in some of the columns like ***station\_id*** is not uniform throughout. |
| How are components like licensing, privacy, security, and accessibility addressed? | The data is licensed under the Divvy company via this [link](https://www.divvybikes.com/data-license-agreement) but cannot be accessed because the server is down and hence, raises a concern. The data is open source, hence publicly accessible to anyone that might require it. Due to privacy issues, the riders' id information has been altered to protect against the possible connection between past purchases and credit card numbers. Copies of the original data files have been made for security purposes and the original files have been stored online using OneDrive. |

#### Inspecting the Data

```python
import pandas as pd

june2023 = pd.read_csv("../../cyclistic-data-folder/divvy-data/202306-divvy-tripdata.csv")
may2023 = pd.read_csv("../../cyclistic-data-folder/divvy-data/202305-divvy-tripdata.csv")
april2023 = pd.read_csv("../../cyclistic-data-folder/divvy-data/202304-divvy-tripdata.csv")
march2023 = pd.read_csv("../../cyclistic-data-folder/divvy-data/202303-divvy-tripdata.csv")
february2023 = pd.read_csv("../../cyclistic-data-folder/divvy-data/202302-divvy-tripdata.csv")
january2023 = pd.read_csv("../../cyclistic-data-folder/divvy-data/202301-divvy-tripdata.csv")
december2022 = pd.read_csv("../../cyclistic-data-folder/divvy-data/202212-divvy-tripdata.csv")
november2022 = pd.read_csv("../../cyclistic-data-folder/divvy-data/202211-divvy-tripdata.csv")
october2022 = pd.read_csv("../../cyclistic-data-folder/divvy-data/202210-divvy-tripdata.csv")
september2022 = pd.read_csv("../../cyclistic-data-folder/divvy-data/202209-divvy-publictripdata.csv")
august2022 = pd.read_csv("../../cyclistic-data-folder/divvy-data/202208-divvy-tripdata.csv")
july2022 = pd.read_csv("../../cyclistic-data-folder/divvy-data/202207-divvy-tripdata.csv")
```

#### Columns Check

This is to assert that all files have the same columns.

```python
all_dfs = [june2023, may2023, april2023, march2023, february2023, january2023, december2022, november2022, october2022, september2022, august2022, july2022]
df = all_dfs[0]
assert all([all(df.columns == df2.columns) for df2 in all_dfs])
print('All files have the same columns.')
```

```python
# checking the data types of the columns
print(june2023.dtypes)
```

### Deliverable: A description of all data sources used

<div data-node-type="callout">
<div data-node-type="callout-emoji">💡</div>
<div data-node-type="callout-text">The data sources used in this analysis consist of riding data provided by Motivate International Inc., a renowned bike-sharing services company. The data is securely stored on Amazon Web Service (AWS), a reputable and reliable cloud provider, ensuring accessibility and data integrity. The dataset is organized in comma-separated files with consistent naming conventions, except for September 2022. Each file contains the same number of columns with consistent names and appropriate data types, ensuring the data's coherence and structure. However, the analysis raises concerns about potential bias due to limited information on the data extraction process. On the positive side, the data represents the past 12 months and is collected in real-time through the company's app, bolstering its credibility and relevance. Nevertheless, the presence of missing values in the dataset may impact the accuracy of the resulting analysis. Additionally, privacy concerns have been addressed by altering riders' ID information to safeguard their identity and protect sensitive data. The data is licensed under Divvy, the bike-sharing company, and although the data is generally open-source, there are challenges related to its current accessibility due to server issues. For security purposes, copies of the original data files have been securely stored online using OneDrive.</div>
</div>

---

## **Process Phase**

#### Tools Used

*For this project, Python and Tableau have been used. Python has extensive libraries like pandas which is versatile for data manipulation. With pandas, we can do data cleaning, transformation and feature engineering. Tableau helps in producing interactive and customizable visualizations. Using both tools, we are able to fetch comprehensive insights from the data, from data analytics to engaging visual representations.*

#### Analysis Log

* Converted the started\_at and ended\_at columns to datetime for all the month dataframes
    
* Calculated ride length for each ride in all dataframes
    
* Added columns for days of the week for all dataframes
    
* Checked the missing values in the dataframes
    
* Computed the fraction of missing data points for all columns in all dataframes to assess the quality of the data
    
* Added month name columns to all dataframes
    
* Calculated distances in kilometres between the start and end stations for all dataframes using the haversine formula
    
* Renamed ride\_length column to ride\_length\_seconds and ride\_distance to ride\_distance\_km in all dataframes for easy understanding
    
* Merged all the monthly dataframes together into one dataframe (yearly\_data)
    
* Removed outliers from the yearly\_data dataframe using the IQR method
    
* Visualized all locations present in the data
    
* Verified that all locations are on land (and not in water)
    
* From the yearly\_data without outliers, removed row where the total ride length is less than zero seconds
    

#### Ensuring Data Integrity

```python
# converting started_at and ended_at to datetime for all dataframes
for dataframe in all_dfs:
    dataframe['started_at'] = pd.to_datetime(dataframe['started_at'])
    dataframe['ended_at'] = pd.to_datetime(dataframe['ended_at'])
```

```python
# calculating ride length for each ride in all the dataframes
for dataframe in all_dfs:
    dataframe['ride_length'] = dataframe['ended_at'] - dataframe['started_at']
    # converting ride length to seconds
    dataframe['ride_length'] = dataframe['ride_length'].astype('timedelta64[s]')
```

```python
# to verify our changes, we randomly select a dataframe and cross check
print(june2023.head())
```

```python
# creating a column for days of the week
for dataframe in all_dfs:
    dataframe['day_of_week'] = dataframe['started_at'].dt.day_name()
```

#### Checking for Missed Values

```python
# checking the number of missing values in each column for all dataframes
i = 0
for dataframe in all_dfs:
    print(f"Dataframe {i}")
    for column in dataframe.columns:
        print(f"{column} : {dataframe[column].isnull().sum()}, fraction: {dataframe[column].isnull().sum()/len(dataframe[column])*100}%")
    print("\n")
    i += 1
```

#### Creating a Column for Months of the Year

```python
# creating a column for month name
for dataframe in all_dfs:
    dataframe['month'] = dataframe['started_at'].dt.month_name(locale = 'English')
```

To compute the distance of each ride trip, we use the latitude and longitude of both start and end destinations with the haversine formula.

<div data-node-type="callout">
<div data-node-type="callout-emoji">💡</div>
<div data-node-type="callout-text">The Haversine Formula is a mathematical equation used to calculate the distance between two points on the surface of a sphere, such as the Earth.</div>
</div>

We can also rename some columns of the dataframes to make them more intuitive:

```python
for dataframe in all_dfs:
    dataframe.rename(columns={'ride_length': 'ride_length_seconds', 'ride_distance': 'ride_distance_km'}, inplace=True)
```

Since we have latitude and longitude, we can also try to verify that all the locations are seemingly on land and no starting or ending stations are in the ocean or in the middle of nowhere.

```python
import matplotlib.pyplot as plt
import cartopy.crs as ccrs
import cartopy.feature as creature
```

Taking the data for May 2023 as an example:

```python
fig = plt.figure(figsize=(12, 8))
ax = plt.axes(projection=ccrs.PlateCarree())

ax.coastlines()
# adding land
ax.add_feature(cfeature.LAND)
# adding ocean
ax.add_feature(cfeature.OCEAN)

ax.scatter(may2023['start_lng'], may2023['start_lat'], marker = '.', label="Start Points", color='red', transform=ccrs.PlateCarree())
ax.scatter(may2023['end_lng'], may2023['end_lat'], marker = '.', label="End Points", color='blue', transform=ccrs.PlateCarree())

plt.legend()
plt.title('Start and End Points of Trips in May 2023')
plt.show()
```

We get a plot like this:

![A scatter plot of the latitude and longitude of the stations in Chicago as contained in the May 2023 Divvy dataset.](https://cdn.hashnode.com/res/hashnode/image/upload/v1691624806259/2d58488e-01d7-4265-98ef-393360bc2389.png align="left")

#### Merging the Dataset

To further prepare our dataset, we merge all the dataframes to have one view of the entire dataset.

```python
yearly_data = pd.concat([june2023, may2023, april2023, march2023, february2023, january2023, december2022, november2022, october2022, september2022, august2022, july2022], ignore_index=True)
```

#### Outlier Detection

We check for outliers within our data using the distance column and setting a threshold of 3 \* Standard Deviation.

<div data-node-type="callout">
<div data-node-type="callout-emoji">💡</div>
<div data-node-type="callout-text">Standard deviation is a statistical measure that quantifies the amount of variation or dispersion in a set of data points. It indicates how much individual data points deviate from the mean (average) of the dataset.</div>
</div>

```python
# Removing Distance Outliers from the dataset (Setting Threshold of 3 * Standard Deviation)
threshold = yearly_data["ride_distance_km"].mean() + 3 * yearly_data["ride_distance_km"].std()
outliers = yearly_data[yearly_data["ride_distance_km"] > threshold]
print(outliers)
```

We can then check what percentage of the data is comprised of outliers:

```python
print("Percentage of data that are outliers: ", (len(outliers) / len(yearly_data)) * 100)
```

#### Extracting the Data Points without the Outliers

```python
yearly_data_without_outliers = yearly_data[yearly_data['ride_distance_km'] <= threshold]
```

#### Descriptive Analysis

```python
yearly_data_without_outliers.describe()
```

Here, we might notice that the minimum ride length in seconds is negative which is impossible. So, we clean our data by removing it.

```python
# removing the entry with a negative ride_length_seconds
yearly_data_without_outliers = yearly_data_without_outliers[yearly_data_without_outliers['ride_length_seconds'] > 0]
```

#### Visualizing for all the 12 Months

```python
# visualizing for all the 12 months.
fig = plt.figure(figsize=(12, 8))
ax = plt.axes(projection=ccrs.PlateCarree())

ax.coastlines()
# adding land
ax.add_feature(cfeature.LAND)
# adding ocean
ax.add_feature(cfeature.OCEAN)

ax.scatter(yearly_data_without_outliers['start_lng'], yearly_data_without_outliers['start_lat'], marker = '.', label="Start Points", color='red', transform=ccrs.PlateCarree())
ax.scatter(yearly_data_without_outliers['end_lng'], yearly_data_without_outliers['end_lat'], marker = '.', label="End Points", color='blue', transform=ccrs.PlateCarree())

plt.legend()
plt.title('Start and End Points of Trips in May 2023')
plt.show()
```

We get the plot below:

![All year round scatter plot of the stations in Chicago from the Divvy data.](https://cdn.hashnode.com/res/hashnode/image/upload/v1691625675005/0dabbcfa-1cd2-4154-8707-2c0c7eefdc9d.png align="left")

---

## Analyze Phase

#### Descriptive Analysis

```python
# fetching all numeric columns from the dataset
numeric_columns = yearly_data_without_outliers.select_dtypes(include=['int64','float64']).columns
yearly_data_without_outliers[numeric_columns].describe()
```

When printed, we can see that the cleaned dataset has about 5.77 million entries. Notably, the standard deviations are all relatively small, indicating consistency in the data. The mean and median values are also relatively close for all the attributes in the descriptive analysis. The shortest ride length is 1 second, which seems impossible and requires a more in-depth look. The average ride length for all rides irrespective of client type is 919.7 seconds which is about 15 minutes. The maximum ride length is 1,922,127 seconds (about 32,035 minutes (equivalent to 533 hours) or (22 days)). This does not seem right. However, there's not much information regarding the maximum time a client could use a ride. Compared to the mean, it is significantly different. Hence, this suggests that this might be a technical error in the data collection stage. With this quick summary, we can see the central tendencies, variability, and potential anomalies, which help us get a better understanding of the dataset we are working with.

#### Mode of the Week: The Day with the Highest Number of Rides

```python
mode_day_of_week = yearly_data_without_outliers['day_of_week'].mode()[0]
mode_day_of_week
```

All year round, the mode of the week is Saturday meaning that there are more rides on Saturdays as compared to other days of the week.

#### Average Ride Length for Each User Type

```python
# calculating the average ride length for members and casual riders
members = yearly_data_without_outliers[yearly_data_without_outliers['member_casual'] == 'member']
casual = yearly_data_without_outliers[yearly_data_without_outliers['member_casual'] == 'casual']

print('Average ride length for members: ', members['ride_length_seconds'].mean())
print('Average ride length for casual riders: ', casual['ride_length_seconds'].mean())
```

On average, we can see that the casual riders make use of the service more than the annual members.

#### Benchmarking the Above According to the Days of the Week

```python
# getting the mean of all days of the week
avg_ride_length_grouped = yearly_data_without_outliers.groupby(['day_of_week','member_casual'])['ride_length_seconds'].mean().reset_index()

# pivoting the avg_ride_length_grouped
pivot_avg_ride_length_grouped = avg_ride_length_grouped.pivot(index='day_of_week', columns='member_casual', values='ride_length_seconds')
print(pivot_avg_ride_length_grouped)
```

#### Inspecting the Distribution of RideType for Each User Type

```python
members_ridetype = members['rideable_type'].value_counts()
print(members_ridetype)

casual_ridetype = casual['rideable_type'].value_counts()
print(casual_ridetype)
```

From the comparison, we see that electric bike is mostly popular across the two rider groups. Annual members however do not make use of docked bikes. On another note, annual members use more of electric bikes and classic bikes compared to their casual counterparts.

#### Adding Hours of the Day and Boolean Weekend Column to the Data

```python
yearly_data_without_outliers['hour'] = yearly_data_without_outliers['started_at'].dt.strftime('%I %p')


# adding weekday or weekend column
weekend_days = ["Saturday", "Sunday"]
yearly_data_without_outliers['weekend'] = yearly_data_without_outliers['day_of_week'].apply(lambda x: 1 if x in weekend_days else 0)
print(yearly_data_without_outliers.head())
```

#### Adding Season Column

```python
def get_season(month):
    if month in ['December', 'January', 'February']:
        return 'Winter'
    elif month in ['March', 'April', 'May']:
        return 'Spring'
    elif month in ['June', 'July', 'August']:
        return 'Summer'
    else:
        return 'Fall'
    
yearly_data_without_outliers['season'] = yearly_data_without_outliers['month'].apply(get_season)
print(yearly_data_without_outliers.head())
```

#### Saving to .CSV File

```python
yearly_data_without_outliers = yearly_data_without_outliers.drop('ride_id', axis=1)
# saving to csv
yearly_data_without_outliers.to_csv('yearly_data_without_outliers.csv')
print('Data saved to csv file!')
```

### Deliverable: A Summary Report

<div data-node-type="callout">
<div data-node-type="callout-emoji">💡</div>
<div data-node-type="callout-text">The descriptive analysis of the cleaned dataset, encompassing around 5.77 million entries, underscores the dataset's coherence, as evidenced by the relatively small standard deviations across attributes. Mean and median values, presenting closeness, further attest to data consistency. A glaring outlier surfaces in the form of the shortest ride length at 1 second, warranting closer scrutiny. The overall average ride length, regardless of user type, is approximately 919.7 seconds or 15 minutes, while an anomaly emerges with a maximum ride length of 1,922,127 seconds (around 22 days). This discrepancy suggests potential data collection issues. The mode day of the week is Saturday. Notably, the average ride lengths for casual and member riders are 1228.85 seconds and 723.85 seconds, respectively. Detailed breakdowns by day of the week reveal valuable insights into ride behaviours, with Saturday being the most popular day. Moreover, categorized by ride type, electric bikes dominate both member and casual ridership, highlighting notable usage trends within the dataset.</div>
</div>

  

# Visualizations

For interactivity, the visualizations have been made on Tableau and can be accessed via this [link](https://public.tableau.com/views/CyclisticDataVisualizations_16916129852850/Sheet1?:language=en-US&:display_count=n&:origin=viz_share_link).

# Act Phase

It is noteworthy to mention that more data should be collected to further understand the user behaviour and interaction of the company's customers. Data on demographics like age, gender, and occupation would definitely lead to more insightful results. Also, trip context data like weather conditions, the purpose of the ride (commuting, leisure, exercise), and traffic and road conditions can help identify patterns that influence the rider's behaviour.

### Top 3 Recommendations:

1. **Weekend Engagement Strategy:** Given the fact that both casual riders and annual members are mostly active on Saturdays, Cyclistic can explore the possibility of offering weekend discounts to increase ridership. This can be done by offering a discount on the annual membership fee for new members who sign up on a Saturday or complete a certain number of rides on a weekend. This will help increase the number of annual members and also increase the number of rides taken by casual riders.
    
2. **Improved Service Experience for Annual Members:** The experiences of both casual riders and annual members are almost similar. To incentivize the idea of becoming an annual member, Cyclistic can try to offer exclusive services like faster access to bikes or priority docking at popular stations during peak hours.
    
3. **User Journey Analysis**: With this, Cyclistic can better understand the end-to-end experience of riders. By analyzing touchpoints from the time a rider signs up for a ride to the time they complete it, the company can identify patterns common amongst annual members and directly target casual riders with these patterns to convert them into annual members.
    

# Important Links

* [Project Link](https://github.com/alliajagbe/data-analytics/tree/master/case_study)
    
* [Visualizations on Tableau](https://public.tableau.com/views/CyclisticDataVisualizations_16916129852850/Sheet1?:language=en-US&:display_count=n&:origin=viz_share_link)
    

If you've come this far, thank you.

As I wrap up my inaugural data analytics case study, I'm reminded that every data point holds the potential to unveil a unique story. This journey has been more than just a project; it's a testament to the power of curiosity and analysis, and I'm excited to embark on new data-driven adventures, armed with insights that continue to shape the way we perceive and harness information.