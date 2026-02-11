# Returns the periodicity of a digiRhythm dataframe

Returns the periodicity of a digiRhythm dataframe

## Usage

``` r
dgm_periodicity(data)
```

## Arguments

- data:

  a digiRhythm friendly dataframe

## Value

returns a periodicity object of type xts.

## Examples

``` r
data("df516b_2", package = "digiRhythm")
df <- df516b_2
dgm_periodicity(df)
#> 15 minute periodicity from 2020-05-01 to 2020-06-14 23:45:00 
```
