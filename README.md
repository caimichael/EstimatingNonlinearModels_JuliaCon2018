# Estimating Non-Linear Macroeconomic Models in Julia

## Link to the video
The video recording of the talk can be found at this link [here](https://www.youtube.com/watch?v=dFyr8U-SY2M).

## Loading the slides
To convert the Jupyter notebook to slides and serve in your browser:

1. [Install Jupyter](http://jupyter.org/install.html) if necessary
2. Run `jupyter nbconvert slides.ipynb --to slides --post serve` at the command
   line

## Abstract

Sophisticated tools are required to accurately estimate modern economic models, in the face of
unprecedented macroeconomic conditions. The tempered particle filter is a novel method for
filtering nonlinear state space models, surpassing conventional tools in accuracy and
flexibility.

## Description
In this talk, I will highlight StateSpaceRoutines.jl, a repository containing state space
filtering and smoothing methods such as the Kalman filter, Durbin Koopman smoother, and
others. Specifically, I will discuss our latest addition to StateSpaceRoutines.jl, the
“tempered particle filter” (TPF) which was developed by Ed Herbst (Federal Reserve Board of
Governors) and Frank Schorfheide (University of Pennsylvania). TPF provides a robust way to
simulate the distribution of the states and to calculate the likelihood in a general state
space model. Furthermore, I will explain why TPF produces more accurate approximations than
the standard bootstrap particle filter, and provide some results showing this. Because TPF
is an inherently parallelizable algorithm, I will also delve into some details of the
computational implementation and some lessons that we have learned along the way about
Julia's parallel framework. I will highlight a few issues we are still currently facing with
regards to optimizing the performance of TPF. StateSpaceRoutines.jl should prove useful to
economists, statisticians, and those generally interested in Bayesian methods as a
stand-alone suite of tools, which can be used to estimate a variety of both linear and
non-linear state space models. Lastly, I will briefly highlight the NY Fed DSGE team's
recent work on implementing various kinds of heterogeneous agent models, both in discrete
and continuous time, and discuss the relevance of our implementations of TPF and other
sequential Monte Carlo methods to estimating these models in the future.

## Disclaimer

This talk reflects the experience of the author and does not represent an
endorsement by the Federal Reserve Bank of New York or the Federal Reserve
System of any particular product or service. The views expressed in this talk
are those of the author and do not necessarily reflect the position of the
Federal Reserve Bank of New York or the Federal Reserve System. Any errors or
omissions are the responsibility of the author.
