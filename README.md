
<!-- README.md is generated from README.Rmd. Please edit that file -->

## zoidtmb

`zoidtmb` is an implementation of the `zoid` package in TMB, using
marginal maximum likelihood instead of Bayesian estimation. This may be
particularly useful for datasets with large dimensions.

The syntax of fitting models matches `zoid`, and can be done with

``` r
fit <- fit_zoidTMB(formula = formula, # required formula
                   design_matrix = design_matrix, # optional covariates
                   data_matrix = data.matrix, # required data matrix
                   overdispersion = FALSE, # optional estimated overdispersion
                   overdispersion_sd = 5, # optional penalty/prior on overdispersion
                   prior_sd = NA) # optional prior/penalty on fixed effects 
```

Parameter estimates and uncertainty can be extracted from

``` r
fit$sdreport
```

Derived quantities (means) are provided with `fit$mu` and uncertainties
`fit$mu_se`.

For additional details, see the documentation for `zoid`,
(<https://github.com/nwfsc-cb/zoid/tree/main>)

## How to cite

Jensen, Alexander J., Ryan P. Kelly, Eric C. Anderson, William H.
Satterthwaite, Andrew Olaf Shelton, and Eric J. Ward. 2022. “
Introducing Zoid: A Mixture Model and R Package for Modeling
Proportional Data with Zeros and Ones in Ecology.” Ecology 103(11):
e3804. <https://doi.org/10.1002/ecy.3804>

## NOAA Disclaimer

This repository is a scientific product and is not official
communication of the National Oceanic and Atmospheric Administration, or
the United States Department of Commerce. All NOAA GitHub project code
is provided on an ‘as is’ basis and the user assumes responsibility for
its use. Any claims against the Department of Commerce or Department of
Commerce bureaus stemming from the use of this GitHub project will be
governed by all applicable Federal law. Any reference to specific
commercial products, processes, or services by service mark, trademark,
manufacturer, or otherwise, does not constitute or imply their
endorsement, recommendation or favoring by the Department of Commerce.
The Department of Commerce seal and logo, or the seal and logo of a DOC
bureau, shall not be used in any manner to imply endorsement of any
commercial product or activity by DOC or the United States Government.

<img src="https://raw.githubusercontent.com/nmfs-general-modeling-tools/nmfspalette/main/man/figures/noaa-fisheries-rgb-2line-horizontal-small.png" height="75" alt="NOAA Fisheries">

[U.S. Department of Commerce](https://www.commerce.gov/) \| [National
Oceanographic and Atmospheric Administration](https://www.noaa.gov) \|
[NOAA Fisheries](https://www.fisheries.noaa.gov/)
