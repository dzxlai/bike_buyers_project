<img width="1212" alt="Screenshot at Aug 24 17-57-31" src="https://github.com/user-attachments/assets/e61145f4-694f-43e9-82e0-31bdceb48a24">


<h1> bike_buyers_project </h1>

<h2> Description </h2>
An Exploratory Data Analysis (EDA) on 'Bike Buyers' dataset using MS Excel. 
'Bike Buyers' dataset contains 1000 entries of customers from different backgrounds, and whether they <b>did</b> or <b>or did not</b> purchase a bike.

In this project, I will analyse the data by exploring through the dataset and its features, creating tables to help summarise and access quick information/highlights, then create insightful data visualisations in the form of graphs and dashboards, which will help me to identify patterns and trends.

<br />
<br />

<h2>Languages/Tools and Skills Used</h2>

- MS Excel 
- Data Cleansing (missing values, removing duplicates, find & replace), Data Standardisation, Data Filtering, Pivot Tables, Data Visualisation (Charts + Dashboard)

<br />
<br />

<h2>Data Cleansing</h2>

In this section, we focus on data cleansing. A crucial process in ensuring the quality and reliability of our dataset. By addressing issues such as missing values, duplicate entries, and inconsistencies. Proper data cleansing lays the foundation for generating meaningful insights and making informed decisions based on clean, reliable data.

