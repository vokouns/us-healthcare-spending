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
    
    2. What does healthcare spending look like for specific services? We broke out spending for Medicaid, Prescription Drugs, and 
    
    3. What trends and estimates can we make from total spending by using regression charts?

For all three questions, we used the Age and Sex spending data CSV file provided by the Centers for Medicare and Medicaid Services. 

To answer the first question, the imported Age and Sex CSV was used to make a complete health spending DataFrame. Then, the columns for Payer,  Service, and Age Group were filtered to include only total expenditure. The total spending row was removed from the Sex column to show spending per Sex. The DataFrame was then filtered to remove the Payer, Service, and Age Group columns so the data could be set for plotting. Once the DataFrame data was filtered down, the index was set to Sex and then transposed to plot a line chart. This final DataFrame was used to create the Total Spedning by Sex line chart using Matplotlib. 

To show total spending by Age Group, the original DataFrame was filtered to show total spending per Age Group per year by filtering Payer, Service, and Sex to total expenditure and then removing the total from the Age Group column. Once that data was cleaned, the Payer, Service, and Sex columns were removed to be able to plot. The index was set to Age Group, and the DataFrame was transposed to plot the line chart. This final DataFrame was used to create the Total Spending by Age Group line chart using Matplotlib. 

To show total spending per Sex per age group, the original DataFrame was filtered to show total spending for the Payer and Service columns, and then the Age Group and Sex columns were filtered to remove total spending rows only to show the spending per Sex and Age Group. The Payer and Service columns were then removed, and the DataFrame was split into separate female and male spending DataFrames by filtering the Sex column. Once the Female and Male DataFrames were created, the Sex column was removed from each one, the index was set to Age Group, and the DataFrames were transposed in order to plot. Each DataFrame was then used to plot Total Spending for Females/Males by Age Group using Matplotlib.

For question two, 

For question three,

# Results

What does total healthcare spending look like from 2002 to 2020 when sorted by sex, by age group, and lastly by sex and age group?

    Based on the line charts created in our analysis, we can see that spending for females consistently outpaced males from 2002 to 2020. Total healthcare spending for Females went from $778,215 millions in 2002 to $1,818,581 millions in 2020, while spending from Males went from $587,266 millions to $1,548,394 millions. 

    The highest healthcare spending occurred in the 45-64 age group throughout all the years, but the 65-84 age group is encroaching on this spending as of 2020. The lowest healthcare spending is within the 85+ plus age group, probably due to the smaller size of this population as individuals pass.

    Lastly, when we look at spending per sex and age group for females, the spending between the three age groups (45-64, 65-84, & 19-44) is pretty similar, with some fluctuations over the years. In 2002, the 65-84 age group was just over the other two and then dipped in the middle from 2006 to 2018, then shot up in 2020 (most likely due to COVID-19 spending per CMS). The 0-18 and 85+ show the lowest spending across all of the years, with under $156,000 millions each in 2020.

    Spending per sex and age group for males follows a similar pattern between age groups, with the 45-64 age group showing the highest expenditure and the 85+ age group the lowest. Unlike health care spending for females, spending for males across age groups does not intertwine over the years; all age groups continuously increase at similar rates. The 65-84 group is showing a spike in 2020, like female spending, but it does not surpass the 45-64 group as female expenditure does.

2. What does healthcare spedning look like for specific services? We broke out spending for Medicaid, Prescription Drugs, and 

3. What trends and estimates can we make from total speding by using regression charts?