# Reads Raw Activity Data from csv files

Reads Activity Data (data, time, activity(ies)) from a CSV file where we
can skip some lines (usually representing the metadata) and select
specific activities.

## Usage

``` r
import_raw_activity_data(
  filename,
  skipLines = 0,
  act.cols.names = c("Date", "Time", "Motion Index", "Steps"),
  date_format = "%d.%m.%Y",
  time_format = "%H:%M:%S",
  sep = ",",
  original_tz = "CET",
  target_tz = "CET",
  sampling = 15,
  trim_first_day = TRUE,
  trim_middle_days = TRUE,
  trim_last_day = TRUE,
  verbose = FALSE
)
```

## Arguments

- filename:

  The file name (full or relative path with extension)

- skipLines:

  The number of non-useful lines to skip (lines to header)

- act.cols.names:

  A vector containing the names of columns to read (specific to the
  activity columns)

- date_format:

  The POSIX format of the Date column (or first column)

- time_format:

  The POSIX format of the Time column (or second column)

- sep:

  The delimiter/separator between the columns

- original_tz:

  The time zone with which the datetime are encoded

- target_tz:

  The time zone with which you want to process the data. Setting this
  argument to 'GMT' will help you coping with daylight saving time where
  changes occur two time a year.

- sampling:

  The sampling frequency in minutes (default 15 min)

- trim_first_day:

  if True, removes the data from the first day if it contains less than
  80% of the expected data points.

- trim_middle_days:

  if True, removes the data from the MIDDLE days if they contain less
  than 80% of the expected data points.

- trim_last_day:

  if True, removes the data from the last day if it contains less than
  80% of the expected data points.

- verbose:

  print out some useful information during the execution of the function

## Value

A dataframe with datetime column and other activity columns, ready to be
used with other functions in digirhythm

## Details

This function prepare the data stored in a csv to be compatible with the
digiRhythm package. You have the possibility to skip the first lines and
choose which columns to read. You also have the possibility to sample
the data. You can also choose whether to remove partial days (where no
data over a full day is present) by trimming last, middle or last days.
This function expects that the first and second columns are respectively
date and time where the format should be mentioned.

file \<- file.path('data', 'sample_data') colstoread \<- c("Date",
"Time", "Motion Index", 'Steps') \#The colums that we are interested in
data \<- improt_raw_icetag_data(filename = file, skipLines = 7,
act.cols.names = colstoread, sampling = 15, verbose = TRUE)

## Examples

``` r
filename <- system.file("extdata", "sample_data.csv", package = "digiRhythm")
data <- import_raw_activity_data(
  filename,
  skipLines = 7,
  act.cols.names = c("Date", "Time", "Motion Index", "Steps"),
  sep = ",",
  original_tz = "CET",
  target_tz = "CET",
  date_format = "%d.%m.%Y",
  time_format = "%H:%M:%S",
  sampling = 15,
  trim_first_day = TRUE,
  trim_middle_days = TRUE,
  trim_last_day = TRUE,
  verbose = TRUE
)
#> [1] "Reading the CSV file /home/runner/work/_temp/Library/digiRhythm/extdata/sample_data.csv"
#> Removing the following columns because they are not numeric
#> [1] "First data points ... "
#>              datetime Motion.Index Steps
#> 1 2020-04-30 11:19:47            0     0
#> 2 2020-04-30 11:20:00            6     0
#> 3 2020-04-30 11:21:00            0     0
#> [1] "Last data point ... "
#>              datetime Motion.Index Steps
#> 1 2020-05-16 06:08:00            0     0
#> 2 2020-05-16 06:07:00            0     0
#> 3 2020-05-16 06:06:00            0     0
#> [1] "Minimum Required number of samples per day 76"
#> [1] "Returning a data frame with datetime colum and 2 variable colums"
#> [1] "Total number of samples is 1440 - Total number of days is 15"
print(head(data))
#>              datetime Motion.Index Steps
#> 1 2020-05-01 00:00:00           47    22
#> 2 2020-05-01 00:15:00            8     5
#> 3 2020-05-01 00:30:00           43    14
#> 4 2020-05-01 00:45:00            5     1
#> 5 2020-05-01 01:00:00            3     0
#> 6 2020-05-01 01:15:00            0     0
```
