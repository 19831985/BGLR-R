## BGLR: An R Package for (Bayesian) High-Dimensional Regression

The BGLR Package implements a variety of shrinkage and variable selection regression procedures. In this repository we maintain the latest
version beta version. The latest stable release can be downloaded from [CRAN](https://cran.r-project.org/web/packages/BGLR/index.html).

Technical details about the software and the methods implemented, as well as several examples can be found in the following article:

[Genome-wide regression and prediction with the BGLR statistical package (Genetics, 2014)](http://www.ncbi.nlm.nih.gov/pubmed/25009151)

**Installing BGLR from GitHub**

```R
   install.packages(pkg='devtools',repos='https://cran.r-project.org/')  #1# install devtools
   library(devtools)                                                     #2# load the library
   install_git('https://github.com/gdlc/BGLR/')                       #3# install BGLR from GitHub
```

*Note*: when trying to install from github on a mac I got the following error message

```
ld: library not found for -lgfortran
```

I was able to fix it by following the following [advise](http://thecoatlessprofessor.com/programming/rcpp-rcpparmadillo-and-os-x-mavericks-lgfortran-and-lquadmath-error/).

Recent changes:
   - In V.1.0.4 We have implemented models for heterogeneous error variances (example).
   - More recently, in this repository, we:
      - added the possiblity of saving samples of effects in binary files (example),
      - implemented a new method (BRR-groups), this model is similar to BRR but uses one variance parameter per set of predictors (example),
      - added a function that computes, from samples of effects, the contribution of sets of SNPs to variance (example).
            

###Examples
- [Comprehensive list of examples (BGLR-Genetics)](http://www.ncbi.nlm.nih.gov/pubmed/25009151)
- [Using BRR_sets (new method)](https://github.com/gdlc/BGLR-R/blob/master/example_sets.md)
- [Saving effects in binary files & computing window variances (new method)](https://github.com/gdlc/BGLR-R/blob/master/example_saveEffects.md)
- [Shinkage & Variable Selection (Human SNPs) ](https://github.com/gdlc/BGLR-R/blob/master/simulationHumanGenos.md)
            
