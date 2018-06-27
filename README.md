# Notebooks on (cognitive neuro)science and statistics
I like reading papers about statistical and methodological innovations for (cognitive neuro)science, but I often have difficulties grasping the mathematical details. Simulating and/or implementing the methods myself aided my understanding a lot, so I decided to keep track of these efforts in this repository with Jupyter notebooks. Feel free to use them in whatever way you like.

## Wishlish
Concepts/papers/methods I want to check out in the future:

- Pattern component modelling from [Diedrichsen et al. (2011)](http://www.sciencedirect.com/science/article/pii/S1053811911000796).
- Modelling correlated noise in decoding analyses by [van Bergen & Jehee (2017)](https://www.sciencedirect.com/science/article/pii/S1053811917306626).

## Contents
This repo contains notebooks on the following concepts/methods:

- `cv_MANOVA.ipynb`

This extensively annotated notebook contains an implementation of the cross-validated MANOVA method for (searchlight-based) fMRI analysis based on the article by [Allefeld & Haynes (2014)](http://www.sciencedirect.com/science/article/pii/S1053811913011920).

- `haufe_activation_weights.ipynb`

This notebook contains code that is used to invert the weights from linear backward ("decoding") models to forward ("encoding") models based on the article by [Haufe et al. (2014)](https://www.sciencedirect.com/science/article/pii/S1053811913010914). It contains almost no annotation, which is something I still want to do at one point.

- `inverted_encoding_models.ipynb`

This notebook contains an implementation of "inverted encoding models", in which a forward model (features &rarr; brain) is inverted (brain &larr; features), which yields an estimation of the features from a (multivariate) brain pattern. This implementation is based on papers like [Ester, Sprague, & Serences (2015)](http://www.sciencedirect.com/science/article/pii/S0896627315006352) and on the code from Tommy Sprague's [Github](https://github.com/tommysprague/IEM-tutorial).

- `polynomial_regression.ipynb`

Simple notebook with some snippets that implement polynomial regression for the purpose of demonstrating how overfitting works (used it once to create figures for a course I taught).

- `prevalence_inference.ipynb`

I'm pretty proud of this notebook! It contains a fully annotated implementation of "prevalence inference" as described in the paper by [Allefeld, Gorgen, & Haynes (2016)](http://www.sciencedirect.com/science/article/pii/S1053811916303470) and the notebook additionally contains a complete replication of the results (and plots) from the original article. Note that I implemented this method in my own [skbold](https://github.com/lukassnoek/skbold) package in a [separate module](https://github.com/lukassnoek/skbold/blob/master/skbold/postproc/prevalence.py).  

- `prewhitening.ipynb`

A notebook with a simple implementation of prewhitening because I was interested in the "multivariate noise normalization" described in the paper by [Walther et al. (2016)](http://www.sciencedirect.com/science/article/pii/S1053811915011258). I aim to extend this to show prewhitening on actual fMRI data and in the context of RSA.

- `simulation_variance_OLS_parameters.ipynb`

I used this notebook to gain a better intuition what "variance" of statistical parameters actually means. 

- `tikhonov_regression_with_non_sphrerical_prior.ipynb`

I came across this interesting abstract titled "Improving predictive models using non-spherical Gaussian priors" from [Nunez-Elizalde, Huth, & Gallant (2017)](https://www2.securecms.com/CCNeuro/docs-0/5928d71e68ed3f844e8a256f.pdf), which uses a more general form of Ridge regression - called Tikhonov regression - in which you specify a prior on the distribution model's parameters. I tried to implement Tikhonov regression in this notebook, which seems to demonstrate that *if you have a reasonable estimate of the distribution (mean & variance) of the parameters*, your predictions get **much** better. 

- `convert_ovo_to_ovr.ipynb`

For multiclass classification, scikit-learn provides implementations for both "one-versus-one" ("ovo") and "one-versus-rest" ("ovr") classification schemes. This choice affects the structure of the coefficient matrix after fitting (i.e., which column corresponds to which pairwise classification?). I used this notebook to see how I should convert these "ovo" coefficients to the structure of "ovr" coefficients (for the purpose of implementing 'inverting backwards coefficients' from the Haufe et al. paper in my [skbold](https://github.com/lukassnoek/skbold) package).

- `time_domain_decoding.ipynb`

This (draft!) notebook implements the "decoding in the time domain" method by [Loula, Varoquaux, & Thirion (2017)](https://www.sciencedirect.com/science/article/pii/S1053811917306651).

- `linear_distriminant_contrast.ipynb`

After attending the RSA-workshop in Cambridge, I wanted to know how the "linear distriminant contrast" metric "worked" exactly and how to implement it, which is convered in the notebook (along with a quite extensive elaboration on how to generate relatively realistic fMRI data).
