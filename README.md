# ExpectedNumberofRelocation
This repo includes Matlab codes to calculate the expected number of relocations for different handling equipment. 

To work with this repository, you just need an Matlab 2016 or later version.

The aim is to run each "mainXXX" script for each zip file to get the expected number of relocations for any bay design with different maximum row and tier numbers. The default values are from 1 to 8 for tiers and from 1 to 9 for rows.

Output:
It will create a single excel file(SUMMARYXXX) including the expected number of relocations, standard deviation, quartiles and run times for each bay configuration.
To try differeny bay designs, you only need to change the "mainXXX" scripts for particular bay configuration of maximum bay and tier numbers. 
The published paper can be found as Karakaya, E., Vinel, A., & Smith, A. E. (2021). Relocations in container depots for different handling equipment types: Markov models. Computers & Industrial Engineering, xx, xx.
