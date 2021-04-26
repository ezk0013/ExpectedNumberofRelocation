# ExpectedNumberofRelocation
This repository includes Matlab codes to calculate the expected number of relocations for different material handling equipment in shipping container yards.

The published paper describing these codes in detail can be found in Karakaya, E., Vinel, A., & Smith, A. E. (2021). Relocations in container depots for different handling equipment types: Markov models. Computers & Industrial Engineering, 157, 107311. https://doi.org/10.1016/j.cie.2021.107311 

To work with this repository, you need the Matlab 2016 or later version.

The first version assumes static arrival and retrieval rates.  Here, the aim is to run each "mainXXX" script for each zip file to obtain the expected number of relocations for any bay design with different maximum row and tier numbers. The default values are from 1 to 4 for tiers and from 1 to 6 for rows. The default arrival rate is 0.5 and the default retrieval rate is (1- arrival rate). Any arrival rate can be used by changing the "index" of the "ArrivalRates" array.

The second version allows for dynamic arrival and retrieval rates and here the aim is to run each "mainXXXVariableArRate" script for each zip file to get the expected number of relocations for various bay designs under one of two alternative scenarios for variable arrival and retrieval rates. Scenario 1 assumes that the retrieval rate is proportional to the number of containers in a bay at any given time, while the arrival rate is proportional to the number of missing containers (that is, depot vacancies). Consequently, the probability of retrieval at a certain time can be evaluated as the number of containers divided by the bay capacity. Scenario 2 assumes that if the number of containers in a bay configuration is less than half of the capacity of the bay design, the retrieval and arrival probabilities are 0.25 and 0.75 respectively, and vice versa if the bay is more than half full. The default scenario is Scenario 1 while Scenario 2 can be run by editing the Rows 29-45 in "mainXXXVariableArRate" script. If rows 30-39 are uncommented and rows 42-43 are commented, Scenario 2 can be run.

XXX: "Crane", "TopLifter", "ReachStacker"

Each of these is specific to the name material handling device.

Output: Each will create a single excel file (SUMMARYXXX) including the expected number of relocations, standard deviation, quartiles, and run times for each bay configuration. To try different bay designs, you only need to change the "mainXXX" scripts for a particular bay configuration of the maximum bay and tier numbers.

