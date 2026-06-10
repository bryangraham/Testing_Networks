
## Overview
The code in this package reproduces the figures and empirical illustration included in the the paper "An optimal test for strategic interaction in social and economic network formation between heterogeneous agents" by Andrin Pelican and Bryan S. Graham. The arXiv version of the paper is available [here](https://arxiv.org/abs/2009.00212). The package also includes a tutorial overview of the methods developed in the paper to facilitate adoption by interested researchers.

## Data availability and provenance statement
The "Data" folder includes the Nyakotote network data used in the empirical illustration. Our estimation sample is a (small) extract of the data collected by Joachim De Weerdt for his dissertation research. This research is featured in De Weerdt (2004, _Insurance Against Poverty_) and several other publications (e.g., Comola and Fafchamps, 2014). We are secondary data users. We obtained raw data files directly from Joachim by e-mail request. Our analysis uses only a small subset of the full dataset. These network data appear frequently in the development economics literature as an illustrative/proto-typical village risk-sharing network (e.g., Comola and Fafchamps, 2014).

Researchers interested in the raw data files will need to contact [Joachim](https://www.ifpri.org/profile/joachim-de-weerdt/) directly. Some of Joachim's source data files are also available in [this GitHub repository](https://github.com/bryangraham/short_courses/tree/master).

## Statement about Rights
We certify that the author(s) of the manuscript have legitimate access to and permission to use the data used in this manuscript.

We certify that the author(s) of the manuscript have documented permission to redistribute/publish the data extracts contained within this replication package.

## Summary of Availability
All data used in our paper is included in this archive. We use two data files. The file _Nyakatoke_ArcList.npy_ is a list of all arcs in the Nyakatoke network. The file _Nyakatoke_AttrDict.npy_ includes the household attributes used in our analysis. These files are binary "pickled" Python numpy arrays. 

## Computational requirements
Our analysis was executed in Python 3. Core modules used include _ugd_, _numpy_, _python-igraph_ and _cairocffi_. Other modules, such as _itertools_, are relatively standard. _igraph_ (which requires _cairocffi_) is used to render many of the network visualizations appearing in the paper.

The Nykatoke graph appears as Figure 3 in the paper. We used the "mds" layout algorithm included in _igraph_ to produce this visualization. Due to _igraph_ updates (e.g., the source code used to solve required eigenvalue problems), it is possible that the replication code will render the network slightly differently than what appears in the paper. Such differences have no bearing on our substantive analysis.

Many users may find it easiest to create a dedicated python environment in order to run our code. Details on how to do this are provided in the included Python Jupyter notebooks. 

## Memory, Runtime, Storage Requirements

Users should have little problem running our code on a modern laptop computer. It is possible that simulating the null distributions in the empirical illstrative could take a few hours, depending on the user's machine. We first ran this code over six years ago on a desktop that was half a dozen years old at the time. Modern machines may be considerably faster. All code blocks that are computationally intensive will provide an estimate of total runtime at the outset; note it may take a few minutes to compute this runtime estimate.

## Description of programs/code
 
In the main directory is this readme file and two Python Juypter Notebooks.

The **Testing_for_Strategic_Interaction_Notebook_1.ipynb** notebook replicates the technical figures in the paper, while the **Testing_for_Strategic_Interaction_Notebook_2.ipynb** notebook replicates the Nyakatoke empirical results and figures.

The second notebook includes detailed instructions on how to set-up a Python virtual environment so that the code runs properly. A few specialized packages are called, including the "ugd one". Please read the markdown boxes in the notebooks for detailed instructions and alternative approaches to setting up the needed Python environment.

Good luck! Although we are not able to provide bespoke support for this replication package (or at least any guarantees of such support), we welcome comments and bug reports.

## References

De Weerdt, J. (2004). _Insurance Against Poverty_, chapter "Risk-sharing and endogenous network formation", pages 197 – 216. Oxford University Press, Oxford.

Comola, M. and Fafchamps, M. (2014). "Testing unilateral and bilateral link formation," _Economic Journal_, 124(579):954 – 975.