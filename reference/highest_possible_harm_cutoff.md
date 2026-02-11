# Function to calculate the smallest possible harmonic to consider given a sampling frequency. The minimum possible harmonic = 2 x the period of the maximum frequency according to the Shanon theorem. Example: if the sampling period is 15 min, the minimum possible treatable period is 30 minutes and that corresponds to the 48th harmonic (24 hours \* 60 minutes / 48 = 30 minutes)

Function to calculate the smallest possible harmonic to consider given a
sampling frequency. The minimum possible harmonic = 2 x the period of
the maximum frequency according to the Shanon theorem. Example: if the
sampling period is 15 min, the minimum possible treatable period is 30
minutes and that corresponds to the 48th harmonic (24 hours \* 60
minutes / 48 = 30 minutes)

## Usage

``` r
highest_possible_harm_cutoff(sampling_period_in_minutes)
```

## Arguments

- sampling_period_in_minutes:

  The sampling period of the acquired data in minutes

## Value

Returns the smallest possible harmonic (of 24 hours) to consider given a
sampling frequency.
