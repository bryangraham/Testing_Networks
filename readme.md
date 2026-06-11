## Overview

The code in this package reproduces the figures and other output associated with the empirical illustration included in the the paper "An optimal test for strategic interaction in social and economic network formation between heterogeneous agents" by Andrin Pelican and Bryan S. Graham. The arXiv version of the paper is available [here](https://arxiv.org/abs/2009.00212). The package also includes a tutorial overview of the methods developed in the paper to facilitate adoption by interested researchers. 

You may cite this replication package as follows:

Pelican, Andrin and Bryan Graham. (2026). *Replication package for: An optimal test for strategic interaction in network formation games* (v1.0) [Replication package]. [Zenodo](https://zenodo.org/). https://doi.org/10.5281/zenodo.19598770

## Data availability and provenance statement

The "Data" folder includes the Nyakotote network data used in the empirical illustration. Our estimation sample is a (small) extract from data originally collected by Joachim De Weerdt for his dissertation research. This research is featured in De Weerdt (2004, _Insurance Against Poverty_) and several other publications (e.g., Comola and Fafchamps, 2014). We are secondary data users. We obtained raw data files directly from Joachim by e-mail request. Our analysis uses only a small subset of the full dataset. These network data appear frequently in the development economics literature as an illustrative/proto-typical village risk-sharing network (e.g., Comola and Fafchamps, 2014).

Researchers interested in the raw data files will need to contact [Joachim](https://www.ifpri.org/profile/joachim-de-weerdt/) directly. Some of Joachim's source data files are also available in [this GitHub repository](https://github.com/bryangraham/short_courses/tree/master).

## Statement about Rights

We certify that the author(s) of the manuscript have legitimate access to and permission to use the data used in this manuscript.

We certify that the author(s) of the manuscript have permission to redistribute/publish the data extracts contained within this replication package.

## Summary of Availability

All data used in our paper is included in this archive. We use two data files. The file **Nyakatoke_ArcList.npy** is a list of all arcs in the Nyakatoke network. The file **Nyakatoke_AttrDict.npy** includes the household attributes used in our analysis. These files are binary "pickled" Python numpy arrays. 

## Computational requirements

Our analysis was executed in Python 3. Core modules used include _ugd_, _numpy_, _python-igraph_ and _cairocffi_. Other modules, such as _itertools_, are relatively standard. _igraph_ (which requires _cairocffi_) is used to render many of the network visualizations appearing in the paper.

The Nykatoke graph appears as Figure 3 in the paper. We used the "mds" layout algorithm included in _igraph_ to produce this visualization. Due to _igraph_ updates (e.g., changes in the source code used to solve required eigenvalue problems), it is possible that the replication code will render the network slightly differently than what appears in the paper. Such differences have no bearing on our substantive analysis.

Many users may find it easiest to create a dedicated python environment in order to run our code. Details on how to do this are provided in the included Python Jupyter notebooks. 

## Memory, Runtime, Storage Requirements

Users should have little problem running our code on a modern desktop computer with a properly configured Python environment. It is possible that simulating the null distributions in the empirical illustration could take a several hours, depending on the user's machine. We first ran this code seven years ago (c. 2019) on a desktop that was half a dozen years old at the time. Modern machines may be considerably faster. All code blocks that are computationally intensive will provide an estimate of total runtime at the outset; note it may take a few minutes to compute this runtime estimate. Although not featured in our replication archive, computing many null distribution draws in parallel would substantially speed up the estimation of reference quantiles for the null distribution of our test statistic.

## Description of programs/code

In the main directory is this readme file and two Python Juypter Notebooks.

The **Testing_for_Strategic_Interaction_Notebook_1.ipynb** notebook replicates the technical figures in the paper, while the **Testing_for_Strategic_Interaction_Notebook_2.ipynb** notebook replicates the Nyakatoke empirical results and figures. This second notebook also includes some basic tutorial material.

The second notebook includes detailed instructions on how to set-up a Python virtual environment so that the code runs properly. A few specialized packages are called, including the "ugd" one. Please read the markdown boxes in the notebooks for detailed instructions and alternative approaches to setting up the needed Python environment.

Our empirical results are based on $B=1000$ draws from the test statistics' null distributions. In the replication archive we set $B=5$ to make it easier and quicker for users to get up and running with the code (e.g., to debug any issues with their Python enviroment). If you would like to replicate the actual empirical results (up to simulation error), in particular Figure 4 in the main paper, just set $B=1000$ in the code. Where to do this is clearly flagged and explained in the **Testing_for_Strategic_Interaction_Notebook_2.ipynb** Jupyter notebook.

Good luck! Although we are not able to provide bespoke support for this replication package (or, more accurately, any guarantees of such support), we do welcome comments and bug reports. We will do our best to assist interested users in adopting our methods.

## References

De Weerdt, J. (2004). _Insurance Against Poverty_, chapter "Risk-sharing and endogenous network formation", pages 197 – 216. Oxford University Press, Oxford.

Comola, M. and Fafchamps, M. (2014). "Testing unilateral and bilateral link formation," _Economic Journal_, 124(579):954 – 975.