 
![Screenshot at Aug 20 17-10-42](https://github.com/user-attachments/assets/29fdc54d-b57d-4422-a9f8-f26571133436)


<h1> bike_buyers_project </h1>

<h2> Description </h2>
An Exploratory Data Analysis (EDA) on 'Bike Buyers' dataset using MS Excel. 
'Bike Buyers' dataset contrains 1000 entries of customers from different backgrounds, and whether they <b>did</b> or <b>or did not</b> purchase a bike.

In this project, I will analyse the data by exploring through the dataset and its features, creating tables to help summarise and access quick information/highlights, then create insightful data visualisaions in the form of graphs and dashboards, which will help me to identify patterns and trends.
<br />

<h2>Languages/Tools and Skills Used</h2>

- MS Excel 
- Data Cleansing (missing values, removing duplicates, find & replace), Data Standardisation, Data Filtering, Pivot Tables, Data Visualisation (Charts + Dashboard)

<br />


<h2>Data Cleansing</h2>

In this section, we focus on data cleansing. A crucial process in ensuring the quality and reliability of our dataset. By addressing issues such as missing values, duplicate entries, and inconsistencies. Proper data cleansing lays the foundation for generating meaningful insights and making informed decisions based on clean, reliable data.

![bike_buyers_dataset_original_csv_to_excel](https://github.com/user-attachments/assets/2656df00-98f1-492b-8f57-78dce2350d54)
![bike_buyers_original_row_count](https://github.com/user-attachments/assets/8bc86c1d-7941-4246-9720-38055376b159)
(1026 rows, excluding the columns/feature headers)

After uploading the <b>bike_buyers.csv</b> dataset into excel, the first step I took was to create a new sheet. I called this the 'working_sheet'.

![bike_buyers_working_sheet](https://github.com/user-attachments/assets/d789067f-e949-42a5-a567-d06b74e8bbdb)

As the sheet describes, it will act a new sheet for which I copied all the original and raw data from the bike_buyers table, into the new sheet to conduct work for data cleansing and exploratory data analysis.

The reason I thought it was important to do this was so that I would have an area on which I could manipulate and transform the dataset freely, without having to worry about errors/mistakes, avoiding losing vital/valuable rows of information/data.
The original dataset is preserved in the case of needing to go back to it, a 'back-up'.
<br/>

Inspecting through the table, I am starting out by making sure to look at the number of rows and columns(features) I have. <br/>
- I want to ensure that I understand the dataset I am working so that I am able to make informed decisions about the next steps to take.<br/>
- I am also looking out for features to consider as potential categorical features which I can maybe use to compare different groups against, or depict patterns/trends within certain areas.
<br/>

I am now able to make a list of the things I am eager to have a look at for my data cleansing process or 'hot' areas in which I think common issues may arise:
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

This is a super useful tool when it comes to cleaning data. Not only am I able to spot missing data within the columns and thus the dataset, I would also be able to look for <b>spelling errors</b> as well as <b>standardisation errors</b>.

Fortunately making my job a slighlty quicker/easier, after investigating each column and each of the unique values within the rows of each column, I was happy to see that there were no missing values!
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
Notice, when applying the tool to a range with multiple columns, the tool will remove the entire row of the duplcated value.

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

- One thing I did note however was the data type that this column was presented to me. I recieved the column data type as a 'general' form, when in this case as an income, it would be much more appropriate for us to have this changed into a currency format.
- I also decided to remove the decimal places in order to simplify the presentation of financial data. Removing decimal places also allows for consistency with our numerical data. This is especially useful for when we later wish to represent the data visually, using graphs and plots.

<br/>
<br/>
<br/>

Continuing through the column features, I am continuing to look through for any errors or formats than need to be changed.
The next column I notice that may cause issues later, is within the commute distances.

In this column, we have values:
- 0-1 Miles
- 1-2 Miles
- 2-5 MIles
- 5-10 Miles
- 10+ Miles

Reading through these, none of the unique value pose problem in how they are appear. However there is one crucial issue with this, in which I later faced when it came to my data visualisation plots.

Excel will count and arrange these data values by taking the 1st characater and then sort into ascending order.

![commute_distance_issue](https://github.com/user-attachments/assets/a6de9b27-3280-45fe-bd15-78b0ebe7dd98)

Here we can see that Excel has valued, 10+ Miles <b>below</b> 2-5 Miles, as 1<2. This causes a real problem for us as it skews the result of our plot.

To tackle this issue, we can once again use the <b>Find & Replace</b> tool.

As this is an issue with the order Excel reads in the data, naturally i believed in order to fix this issue, I would need to change all the '10+ Miles' values to something that would exceed numerical data, i.e. text values.

![commute_distance_issue_1](https://github.com/user-attachments/assets/19cd94f7-f10d-48e8-939a-2f438d5a9cfa)

I decided to replace these values with 'Over 10 Miles'

![commute_distance_issue_2](https://github.com/user-attachments/assets/3890db76-dab0-4e32-af6d-757346569dd2)

Here, we can see 113 replacements were made, and the values wthin the column were successfully replaced.
This has helped me to quickly resolve the issue, the values now read in order of their respective distances as you will see later when we approach the next sections.

<br/>
<br/>

<h3>Grouping/Clustering</h3>

Lastly before our dataset is ready and complete, Lloking for features to group/cluster during exploratory data analysis helps to uncover patterns, relationships, and underlying structures within the data. 
Being able to group similar data points in features allows you to erxplore and reveal hidden trends and guide more targeted analysis ultimately leading to better-informed decisions.

When considering this dataset, 3 particular groups came to mind:
- Gender group
  - For the gender no work is required here as the are already natrually distincting grouped apart, these being by <b>Male</b> and <b>Female</b>.
- Income group
  - For the income group, I will look at the averages later, so there is also no need to form any new groups here. 
- Age group
  - For the age group, natually as the dataset comes, each entry/row data pointmhas their owen personal specific age associated to that person.
<br/>

By grouping age groups together we can simplify analysis and gain insights more easily. It allows for the identification of trends/patterns and behaviours within  demographic groupings, making it easier to compare data. Additionally grouping also helps manage variability by reducing the number of unique values, especially in large datasets.



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

<h2>Program walk-through:</h2>

<p align="center">
Launch the utility: <br/>
<img src="https://i.imgur.com/62TgaWL.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
Select the disk:  <br/>
<img src="https://i.imgur.com/tcTyMUE.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
Enter the number of passes: <br/>
<img src="https://i.imgur.com/nCIbXbg.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
Confirm your selection:  <br/>
<img src="https://i.imgur.com/cdFHBiU.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
Wait for process to complete (may take some time):  <br/>
<img src="https://i.imgur.com/JL945Ga.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
Sanitization complete:  <br/>
<img src="https://i.imgur.com/K71yaM2.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
Observe the wiped disk:  <br/>
<img src="https://i.imgur.com/AeZkvFQ.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>

<!--
 ```diff
- text in red
+ text in green
! text in orange
# text in gray
@@ text in purple (and bold)@@
```
--!>

