DELETE THIS LATER

# US-Healthcare-Spending
# Project Overview
The following project overview focuses on our project proposal, data sources, and data cleanup and analysis.

# Project Proposal
We are focusing our research project on national health expenditures. We aim to find patters in health care spending by a variety of funding sources and national demographics over the course of multiple years. 

# Finding Data
We will use data provided by the Centers for Medicare & Medicaid Services on their data and research website: https://www.cms.gov/data-research/statistics-trends-and-reports/national-health-expenditure-data. Specifically, we are using national heath expediture data gathered by age and gender. 

Source: Centers for Medicare and Medicaid Services, Office of the Actuary, National Health Statistics Group


# Data Cleanup and Analysis
For our analysis, we wanted to look at the following three questions:

1. What does total healthcare spending look like from 2002 to 2020 when sorted by Sex, by age group, and lastly by Sex and age group?
    
2. What is the breakdown of spending per service? What does healthcare spending look like for specific services? We looked closer at spending for Dental Services and on Prescription Drugs.

3. What trends and estimates can we make from total spending by using regression charts?

For all three questions, we used the Age and Sex spending data CSV file provided by the Centers for Medicare and Medicaid Services. 

To answer the first question, the imported Age and Sex CSV was used to make a complete health spending DataFrame. Then, the columns for Payer,  Service, and Age Group were filtered to include only total expenditure. The total spending row was removed from the Sex column to show spending per Sex. The DataFrame was then filtered to remove the Payer, Service, and Age Group columns so the data could be set for plotting. Once the DataFrame data was filtered down, the index was set to Sex and then transposed to plot a line chart. This final DataFrame was used to create the Total Spedning by Sex line chart using Matplotlib. 

To show total spending by Age Group, the original DataFrame was filtered to show total spending per Age Group per year by filtering Payer, Service, and Sex to total expenditure and then removing the total from the Age Group column. Once that data was cleaned, the Payer, Service, and Sex columns were removed to be able to plot. The index was set to Age Group, and the DataFrame was transposed to plot the line chart. This final DataFrame was used to create the Total Spending by Age Group line chart using Matplotlib. 

To show total spending per Sex per age group, the original DataFrame was filtered to show total spending for the Payer and Service columns, and then the Age Group and Sex columns were filtered to remove total spending rows only to show the spending per Sex and Age Group. The Payer and Service columns were then removed, and the DataFrame was split into separate female and male spending DataFrames by filtering the Sex column. Once the Female and Male DataFrames were created, the Sex column was removed from each one, the index was set to Age Group, and the DataFrames were transposed in order to plot. Each DataFrame was then used to plot Total Spending for Females/Males by Age Group using Matplotlib.

To answer question two, three different broad categories were analyzed. First, we looked at spending per Service. We filtered the raw data to show the total for all payer sources, made sure all medical services were listed, and filtered to the total for all age groups genders. From their we averaged the total spending for each service across the years we have data for. We then plotted the average results into a doughnut chart and a bar chart. During the cleaning and filtering process, some trends emerged that we wanted to explore closer. We wanted to explore Dental Services and Prescription Drugs closer. For each, we applied similar filters as before and charted line and bar charts. 

For question three, I imported all that was needed to make my linear regression. I opened the data set using age_and_sex.csv, and then I started cleaning my data set to specify what I wanted first. I used the payer column to grab the total spending; then, I took the service column to filter by Total Personal Health Care. The last column I filtered was age group by total. The next step was to make the sex my index for the year, then flip my data set by using the transpose for my health index. Once everything was simplified I defined my linear regression. Once I had my definition completed, I made three linear regression graphs to show the total of male and female healthcare spending, male spending, and female spending. 


# Results

-What does total healthcare spending look like from 2002 to 2020 when sorted by sex, by age group, and lastly by sex and age group?

Based on the line charts created in our analysis, we can see that spending for females consistently outpaced males from 2002 to 2020. Total healthcare spending for Females went from $778,215 millions in 2002 to $1,818,581 millions in 2020, while spending from Males went from $587,266 millions to $1,548,394 millions. 

The highest healthcare spending occurred in the 45-64 age group throughout all the years, but the 65-84 age group is encroaching on this spending as of 2020. The lowest healthcare spending is within the 85+ plus age group, probably due to the smaller size of this population as individuals pass.

Lastly, when we look at spending per sex and age group for females, the spending between the three age groups (45-64, 65-84, & 19-44) is pretty similar, with some fluctuations over the years. In 2002, the 65-84 age group was just over the other two and then dipped in the middle from 2006 to 2018, then shot up in 2020 (most likely due to COVID-19 spending per CMS). The 0-18 and 85+ show the lowest spending across all of the years, with under $156,000 millions each in 2020.

Spending per sex and age group for males follows a similar pattern between age groups, with the 45-64 age group showing the highest expenditure and the 85+ age group the lowest. Unlike health care spending for females, spending for males across age groups does not intertwine over the years; all age groups continuously increase at similar rates. The 65-84 group is showing a spike in 2020, like female spending, but it does not surpass the 45-64 group as female expenditure does.

-What does healthcare spending look like for specific services? We broke down spending for Dental Services and Prescription Drugs.

Looking at the chart for Average Spending by Service, Hospital Care is by far the highest spending category on average. Between the years 2002-2020, it averaged almost 37% of all healthcare spending across all payer sources. The next highest category was Physician and Clinical Services, accounting for almost 25% of all spending. Together, the top 3 highest spending categories (adding in Prescription Drugs) averaged $1.6 billion (72.4% of all healthcare spending). 

Dental Services spending shows quite a large change in services per age group. Looking at spending year over year per age group, people in groups 65-84 and 0-18 saw the largest increases in dental spending. Contrary to that, the age group of indiviuals who are 85+ spent not only the least amount of money on Dental Services, but also saw the smallest increase in spending from 2002-2020.

Looking at Prescription Drug spending, we see increases in spending every year, more than doubling in average spending from 2002 to 2020. Spending on prescription drugs per gender appears realatively even. Although female spending is slightly higher per year, the difference is minimal. From 2002-2006 age groups 19-44 and 65-84 had very similar prescription drug spending, then 65-84 started spending more each year, ultimatly spending roughly $35 billion more by the year 2020. The 85+ age group, again, saw the least amount of spending each year.

-What trends and estimates can we make from total speding by using regression charts?

Noticeable trends we've seen were that female spending is higher than male spending. From 2002 to 2020, the total expenditure increased by $2,001,494 million. For Females, spending increased by $961,128 millions. For males, spending increased by $1,040,366 millions. Between 2002 and 2020, male healthcare spending increased by 79,238 more than that of females. The most significant increase happened in 2020 (COVID), when we saw a rise in healthcare spending by almost two hundred thousand. If the trend continues to increase every two years by the rate, we would be spending an estimated $3,756,975 - $5,802,344 million.