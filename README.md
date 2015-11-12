## [Kaggle: How Much Did It Rain? II](https://www.kaggle.com/c/how-much-did-it-rain-ii)

he training data consists of NEXRAD and MADIS data collected on 20 days between Apr and Aug 2014 over midwestern corn-growing states. Time and location information have been censored, and the data have been shuffled so that they are not ordered by time or place. The test data consists of data from the same radars and gauges over the remaining days in that month. Please see this page to understand more about polarimetric radar measurements.
File descriptions

    train.zip - the training set.  This consists of radar observations at gauges in the Midwestern US over 20 days each month during the corn growing season. You are also provided the gauge observation at the end of each hour.
    test.zip - the test set.  This consists of radar observations at gauges in the Midwestern US over the remaining 10/11 days each month of the same year(s) as the training set.  You are required to predict the gauge observation at the end of each hour.
    sample_solution.zip - a sample submission file in the correct format
    sample_dask.py - Example program in Python that will produce the sample submission file.  This program applies the Marshall-Palmer relationship to the radar observations to predict the gauge observation.

Data columns

To understand the data, you have to realize that there are multiple radar observations over the course of an hour, and only one gauge observation (the 'Expected'). That is why there are multiple rows with the same 'Id'.

The columns in the datasets are:

    Id:  A unique number for the set of observations over an hour at a gauge.
    minutes_past:  For each set of radar observations, the minutes past the top of the hour that the radar observations were carried out.  Radar observations are snapshots at that point in time.
    radardist_km:  Distance of gauge from the radar whose observations are being reported.
    Ref:  Radar reflectivity in km
    Ref_5x5_10th:   10th percentile of reflectivity values in 5x5 neighborhood around the gauge.
    Ref_5x5_50th:   50th percentile
    Ref_5x5_90th:   90th percentile
    RefComposite:  Maximum reflectivity in the vertical column above gauge.  In dBZ.
    RefComposite_5x5_10th
    RefComposite_5x5_50th
    RefComposite_5x5_90th
    RhoHV:  Correlation coefficient (unitless)
    RhoHV_5x5_10th
    RhoHV_5x5_50th
    RhoHV_5x5_90th
    Zdr:    Differential reflectivity in dB
    Zdr_5x5_10th
    Zdr_5x5_50th
    Zdr_5x5_90th
    Kdp:  Specific differential phase (deg/km)
    Kdp_5x5_10th
    Kdp_5x5_50th
    Kdp_5x5_90th
    Expected:  Actual gauge observation in mm at the end of the hour.

Referencing this data

To reference this dataset in scientific publications, please use the following citation:

Lakshmanan, V, A. Kleeman, J. Boshard, R. Minkowsky, A. Pasch, 2015. The AMS-AI 2015-2016 Contest: Probabilistic estimate of hourly rainfall from radar. 13th Conference on Artificial Intelligence, American Meteorological Society, Phoenix, AZ
