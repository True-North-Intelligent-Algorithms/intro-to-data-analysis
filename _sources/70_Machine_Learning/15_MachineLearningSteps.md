# Machine Learning Steps 

* Collect Data  
  * Scrape a web site  
  * Use an API  
  * create a survey  
  * built a device (weather, blood glucose) 
  * Acquire Images 
* Prepare Input data  
  * Fix errors  
  * Deal with missing data
  * Make sure filenames are consistent  
* Explore data
  * Open data (spread sheet, image viewer, etc.)
  * Do you recognize patterns ?  
* Create Training Data
  * Training data is a set of inputs with the correct answers.
* Train algorithm  
  * This is machine learning  
  * Apply algorithm to known values so it can learn
* Sanity check algorithm
  * Use self prediction (predict the training set) to verify the algorithm is learning properly
  * Results on self prediction should be very good, often deceptively good.  
  * Do not present these results to the CEO. 
* Test algorithm
  * Apply algorithm to known but 'unseen' values to test performance
  * DO NOT use training data for this testing. 
  * This test should be run on separate partition that was not in the training data.
  * Maybe not a good idea to show these results to CEO either
* Tune algorithm
  * Adjust algorithm parameters to achieve better test performance
* Validate algorithm 
  * Apply algorithm to completely new test values to verify algorithm works on new 'completely unseen'
  * If performance not yet satisfactory the new partition of data, can be used for training/testing data and start cycle again.
  * Only show CEO the results when performance becomes good on sets of data the AI engineer has never seen before. 