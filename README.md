# CHILD-LABOUR-CASE
ASSIGNMENT DATA PREPARATION AND CLASSIFICATION: CHILD LABOUR CASE

**1. CONTEXT **

In  recent  years,  the  Belgian  government  has  taken  an  active  interest  in  promoting  the  well‐being  of 
children worldwide. As part of this effort, they have funded programs aimed at assessing the quality of 
life of children across the globe.  
Your team is working with the "A Better Future" NGO, a leading organization focused on monitoring and
combating  child  labour  around  the  world.  Recently,  the NGO  conducted  a  comprehensive  survey  of 
children between the ages of 7 and 17 in Africa, with the goal of better understanding the extent and 
nature of child labour in the continent. 
Your  team's  objective  is  to  prepare  and  analyse  the  data  collected  in  this  survey  and  develop  a 
classification model that can accurately predict whether a child is involved in child labour or not. This 
model will  be a powerful  tool  for identifying  the key  predictors  of  child labour and  taking action  to 
prevent it. By gaining a deeper understanding of the factors that contribute to child labour, we can work 
to create a better future for children around the world. 

**2. DATA **

The survey was conducted in 2022 and collected more than 13,000 responses.  
10% of the record has been kept away to evaluate the performance of your model on unseen data. You 
can find those records under unlabelled_data.csv.  
You will be using the remaining 90% of the records to train and evaluate your models. Those records have 
been organized into three datasets, each of which is represented as a CSV file: dataset1.csv, dataset2.csv, 
dataset3.csv.  These  datasets  include  valuable  information  on  various  aspects  of  the  children's  lives, 
including their demographics information, educational background, … 

All the details about the collected data can be found in the “STATS406 ‐ Assignment metadata info.pdf” 
file. 

**3. WHAT IS EXPECTED FROM YOU? **

You can find below a schema of the general workflow you should follow for this assignment. Note that 
even if this process is here depicted as a linear process, you should work in iterations. For example, you 
may go back to the data cleaning step after the data exploration step. You will also find in the schema the 
tool that we recommend for each step. 

STEPS TO DO:

_1. Business understanding
Make sure you understand the use case and the different features  (refer to STATS406 ‐ Assignment metadata info.pdf).
Data merging
_2. Merge the 3 datasets into one dataframe Python (using pandasql).
_3. Data cleaning Handle missing values, encoding  errors, outliers Python.__

ADITIONAL INFO @:

You will have to perform the data merging and cleaning in python. This means that you are not allowed  to manually modify  the input  files. For  this, we advise using pandasql. Pandasql will have access  to all pandas dataframes you create (if you read in the csv files, but also if you create new dataframes) and will  always return a pandas dataframe (that you can also use in next pysql query). You will have to run the following lines to initate pandasql: 

![image](https://user-images.githubusercontent.com/131664916/233973649-1ae1334d-3a15-4e2a-a4d8-bfd37f40eaae.png)

**4. SOME TIPS **

Please find below some tips or useful tricks that will help you out in this assignment: 
‐ If you can't read or write to your google drive as you can't find the right path, you can do 
import os
os.listdir('/gdrive/')
This will print out all the files and folders of the specified path, like this you can incrementally 
check if your path is correct by each time adding the next folder to the path in the listdir 
function 
‐ If you need to combine two or multiple dataframes having the same columns into one dataframe, 
think about using the UNION ALL operator in SQL as we did in TP 2 here. 
‐ In python, df.colums will print out the column names of your dataframe so that you can check 
if there are no spaces or other specific characters 
‐ In python, df.dtypes will print out the types of each column, if it marks object, it is probably 
a string. 
‐ You  will  notice  that  the  dataset  has  missing  values.  You  will  need  to  understand  how  the 
questionnaire was made and answered (refer to the metadata.pdf file) to understand how to deal 
with  those  missing  values.  For  example,  Q16Mothparthh  is  skipped,  so  is  missing,  if  the 
respondent answered ‘no’ in Q15Mothaliv. 
‐ Make sure to use the “Child_Labor” as target variable in your modelling part. 
‐ Since the target variable is characterized by quite an unbalanced distribution in both the training 
and test sets, we would suggest having a look at chapter 15.5 SAMPLING AND MISSING VALUE 
TOOLS (pages 513 to 516) in the Reference book (you can find here the link to the pdf version on 
the  UV).  There  you  can  find  useful  suggestions  on  how  to  handle  unbalanced  datasets  with 
Rapidminer. 
‐ For the recommendation part, an idea could be to look at the variable's importance of your model. 
This could give you insights about which variables have a high impact on whether a child would 
be predicted to be involved in Child Labor or not. For example, for random forest models, you can 
refer to Weight by Tree Importance ‐ RapidMiner Documentation. 