![bike_buyers_dataset_original_csv_to_excel](https://github.com/user-attachments/assets/2656df00-98f1-492b-8f57-78dce2350d54)
![bike_buyers_original_row_count](https://github.com/user-attachments/assets/8bc86c1d-7941-4246-9720-38055376b159)
(1026 rows, excluding the columns/feature headers)

After uploading the <b>bike_buyers.csv</b> dataset into excel, the first step I took was to create a new sheet. I called this the 'working_sheet'.

![bike_buyers_working_sheet](https://github.com/user-attachments/assets/d789067f-e949-42a5-a567-d06b74e8bbdb)

I created a separate area for manipulating and transforming the dataset to avoid errors and protect valuable data. The original dataset is preserved as a backup for reference if needed.
<br/>

To start, I’m reviewing the number of rows and columns in the table to understand the dataset thoroughly. This helps me make informed decisions about the next steps. I’m also identifying potential categorical features for comparing groups and detecting patterns or trends.
<br/>

I compiled a list of key areas to focus on during the data cleansing process, highlighting potential common issues.
- missing/NULL values
- duplicate values
- formatting standardisation, we want entries to be all the same/similar format
- spelling errors
- whitespaces
- currencies
- dates
<br/>

<h3>Missing/NULL data</h3>

Removing missing values is crucial for ensuring data accuracy, integrity, and consistency. Clean data helps to prevent bias or inconsistent analysis. Clean data without missing values to better decision-making by providing reliable insights.

Within Excel, I am able to use the Filter tool. The filter tool allows me to quickly filter on the relevant data in my table, i.e. the columns/features.

![filter_tool](https://github.com/user-attachments/assets/854adc7c-d322-4eb5-9849-edad04f549c3)

I am able to look within column data, and the values contained within each row of each column. Values such as, text values, numerical data, dates etc.

A useful tool when it comes to cleaning data. Not only am I able to spot missing data within the columns and thus the dataset, I would also be able to look for <b>spelling errors</b> as well as <b>standardisation errors</b>.

After investigating each column and each of the unique values within the rows of each column, I was happy to see that there were no missing values!
Missing values will normally be easy to spot as they would show as <b>'NULL'</b> or <b>'(Blanks)'</b>.

I also noticed that the dataset seemed very clean in the spelling errors department as well, as I was not able to spot any, allowing me to move on to the next step of my data cleansing process.

<br/>
<br/>

<h3>Removing Duplicates</h3>

For the next step of my data cleansing steps, it was important for me to check the dataset for duplicates, with values and rows. Likewise with the necessity of removing missing data, removing duplicate data is just as essential for maintaining data accuracy and consistency. Duplicated data can distort analysis results, leading to biased or misleading insights. They can in some cases inflate dataset size unnecessarily, which can lead to increasing storage costs and processing time. 
Expelling duplicates will ensure that each data point/row is unique, thus improving the reliability and accuracy with our actionable insights.

Within Excel again, I am able to utilise a built-in tool to help me with this, 'Remove Duplicates'. This tool lets me remove duplicated rows within a column(/feature) or a set of columns.

![bike_buyers_remove_duplicates_1](https://github.com/user-attachments/assets/5b2b8367-20ec-460c-9dfe-92f2bdcb970a) 
<br/>
Notice, when applying the tool to a range with multiple columns, the tool will remove the entire row of the duplicated value.

![bike_buyers_removing_duplicates_2](https://github.com/user-attachments/assets/8a82d0f8-8d98-464b-b8df-7a80b4ad7325)
<br/>
Applying the 'Remove Duplicates' tool has allowed me to pinpoint and remove 26 duplicated values.
As a result, we are left with 1000 unique values.

<br/>
<br/>

<h3>Data value manipulation, using 'Find & Replace'</h3>

When conducting my dataset/table overview, I made sure to take note of things that may need to be changed or further inspected. One thing I noticed quickly was within a couple columns, 'Marital Status' and 'Gender'.

The issue here was the values held within each column:
- For the 'Marital Status' feature, values were either <b>M</b> to represent <b>Married</b> or <b>S</b> to represent <b>Single</b>.
- For the 'Gender' feature, values were either <b>M</b> to represent <b>Male</b> or <b>F</b> to represent <b>Female</b>.

![bike_buyers_maritalstatus_gender_1](https://github.com/user-attachments/assets/1b27e08b-8da4-478e-834d-8a9543559f20)

Instantly I was able to pick up on the fact that both feature columns are using the same value of <b>M</b> to represent two completely different things. 
I knew this would cause an issue not only in confusion, but perhaps also being troublesome when it comes to later steps of this EDA, such as with data visualisations.

In order to go around this problem, the solution is to simply manipulate the values within each column feature and ensure they identify uniquely.
For both simplicity and convenience, in this case, it is better to spell the values out, as that would read with ease.

Using CTRL h, I am able to use the 'Find & Replace' tool.

![bike_buyers_maritalstatus_gender_2](https://github.com/user-attachments/assets/79fcb93a-8551-444d-961c-06c7717c1671)

With 'Find & Replace' I am able to look up select a range to search through for specific text or number data within my worksheet, I am then able to choose what to replace those original values with.
Here I have successfully changed both columns feature values to their newly assign unique identifiers, and as a result, we are able to distinguish between the values much easier.

![bike_buyers_maritalstatus_gender_4](https://github.com/user-attachments/assets/0126b5c7-efc6-453e-b256-4b5c69866dd3)

<br/>
<br/>

<h3>Data Standardsation</h3>

Data standardisation can be important for ensuring consistency,accuracy, and reliability across datasets. 
One common feature that needs checking frequently will be able column with a numerical or date value, as these two features tend to most likely have the possibility of different curriences or formats, etc.

In the dataset our bike_buyers dataset, we have income column, filled with numerical values of the incomes of our 1000 entries. At a glance, I notice there is not much wrong with this column at all, it seems clean, and clear, and using the filter tool, I am able to confirm this.

![bike_buyers_income_1](https://github.com/user-attachments/assets/99350d10-3ac4-4fb0-bda3-995540e17146)![bike_buyers_income_2](https://github.com/user-attachments/assets/4251e130-2ad0-42ad-96c7-db867e4c8c63)

- I noticed that the column was initially formatted as 'General', when in this case as an income, it would be much more appropriate for us to have this changed into a currency format.
- I also decided to remove the decimal places in order to simplify the presentation of financial data. Removing decimal places also allows for consistency with our numerical data. This is especially useful for when we later wish to represent the data visually, using graphs and plots.

<br/>
<br/>

Continuing through the column features, I am continuing to look through for any errors or formats than need to be changed.
The next column I notice that may cause issues later, is within the commute distances.

In this column, we have values: [0-1 Miles], [1-2 Miles], [2-5 Miles], [5-10 Miles], [10+ Miles]; While the unique values initially seemed fine, I encountered a crucial issue later during data visualization.

Excel sorts data based on the first character, which caused '10+ Miles' to be placed below '2-5 Miles' due to the 1 < 2 sorting logic. This issue skewed our plot results.

![commute_distance_issue](https://github.com/user-attachments/assets/a6de9b27-3280-45fe-bd15-78b0ebe7dd98)

To fix this, I used the Find & Replace tool to change '10+ Miles' to a text value that Excel would correctly order above the numerical data.

![commute_distance_issue_1](https://github.com/user-attachments/assets/19cd94f7-f10d-48e8-939a-2f438d5a9cfa)

I decided to replace these values with 'Over 10 Miles'

![commute_distance_issue_2](https://github.com/user-attachments/assets/3890db76-dab0-4e32-af6d-757346569dd2)

Here, we can see 113 replacements were made, and the values wthin the column were successfully replaced.
This has helped me to quickly resolve the issue, the values now read in order of their respective distances as you will see later when we approach the next sections.

<br/>
<br/>

<h3>Grouping/Clustering</h3>
Lastly before our dataset is ready and complete, looking for features to group/cluster during exploratory data analysis helps to uncover patterns, relationships, and underlying structures within the data. 
Being able to group similar data points in features allows you to explore and reveal hidden trends and guide more targeted analysis ultimately leading to better-informed decisions.

When considering this dataset, 3 particular groups came to mind:
- Gender group
  - For the gender no work is required here as the are already naturally distincting grouped apart, these being by <b>Male</b> and <b>Female</b>.
- Income group
  - For the income group, I will look at the averages later, so there is also no need to form any new groups here. 
- Age group
  - For the age group, natually as the dataset comes, each entry/row data pointmhas their owen personal specific age associated to that person.
<br/>

By grouping age groups together we can simplify analysis and gain insights more easily. It allows for the identification of trends/patterns and behaviours within  demographic groupings, making it easier to compare data. Additionally grouping also helps manage variability by reducing the number of unique values, especially in large datasets.

The first thing I wanted to check was the youngest entry, and the oldest entry.
In order to do this, I highlights the 'Age' column, and used Excel mathematical formulas to figure this out:
- Using the =MIN() formula to identify to smallest numercial value within the 'Age' column, i.e. the youngest person.
- Conversely using the =MAX() formula I can identify to largest numercial value within the 'Age' column, i.e. the oldest person.

As a result I identified the youngest age to be 25, and the oldest to be 89.
Knowing this allows me to carefully dispict and disect my age groups/brackets.

For my age brackets, I decided to split the data into 3 groups: Adolescent, Middle Age, Old (bearing in mind I wanted to name this alphabetically, so that Excel maintains the order in correspondecne to the age group values.
- Adolescent, x < 31, i.e. ages 0-30
- Middle Age, 31 =< x =< 54, i.e. ages 31-54
- Old, x > 54, i.e. ages 55+

Firstly, I created a new column for the 'Age Groups'.

![bike_buyers_age_groups_1](https://github.com/user-attachments/assets/fdb6cf95-0993-4813-beeb-a3f520bed5fa)

Then to be able to map these brackets out, I used a neat trick using Excel formulas, in the form of nested IF statements.

We have three conditions to determine the appropriate 'age group' based on 'age.' The nested IF statement first checks if the age is greater than 54; if 'TRUE,' it returns 'Old.' If 'FALSE,' the statement moves to the next condition, checking if the age qualifies as 'Middle Age.' If this condition is also 'FALSE,' it falls to the final IF statement to determine the remaining age group."

![bike_buyers_age_groups_2](https://github.com/user-attachments/assets/8201f1c1-ca0c-42c9-a890-1fc09708945d)

As a result, we are easily able to generate this new column, where the specific age's of each person have been categorized into 3 separate groups.

<br/>

After thoroughly cleaning and formatting the dataset, all duplicates, and errors have been addressed. The data is now standardized, complete, and well-structured, ensuring accuracy and reliability for subsequent analysis. 
<br/>
With a clean and properly formatted dataset, I am now ready to proceed to the next phase of the project, where I will be creating and analysing pivot tables to extract meaningful insights.

<br/>
<br/>

<h2>Pivot Tables and Data Visualisations</h2>
















<br/>
<br/>
<br/>
<br/>
<br/>
<br/>
<br/>
<br/>
<br/>
<br/>
<br/>
<br/>
<br/>
<br/>
<br/>
<br/>
<br/>
<br/>
<br/>
<br/>
<br/>
<br/>
