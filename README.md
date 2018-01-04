# Notebooks on (cognitive neuro)science and statistics
I like reading papers about statistical and methodological innovations for (cognitive neuro)science, but I often have difficulties grasping the mathematical details. Simulating and/or implementing the methods myself aided my understanding a lot, so I decided to keep track of these efforts in this repository with Jupyter notebooks. Feel free to use them in whatever way you like.

## Wishlish
Concepts/papers/methods I want to check out in the future:
- 

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
