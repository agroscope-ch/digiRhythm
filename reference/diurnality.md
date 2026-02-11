# Computes the diurnality index based on an activity dataframe

Computes the diurnality index based on an activity dataframe

## Usage

``` r
diurnality(
  data,
  activity,
  day_time = c("06:30:00", "16:30:00"),
  night_time = c("18:00:00", "T05:00:00"),
  save = NULL
)
```

## Arguments

- data:

  a digiRhythm-friendly dataset

- activity:

  The number of non-useful lines to skip (lines to header)

- day_time:

  an array containing the start and end of the day period. Default:
  c("06:30:00", "16:30:00").

- night_time:

  an array containing the start and end of the night period. Default:
  c("18:00:00", "T05:00:00").

- save:

  if NULL, the image is not saved. Otherwise, this parameter will be the
  name of the saved image. it should contain the path and name without
  the extension.

## Value

A ggplot2 object that contains the diurnality plot in addition to a
dataframe with 2 col: date and diurnality index

## Examples

``` r
data("df516b_2", package = "digiRhythm")
data <- df516b_2
data <- remove_activity_outliers(data)
activity <- names(data)[2]
d_index <- diurnality(data, activity)

```
