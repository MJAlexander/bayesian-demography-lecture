## Hello!

Here are some materials for a guest lecture given on Bayesian Demography as part of the 'Advanced Demographic Methods' (DEMG7310 / POP514) course. 

## Packages to install

If you would like to follow along with the coded examples, as well as having R and RStudio installed, you will need to install the following packages:

- `tidyverse`
- `rstan`
- `rstanarm`
- `tidybayes`
- `janitor`
- `rcbayes`

The `rstan` package is probably the most important but could be annoying to install. If you have issues, see detailed instructions here: https://github.com/stan-dev/rstan/wiki/RStan-Getting-Started

## Lecture slides

pdf version is [here](https://github.com/MJAlexander/bayesian-demography-lecture/blob/main/slides/bayes_slides.pdf).

## Lab materials

There are three labs written in Quarto files. (in the [`labs`](https://github.com/MJAlexander/bayesian-demography-lecture/tree/main/labs) folder). The data and models required to compile the Quarto documents are also in their respective folders. A pdf version of each lab is listed below. 

- [Gompertz](https://github.com/MJAlexander/bayesian-demography-lecture/blob/main/labs/gompertz.pdf)
- [SVD](https://github.com/MJAlexander/bayesian-demography-lecture/blob/main/labs/svd.pdf)
- [Rogers Castro](https://github.com/MJAlexander/bayesian-demography-lecture/blob/main/labs/rogers_castro.pdf)

## Optional exercise

Here is an optional exercise based on the Gompertz lab. 

1. Download or read in the Deaths and Population data for Quebec from the [Canadian Human Mortality Database](http://www.bdlc.umontreal.ca/chmd/)
2. Plot mortality rates on the log scale for ages 40+ for females in years 1940, 1980, and 2020.
3. Fit a Gompertz model in Stan separately for each year specified above for females aged 40-105. Make some plots that show the estimates for $\log \alpha$ and $\beta$ for each of the years (`geom_point` with `geom_errorbar` would be suitable here)
4. Now fit a dynamic Gompertz model for all years between 1940 and 2020 with a random walk on both $\log \alpha$ and $\beta$. Compare the resulting estimates to those in Step 3. How similar or different are they? What are the advantages and disadvantages of each approach?
5. Rather than a random walk model on $\log \alpha$ and $\beta$ as in 4, imagine you would like to model these parameters with a quadratic function of time. How would you implement this in Stan?
