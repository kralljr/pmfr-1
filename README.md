# **pmfr**

[![Build Status](https://travis-ci.org/skgrange/pmfr.svg?branch=master)](https://travis-ci.org/skgrange/pmfr)

## Introduction

The [EPA's Positive Matrix Factorization (PMF) Model](https://www.epa.gov/air-research/positive-matrix-factorization-model-environmental-data-analyses) (EPA PMF) is an unmaintained and Windows-only tool which is used for analysis of environmental data, most commonly for source apportionment of particulate matter (PM) in the atmosphere or water quality analysis. EPA PMF is, by modern standards, clunky and constrained but it still sees wide usage in data analysis activities. When I first encountered this tool, I desired to build an R interface around the core PMF and generalized multilinear engine (ME-2) Fortran programmes to allow for automation and efficient integration of model running and data analysis. However, the core Fortran source is unavailable due to its proprietary nature and seems to have been developed only with Windows in mind so would be a rather large job to port. Therefore, I have committed to using the EPA PMF tool for what it does best and then develop an R package to pick up all the outputs and allow for efficient data analysis. This is the goal of **pmfr**. 

## Installation

To install the development version, install [**remotes**](https://github.com/r-lib/remotes) first, then try this: 

```
# Install pmfr
remotes::install_packages("skgrange/pmfr")
```

## Usage

**pmfr** contains a number of `read_pmf_*` functions which read EPA PMF's outputs into R. Currently, only the `.csv` output format is supported because this was the easiest place to start. 
