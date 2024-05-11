# PyRanuni

Author: Thomas McGeehan  
Created on: Jan 24, 2016

## Overview

PyRanuni is a Python class that implements the Ranuni function often used in SAS. The Ranuni function computes a pseudo-random variable from a uniform distribution. This class aims to replicate the behavior of the SAS function `call ranuni(seed,ranuni)`.

### Functionality

- **Function Name**: PyRanuni
- **Function Purpose**: Compute a pseudo-random variable from a uniform distribution such that:
  - If seed is >0 then 0<ranunix<=1
  - If seed = 0 then use to_char(current_date,'YYYYDDHH24MISS') as the seed
  - If seed <0 then -1<=ranuni<0
- The class supports two scenarios:
  1. Returns a value in (0,1]: `ranuni (25938940)`
  2. Returns a value between (100,500]: `100+(500-100)*ranuni(25938940)`

### Reference

- Fishman, GS, and LR Moore (1982), "A Statistical Evaluation of Multiplicative Congruential Random Number Generators With Modulus (2^^31)-1. J. Amer. Stats. Assoc., 77(377), 129-136

## Usage

### Installation

No installation is required. Simply use the provided Python script.

### Running the Script

1. Make sure you have Python installed on your system.
2. Execute the script `PyRanuni.py`.
3. Optionally, you can provide command-line arguments:
   - `-v` or `--verbose` for verbose mode.
   - `-p` or `--_seed` to specify the random generator seed. Default is 9.

Example: python PyRanuni.py -v -p 12345
