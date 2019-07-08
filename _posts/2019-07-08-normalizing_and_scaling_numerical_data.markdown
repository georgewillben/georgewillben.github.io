---
layout: post
title:      "Normalizing and Scaling Numerical Data"
date:       2019-07-08 04:36:52 +0000
permalink:  normalizing_and_scaling_numerical_data
---


         When trying to create a model to make predictions, it is important to have it free of outliers, as well as make sure data follows the proper distribution.  Also, when dealing with multiple sources of data, it is important to have the diffrent sources of data lie close to each other on the numberline, so that numbers of high magnitude are not seen as more important then data sources of lower magnitudes. Unfortunately us data scientists often get data that is not suitible to be fit to a known model. However, the data can often still be used if we manipulate the data. Transforming data so that it fits a normal distribution is called normalizing, and manipulating data so that diffrent sources of data are all relatively close on the number line is called scaling. The best thing to do first is remove outliers. Then it is time to  log-transform the data to make it normalized, and finally it is time to scale the data so that it fits within the range of zero to one. 
				 
				 Firstly, I will remove outliers from the data. To do this I find the inter-quartile range. This can be done by finding the 25% quantile and subtracting it from the 75% quantile. This can be done in pandas easily by using the .quantile() method; documentation seen here: (https://pandas.pydata.org/pandas-docs/stable/reference/api/pandas.DataFrame.quantile.html). Then I take the inter-quartile range and multiply it by three halves. If any data is farther away from the mean than 1.5 times the inter-quartile range, It is an outlier and I throw the data out. Removing outliers ussually makes models more accurate.

				 Secondly, I normalize the data using log-transformation. Log-transforming can often take data that looks unpredictable, and turn it into a smooth normal distribution. It does this by replacing every element from an array with that elements natural log. To do this to an array simply call np.log() and use your array as the parameter. For more information on np.log() see the documentation here: (https://docs.scipy.org/doc/numpy/reference/generated/numpy.log.html).
				 
				 Lastly, I scale the data to a range from zero to one. To do this I use the 'min-max' method. First take the data's minumum values and maximum values and save them. Then go through each element in an array of data, taking the element's value and subtracting the minimum value of the array from it. The third step is to take this number and divide it by the maximum minus the minimum. Doing this will make all the data contained in an array lie in a range from zero to one. In my opinion the 'min-max' method is the best way to scale data.
				 
				 In conclusion I covered how to remove outliers, log-transform data, and the 'min-max' method. These are important things to do to make the data optimal to work with. This is a very important part of the data science process.
				 
				 
				 
				 
				 
				 
				 
