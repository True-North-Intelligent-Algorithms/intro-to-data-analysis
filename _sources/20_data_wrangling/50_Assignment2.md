# Assignment 2

Individual Assignment: 14 Points
 
Purpose of assignment: 

Learn to join datasets  
Learn to create groups  
Learn to analyze groups for trends  
Learn to plot data from groups  

Background

Two years ago NIKE introduced a new shoe called the 4%, that was advertised as improving running times by 4%.  Very quickly almost all elite athletes began using the new shoe.  In this assignment you will look at data from 2013 and 2015 (before the new shoe waas introduced) and 2018 and 2019 (at which point the majority of athletes were using the new shoe).  

You will group this data in an attempt to identify how running times changed for elite athletes after the introduction of the new shoe. 

You will need the following datasets, men2013.txt, men2015.txt, men2018.txt, mean2019.txt, women2013.txt, women2015.txt, women2018.txt, and women2019.txt.  

The datasets can be found in the class repository under the 20_data_wrangling section.   

1.  In the example we use ```pd.read_fwf``` to open data.  What is the ```pd.read_fwf``` function??  Why do we use it in this case instead of ```pd.read_csv```??  
2.  Why do we pass an extra parameter called ```name``` (hint for help on the ```pd.read_fwf``` function call ```help(pd.read_fwf```, it should list all the optional parameters)  
3.  Why do we call ```.head(numRunnersToAnalyze()``` at the end of each ```read_fwf``` call??  (hint try changing the parameter numRunnersToAnalyze to 10 and rerun the notebook)
4.  Modify the notebook so that we also read the men and women datasets from 2013 and 2018 (hint you will have to copy and paste a bit).  Run the notebook over and take a screen shot.  After this modification you should have stats for years 2013 and 2018 in addition to 2015 and 2019.    
5.  Change the ```numRunnersToAnalyze``` parameter to 10 and rerun the notebook.  Take a screen shot.  Are the trends in performance for the top 10 different than the top 100?? 
6.  What does the following block do??  what is ```def``` used for??  Why is there no output when you run the block?
``` python
def timeToSeconds(time):
    temp=time.split(':')
    return 3600*int(temp[0])+60*int(temp[1])+int(temp[2])
```
7.  What does the below block do??  What is ```apply``` (hint run ```help(final['time'].apply)```).  (hint 2 - look at the dataframe ```final``` before and after calling ```apply```)
``` python
final['seconds']=final['time'].apply(lambda x: timeToSeconds(x))
```
8.  Make a bar plot showing the average time of the top 20 runners before (2013 and 2015 and after 2018 and 2019) 
the new shoe was introduced.
9.  Make bar plots showing the average time of runners from each country.  What other bar plots would be interesting to see?
10.  What is a cofounder ?  Can we conclude for sure the new shoes made runners faster?  How confident can we be in our result?  Answer in words and think about what math we'd need to use to answer these questions more formally (in one of the next sections we will explore hypothesis testing and statistics more formally)
11.  Submit homework via your github account.  Create a new folder 'homework' and add new notebooks and markdown files with the answers, then add (stage), commit, and push your work to your personal branch of the class repository. 