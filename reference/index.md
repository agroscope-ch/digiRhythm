# Package index

## All functions

- [`actogram()`](https://nasserdr.github.io/digiRhythm/reference/actogram.md)
  : Plot a an single actogram over a period of time for a specific
  variable
- [`daily_activity_wrap_plot()`](https://nasserdr.github.io/digiRhythm/reference/daily_activity_wrap_plot.md)
  : Plot daily average over a period of time for a specific variable.
- [`daily_average_activity()`](https://nasserdr.github.io/digiRhythm/reference/daily_average_activity.md)
  : Plot daily average over a period of time for a specific variable.
- [`df516b_2`](https://nasserdr.github.io/digiRhythm/reference/df516b_2.md)
  : df516b_2 Activity Data Sets
- [`df603`](https://nasserdr.github.io/digiRhythm/reference/df603.md) :
  df603 Activity Data Sets
- [`df625`](https://nasserdr.github.io/digiRhythm/reference/df625.md) :
  df625 Activity Data Sets
- [`df678_2`](https://nasserdr.github.io/digiRhythm/reference/df678_2.md)
  : df678_2 Activity Data Sets
- [`df689b_3`](https://nasserdr.github.io/digiRhythm/reference/df689b_3.md)
  : df689b_3 Activity Data Sets
- [`df691b_1`](https://nasserdr.github.io/digiRhythm/reference/df691b_1.md)
  : df691b_1 Activity Data Sets
- [`df759a_3`](https://nasserdr.github.io/digiRhythm/reference/df759a_3.md)
  : df759a_3 Activity Data Sets
- [`df_act_info()`](https://nasserdr.github.io/digiRhythm/reference/df_act_info.md)
  : Outputs some information about the activity dataframe
- [`dfc()`](https://nasserdr.github.io/digiRhythm/reference/dfc.md) :
  Computes the Degree of Function coupling (DFC), Harmonic Part (HP) and
  Weekly Lomb-Scargle Spectrum (LSP Spec) for one variable in an
  activity dataset. The dataset should be digiRhythm friendly.
- [`dgm_periodicity()`](https://nasserdr.github.io/digiRhythm/reference/dgm_periodicity.md)
  : Returns the periodicity of a digiRhythm dataframe
- [`diurnality()`](https://nasserdr.github.io/digiRhythm/reference/diurnality.md)
  : Computes the diurnality index based on an activity dataframe
- [`diurnality_customTimes()`](https://nasserdr.github.io/digiRhythm/reference/diurnality_customTimes.md)
  : Computes the diurnality index, using different start and end
  definitions for each day and night, based on an activity dataframe
- [`highest_possible_harm_cutoff()`](https://nasserdr.github.io/digiRhythm/reference/highest_possible_harm_cutoff.md)
  : Function to calculate the smallest possible harmonic to consider
  given a sampling frequency. The minimum possible harmonic = 2 x the
  period of the maximum frequency according to the Shanon theorem.
  Example: if the sampling period is 15 min, the minimum possible
  treatable period is 30 minutes and that corresponds to the 48th
  harmonic (24 hours \* 60 minutes / 48 = 30 minutes)
- [`import_raw_activity_data()`](https://nasserdr.github.io/digiRhythm/reference/import_raw_activity_data.md)
  : Reads Raw Activity Data from csv files
- [`is_dgm_friendly()`](https://nasserdr.github.io/digiRhythm/reference/is_dgm_friendly.md)
  : Informs if a dataset is digiRhythm Friendly
- [`levopt()`](https://nasserdr.github.io/digiRhythm/reference/levopt.md)
  : Returns the level given the p-value computed with pbaluev (2008).
  Copied from the LOMB library.
- [`lomb_scargle_periodogram()`](https://nasserdr.github.io/digiRhythm/reference/lomb_scargle_periodogram.md)
  : Computes the Lomb Scargle Periodogram and returns the information
  needed for computing the DFC and HP. A plot visualizing the Harmonic
  Frequencies presence in the spectrum is possible. The function is
  inspired from the Lomb library in a great part, with modifications to
  fit the requirements of harmonic powers and computation of the DFC.
  This function is inspired by the lsp function from the lomb package
  and adapted to add different colors for harmonic and non harmonic
  frequencies in the signal. For more information about lomb::lsp,
  please refer to: https://cran.r-project.org/web/packages/lomb/
- [`pbaluev()`](https://nasserdr.github.io/digiRhythm/reference/pbaluev.md)
  : Returns p-value of a frequency peak according to pbaluev (2008)
  given Z, fmax and tm. Reused from the LOMB library
  (https://rdrr.io/cran/lomb/)
- [`print_v()`](https://nasserdr.github.io/digiRhythm/reference/print_v.md)
  : Print if Verbose is true
- [`remove_activity_outliers()`](https://nasserdr.github.io/digiRhythm/reference/remove_activity_outliers.md)
  : Remove outliers from the data
- [`resample_dgm()`](https://nasserdr.github.io/digiRhythm/reference/resample_dgm.md)
  : Change the sampling of a digiRhythm friendly dataset
- [`timedata`](https://nasserdr.github.io/digiRhythm/reference/timedata.md)
  : timedata Dataset of start and end of day and night
