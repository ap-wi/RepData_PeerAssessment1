
### Peer Assessment 1 for Reproducible Research

## Source:

# Dataset: Activity monitoring data [52K]

  "https://d396qusza40orc.cloudfront.net/repdata%2Fdata%2Factivity.zip"

# The variables included in this dataset are:

  steps: Number of steps taking in a 5-minute interval (missing values are coded as NA)
  date: The date on which the measurement was taken in YYYY-MM-DD format
  interval: Identifier for the 5-minute interval in which measurement was taken

# The dataset is stored in a comma-separated-value (CSV) file and there are 
  a total of 17,568 observations in this dataset.

	
## Documents for the assignment

# Description / Ansers / Plots

* PA1_activity_movement.Rmd
* PA1_activity_movement.md	
* PA1_activity_movement.html

* hist_steps_per_day.png
* time_series_of_steps_per_day.png
* time_series_of_steps_per_5min.png
* hist_steps_per_day2.png
* compare_ave_number_of_steps.png


## R-Script my_activity_movement.R

The script includes all functions which are using in the 
R-Markdown PA1_activity_movement.Rmd.

# function main_activity()
    using functions
       read_data_activity() 
       preprocessed_data_activity( df )
       plot_hist_per_day( df, f_screen = TRUE )
       get_mean_median_per_day( df )
       plot_time_series_of_steps( df, f_screen = TRUE )
       plot_time_series_of_steps( df, f_screen = TRUE )
       plot_time_series_of_steps_per_5min( df, f_screen = TRUE )
       my_act_impute <- impute_missing_value( df, df_na )
          using function 
             impute_missing( df, df_na )
       plot_compare_ave_number_of_steps( df, f_screen = TRUE )
    	
1.  Code for reading in the dataset and/or processing the data
1.1 Load the data (i.e. read.csv())
    my_activity <- read_data_activity()  
1.2 Process/transform the data into a format suitable for your analysis
    my_act_list <- preprocessed_data_activity( df = my_activity )
    
2.  Histogram of the total number of steps taken each day
    plot_hist_per_day( df = my_act, f_screen = TRUE )
   
3.  Mean and median number of steps taken each day
    my_mean_median <- get_mean_median_per_day( df = my_act )

4.  Time series plot of the average number of steps taken
    plot_time_series_of_steps( df = my_mean_median, f_screen = TRUE )

5.  The 5-minute interval that, on average, contains the maximum number of steps
    plot_time_series_of_steps_per_5min( df = my_act, f_screen = TRUE )
   
6.  Code to describe and show a strategy for imputing missing data
    my_act_impute <- impute_missing_value( df = my_act, df_na = my_act_na )

7.  Histogram of the total number of steps taken each day after 
    missing values are imputed
    plot_hist_per_day( df = my_act_impute, f_screen = TRUE )
   
8.  Panel plot comparing the average number of steps taken 
    per 5-minute interval across weekdays and weekends
    plot_compare_ave_number_of_steps( df = my_act_impute, f_screen = TRUE )
    
