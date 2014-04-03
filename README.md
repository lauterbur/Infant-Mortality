Infant-Mortality
================

Code relating to Propithecus edwardsi infant mortality study

There were some months in which phenology and/or feeding data were not collected. For these months, we replaced the missing data using multiple imputation with predictive mean matching (mi-pmm), after (Marshall et al. 2010), creating 20 complete data sets. We used the MICE package in R (van Buuren and Groothuis-Oudshoorn, 2011) to impute the missing data. This resulted in 20 data sets. All further analyses were performed on each data set separately.

We used the Survival package in R to run the time-dependent Cox PH model (Therneau, 2014).

We used the MuMIn package in R to run the AICc procedure on models including all formative periods, and either the parameter of current fruit and/or leaf abundance for each time step, or the parameter of the previous month's fruit and/or leaf abundance parameter for each time step (Bartoń, 2013).

We then used the mi.inference() command in the norm package in R to pool imputations across the 20 data sets (Schafer, 2013), resulting in a set of coefficients and significance values for each parameter.
