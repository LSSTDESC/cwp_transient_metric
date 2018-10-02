# The Basic Idea

How well can we analyze (characterize, classify) a particular time varying object from its light curve? And what properties of the set of observations are critical for the the analysis?
The performance of analysis (light curve fit, classification, etc.) for a particular implementation of an algorithm depends on 

1. the observations of the transient itself, as well as 
2. our understanding of the population of transients that went into the algorithm as a training sample or model.

For example, in the case of Type Ia Supernovae (SNIa) light curve fits, (1) is determined by the the set of observations of the supernova while (2) is determined by the aggregate of observations of a large set of SNIa representing the analyzed population termining the model. Given observations from a previous survey, (2) can be partly addressed. So, we will try to focus on (1), though we may have to think about (b) for at least some parts of the survey. Our objective is to build a map from the characteristics of observations to the successful analysis of  the object's light curve. 

For a particular observing strategy of LSST, it is possible that good performance using a particular analysis method might be achieved for a relatively small fraction of objects, either because that selected set of objects were the brightest in the population, or because the objects received a fortuitious set of visits. In this case, the central tendencies of these properties (mean/median) will not be linked to the better analysis, but variations from these central tendencies will be important.


To study the properties of observations that are good for analysis, we need to do the following:
1. Build a set of criteria of properties of the cadence during the lifetime of a transient/variable source that can be used to characterize it. This is the hard one!
2. A set of properties to evaluate the performance of the analysis: This is effectively a set of metrics of the performance of classification/analysis. For classification, this is a function whose input is the sequence of probabilities of each class assigned to the transient by the classification implementation, and its output is a scalar. We should start with the two metrics that we have investigated in ProClam.
3. A set of properties of the transient source: eg. peak brightness in different bands, redshift, lifetime in different bands. Further suggestions welcome !


So, in order to do the (1): we should start by 
a. collecting the basic criteria we need
b. implement them
c. combine them to create compound criterion.

This initial document (which should improve with questions and contributions from everyone) is to have the basic structure for [starting](https://docs.google.com/document/d/11PMjGBe_kfHpaJXiDJtMnAjNvhsoEWng1nuNj8BVEkE/edit?usp=sharing).  Please start adding basic criteria to these two lists of basic and compound criteria for light curves. To do this, one should assume that one has light curves with the fields of measured quantities:

```
mjd,band,flux,fluxerr,ZeroPoint 
```
and a basic criterion should be a function which takes these fields and produces a scalar value. In fact, one can define a few scalar values in this way together (for example by producing a value for each band). 

