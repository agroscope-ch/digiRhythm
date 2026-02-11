# Returns p-value of a frequency peak according to pbaluev (2008) given Z, fmax and tm. Reused from the LOMB library (https://rdrr.io/cran/lomb/)

Returns p-value of a frequency peak according to pbaluev (2008) given Z,
fmax and tm. Reused from the LOMB library (https://rdrr.io/cran/lomb/)

## Usage

``` r
pbaluev(Z, fmax, tm)
```

## Arguments

- Z:

  the power of the frequency

- fmax:

  the maximum frequency in the spectrum

- tm:

  the time grid of the original time series

## Value

an intermediate calculation step needed to compute the p-value according
to pbaluev (2008).
