# Efflux Processing
## Purpose
This shiny application provides an easy interactive method to trim sample data 
and fit linear regressions to each sample's data. It is specifically designed 
for soil and stem efflux but it will work with any type of data that has a 
unique sample ID and dependent/independent variables.

## Process
### Upload a File
Select either a raw *.dat file from a PP Systems EGM infrared gas analyzer or 
any *.csv. If selecting a *.csv please be sure your file contains one or more 
column that can be used as a unique sample ID.

### Identify variables and identifiers
Drop down menus will be populated with column names, if you are working with any
non-efflux data the time variable corresponds to the x-axis and the concentration
variable corresponds to the y-axis.  
  
The unique identifier can be made up of multiple columns and these will be 
pasted into a single 'SampleID' column. If one column is selected it is renamed to 
'SampleID'.

### Remove unwanted data
Data for each sample are displayed on a plot and points can be removed by 
selecting them on the plot or remove multiple points by creating a box around 
the points you wish to remove. _Please keep in mind that this step is not for removing data you view as 'outliers'. Points should only be removed due to equipment/sampling errors or to remove efflux 'ramp up' at the beginning of sampling."_  
  
After you are finished with a sample press 'Save & Next' to advance to the next sample. This will also save information about the model fit and update the output data, removing the data you selected. You can view any sample using the dropdown mean or return to the previous plot with the 'Previous' button (navigating this way will not save any of your selections). Resetting the probe will delete the saved regression information and add all of the sample points back to your plot and the output data."

### Download  
Once you have saved information from at least one plot the updated datset, regression information, and the final plot will all be available for download. I recommend downloading data often to avoid losing work if the app or your browser has a problem.

Downloaded data will be a zipped file containing the final plots for each sample and four CSVs.'Editted_Samples.csv' contains only the samples you editted and 'All_Samples.csv' contains your editted samples with uploaded samples you did not edit. 'Efflux_Summary.csv' contains the sample ID and the slope (assumed to be efflux in ppm), futher information about the models can be found in 'Model_Fits.csv'."


__To Do__
* Add PPM to gCO<sub>2</sub> conversion
* Remove X & Y variables from Unique ID choices
* Download a csv of removed data points
* Delete processed data when ID is changed
* Move variables selection to UI instead of server�
