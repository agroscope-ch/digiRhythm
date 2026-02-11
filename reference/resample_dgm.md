# Change the sampling of a digiRhythm friendly dataset

This function upsamples the data but does not downsample them. The new
sampling should be a multiple of the current sampling period, and should
be given in minutes.

## Usage

``` r
resample_dgm(data, new_sampling)
```

## Arguments

- data:

  The dataframe containing the activity data

- new_sampling:

  The new sampling (multiple of current sampling) in minutes

## Value

A digiRhythm friendly dataset with the new sampling

## Examples

``` r
data("df516b_2", package = "digiRhythm")
df <- df516b_2
df <- remove_activity_outliers(df)
new_sampling <- 30
new_dgm <- resample_dgm(df, new_sampling)
```
