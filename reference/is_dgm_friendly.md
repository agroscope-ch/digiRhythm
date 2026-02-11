# Informs if a dataset is digiRhythm Friendly

Takes an activity dataset as input and gives information about 1) If a
dataset is digiRhythm friendly, i.e., the functions used can work with
this dataset and 2) Tells what's wrong, if any.

## Usage

``` r
is_dgm_friendly(data, verbose = FALSE)
```

## Arguments

- data:

  The dataframe containing the activity data

- verbose:

  if TRUE, prints info about the dataset

## Value

Boolean. If True, the dataframe is digirhythm friendly. If False, the
dataframe is not digirhythm friendly.

## Examples

``` r
data("df516b_2", package = "digiRhythm")
d <- df516b_2
is_dgm_friendly(data = d, verbose = TRUE)
#> v Correct time format: First column has a POSIXct Format 
#> v Number of days good for DFC: 46 days >= 2 days 
#> v Correct numeric format - Column 2 ==> Motion.Index 
#> v Correct numeric format - Column 3 ==> Steps 
#> The data is digiRhythm friendly 
#> [1] TRUE
```
