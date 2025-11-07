# ⚡ Project Name

> This group project is part of Special Topics in Database's class, I focused on cleaning and preparing data for the next step (PowerBI).

---

## Initial Step

we used the dataset from this kaggle <a href="https://www.kaggle.com/datasets/arashnic/cinema-ticket">(cinema-ticket) 

This dataset contain around 8 months of data in 2018 from Feb to Nov.
- 14 variables
- 142,524 rows with around 125 missing values in 2 columns: occu_perc and capacity.
- The data inside the main table might not make sense much if compare to Thailand context that is the reason why I modified the main table to close to the realistic Thailand Theatre Industry
by adding 2 tables: 
<img width="623" height="491" alt="image" src="https://github.com/user-attachments/assets/379a3751-eb27-4a0a-92f3-23373a30d483" />

The main table reason why I choosed to modified the main table because the main table many variables has highly correlation and calculatable from each other. <br>
Ex. occu_perc is short for occupancy_rate that can be calculated from the capacity fields. <br>
Total_sales can be calculated from tickets_sold - ticket_outs (ticket that sold but got cancelled)


---
>> One of many things that I have learned from this project is that there are many ways to permutate when doing data cleaning, analysis.
>>  Really, depends on thesis idea! ⚡
