# Plot a an single actogram over a period of time for a specific variable

Takes an activity dataset as input and plot and save an actogram of the
specified activity column

## Usage

``` r
actogram(df, activity, activity_alias, start, end, save = "actogram")
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

A ggplot2 object that contains the actogram plot

## Examples

``` r
data("df516b_2")
df <- df516b_2
activity <- names(df)[2]
start <- "2020-05-01" # year-month-day
end <- "2020-08-13" # year-month-day
activity_alias <- "Motion Index"
my_actogram <- actogram(df, activity, activity_alias, start, end,
  save = NULL
)
#> Warning: The `size` argument of `element_line()` is deprecated as of ggplot2 3.4.0.
#> ℹ Please use the `linewidth` argument instead.
#> ℹ The deprecated feature was likely used in the digiRhythm package.
#>   Please report the issue to the authors.

print(my_actogram)
```
