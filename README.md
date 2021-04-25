# Gaussian Distribution Function

### By Rodrigo Guarneros

This package is created based on an Oriented Object Programming approach.

This package is able to calculate gaussian and binomial distributions for a simple list of observations.

# Files

You need a simple list in format .txt

# Installation

pip install calculating-distributions
from calculating_distributions import Gaussian, Binomial


# Documentation
## Gaussian Distribution

    Gaussian distribution class for calculating and 
    visualizing a Gaussian distribution.

### Method Gaussian()
To calculate the distribution 
Attributes:
    - mean (float) representing the mean value of the distribution
    - stdev (float) representing the standard deviation of the distribution
    - data_list (list of floats) a list of floats extracted from the data file

### Method calculate_mean()
To calculate the mean of the data set.
        
Args: 
     - None
Returns: 
     - float: mean of the data set
     
## calculate_stdev():

Function to calculate the standard deviation of the data set.
        
Args: 
      - sample (bool, TRUE or FALSE): whether the data represents a sample or population
        
Returns: 
      - float: standard deviation of the data set     
      
## read_data_file():
    
  Function to read in data from a txt file. The txt file should have
  one number (float) per line. The numbers are stored in the data attribute. 
  After reading in the file, the mean and standard deviation are calculated
                
  Args:
  file_name (string): name of a file to read from
        
  Returns:
  None

## plot_histogram():

 Function to output a histogram of the instance variable data using 
 matplotlib pyplot library.
        
 Args:
 None
            
 Returns:
 None
 
## pdf(x):

  Probability density function calculator for the gaussian distribution.
        
  Args:
  x (float): point for calculating the probability density function
        
  Returns:
  float: probability density function output

## plot_histogram_pdf(n_spaces)

  Function to plot the normalized histogram of the data and a plot of the 
  probability density function along the same range
        
  Args:
  n_spaces (int): number of data points 
        
  Returns:
  list: x values for the pdf plot
  list: y values for the pdf plot
  
## Examples:

  gaussian_one = Gaussian()
  gaussian_one.read_data_file("numbers.txt")
  
  print(gaussian_one.mean)
  print(gaussian_one.stdev)
  
  gaussian_one.plot_histogram()

  gaussian_one.plot_histogram_pdf()
  gaussian_one = Gaussian(5,2)
  gaussian_two = Gaussian(10,1)

  gaussian_sum = gaussian_one + gaussian_two

  print(gaussian_sum.mean)
  print(gaussian_sum.stdev)
  gaussian_sum
  
# Binomial 

## Binomial(Distribution)

   Binomial distribution class for calculating and 
   visualizing a Binomial distribution.

Attributes:
   mean (float) representing the mean value of the distribution
   stdev (float) representing the standard deviation of the distribution
   data_list (list of floats) a list of floats to be extracted from the data file
   p (float) representing the probability of an event occurring
   n (int) number of trials
   
# Method to calculate the mean from p and n
        
   Args: 
   None
        
   Returns: 
   float: mean of the data set

calculate_stdev(self):

   Function to calculate the standard deviation from p and n.
        
   Args: 
   None
        
   Returns: 
   float: standard deviation of the data set
  
## replace_stats_with_data()
    
Function to calculate p and n from the data set
        
Args: 
None
        
Returns: 
float: the p value
float: the n value

## plot_bar():
  Function to output a histogram of the instance variable data using 
  matplotlib pyplot library.
        
  Args:
  None
            
  Returns:
  None

## pdf(k):
 
 Probability density function calculator for the gaussian distribution.
 
 Args:
 x (float): point for calculating the probability density function
 
 Returns:
 float: probability density function output


## plot_bar_pdf()

 Function to plot the pdf of the binomial distribution
        
 Args:
 None
        
 Returns:
 list: x values for the pdf plot
 list: y values for the pdf plot


## __add__(other):
        
   Function to add together two Binomial distributions with equal p
        
   Args:
   other (Binomial): Binomial instance
            
   Returns:
   Binomial: Binomial distribution
   
   
## __repr__()
    
  Function to output the characteristics of the Binomial instance
        
  Args:
  None
        
  Returns:
  string: characteristics of the Gaussian
![BasicMap](https://github.com/RodGuarneros/gaussiancalculator/blob/main/distribution2.png)
