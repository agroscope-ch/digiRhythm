# Plot daily average over a period of time for a specific variable.

Takes an activity dataset as input and plot and save the daily average
of the specified activity column

## Usage

``` r
daily_average_activity(df, activity, activity_alias, start, end, save)
```

## Arguments

- df:

  The dataframe containing the activity data

- activity:

  the name of activity

- activity_alias:

  A string containing the name of the activity to be shown on the graph.

- start:

  The start day (in "%Y-%m-%d" format).

- end:

  The end day (in "%Y-%m-%d" format).

- save:

  if NULL, the image is not saved. Otherwise, this parameter will be the
  name of the saved image. it should contain the path and name without
  the extension.

## Value

None

## Examples

``` r
data("df516b_2")
df <- df516b_2
activity <- names(df)[2]
start <- "2020-05-01" # year-month-day
end <- "2020-08-13" # year-month-day
activity_alias <- "Motion Index"
my_daa <- daily_average_activity(df, activity, activity_alias, start, end,
  save = NULL
)

print(my_daa)
```
