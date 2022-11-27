# MNXB01-TEAMF


####################################################################################################################################################################
FILTERED DATA
2022.07.2+576

###########################################################
How to execute
###########################################################

1. Be sure to have the last available version of R
2. We recommend to use RStudio 
3. Please install the required libraries 
4. Load the libraries
5. You are done!, the code is good to go. 

############################################################
Content
############################################################

Data_Filtered_GREA_LESS:
File that contains all the data divided in two groups (0-269 days), (270-365 days) and filtered by hours 07:00:00, 13:00:00, 20:00:00

Data_Filtered_Hours:
File that contains all the data Filtered by hours 07:00:00, 13:00:00, 20:00:00

############################################################
Outputs
############################################################

FALSTERBO_GREATER_HOURS: 
File that contains the FALSTERBO data filtered by the group (0-269 days)  

FALSTERBO_LESS_HOURS: 
File that contains the FALSTERBO data filtered by the group (270-365 days)  

UMEA_GREATER_HOURS: 
File that contains the UMEA data filtered by the group (270-365 days) 

UMEA_LESS_HOURS: 
File that contains the FALSTERBO data filtered by the group (270-365 days)  


The filtered data have been furhter modified with Excell, in order to add some new columns to make two final .txt files, one for Falsterbo and one for Umeå, which include all the necessary informations, to be used in ROOTcfor all the plots. Excell was used first to add two new columns for each one of the files Falsterbo_1 and Umea_1, reporting the difference between the maximum temperature values ("Maxm") and the mean temeperatures ("Avg") in the column "DeltaTmax", and for the difference between "Minm" and "Avg" in "DeltaTmin". Furhtermore, Excell has been used to make other two new columns with the days shifted, used in section 2.4 of the report. To shift the data, we chose first to filter the data in two different files for each place, called respectively "Falsterbo_GREATER_2", "Falsterbo_LESS_2", "Umeå_GREATER_2", "Umeå_LESS_2". The "GREATER" files report the values of the warmest and coldest days only if they are measured after September, namely after the 270th day of the year, while if the day is before the 270th is reported in the LESS file. In this way, it was possible to make with Excell a new merged-column with all the coldest/warmest day of the "GREATER" file shifted by -270 days, and the coldest/warmest day of the "LESS" file shifted by +95 days. The reason of this shift is explained in the report. Then, it was possible to make the two complete files suitable for all the plots, called "Umeå_final" and "Falsterbo_final".

Now that we have the data files cleaned with the calculations we need for the plots, we can use ROOT to obtain the different plots. In the folder code of this repository you can find six different files with extension ".C", those are the files we need to plot the graphs.On the other hand, in thefinal_filtered folder you can find the file in which we have the data for both locations.
The next step is to download all these files and put them on the same folder. From this folder we are going to start ROOT.
Now with root openned we have to use the flag .L to compile every file with extension .C with the following command: .L NAME_OF_THE_FILE.
The last step to generate the plots is to execute the functions of the files in root. In order to do so, we have to write the name of the function and press enter.
It is not necessary to use any parameter in function as the code is not developed like that. The names we have chosen are for the functions can be seen when the function is defined in the .C file.











