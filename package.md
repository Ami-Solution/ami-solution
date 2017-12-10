---
title: "TSrepr - R package for time series representations"
permalink: /package/
layout: page
---

[**TSrepr**](https://github.com/PetoLau/TSrepr) is **R** package for fast time series **representations** and dimensionality reduction computations. Z-score normalisation, min-max normalisation, forecasting accuracy measures and other useful functions implemented in C++ (Rcpp) and R.

Install `TSrepr` R package from GitHub via `devtools` package (you need it to be installed - `install.packages('devtools')`):

`
devtools::install_github("PetoLau/TSrepr")
`

These representations of time series are implemented so far:
 * PAA - Piecewise Aggregate Approximation (`repr_paa`)
 * DWT - Discrete Wavelet Transform (`repr_dwt`)
 * DFT - Discrete Fourier Transform (`repr_dft`)
 * DCT - Discrete Cosine Transform (`repr_dct`)
 * SMA - Simple Moving Average (`repr_sma`)
 * PIP - Perceptually Important Points (`repr_pip`)
 * SAX - Symbolic Aggregate Approximation (`repr_sax`)
 * PLA - Piecewise Linear Approximation (`repr_pla`)
 * Mean seasonal profile - Average seasonal profile, Median seasonal profile, etc. (`repr_seas_profile`)
 * Model-based seasonal representations based on linear (additive) model (lm, rlm, l1, gam) (`repr_lm`, `repr_gam`)
 * Exponential smoothing seasonal coefficients (`repr_exp`)
 * FeaClip - Feature extraction from clipping representation (`repr_feaclip`, `clipping`)
 * FeaTrend - Feature extraction from trending representation (`repr_featrend`, `trending`)
 * FeaClipTrend - Feature extraction from clipping and trending representation (`repr_feacliptrend`)
 
Additional useful functions are implemented as:
  * Windowing (`repr_windowing`) - applies above mentioned representations to every window of a time series
  * Matrix of representations (`repr_matrix`) - applies above mentioned representations to every row of a matrix of time series
  * Normalisation functions - z-score (`norm_z`), min-max (`norm_min_max`)
  * Normalisation functions with output also of scaling parameters - z-score (`norm_z_list`), min-max (`norm_min_max_list`)
  * Denormalisation functions - z-score (`denorm_z`), min-max (`denorm_min_max`)
  * Forecasting accuracy measures - MAE, RMSE, MdAE, MAPE, sMAPE, MASE


For any suggestions and comments write me an email at: [tsreprpackage@gmail.com](mailto:tsreprpackage@gmail.com)

{% include share-page.html share-page_identifier=page.share-page_identifier %}
