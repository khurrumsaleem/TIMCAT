## What is TIMCAT?

See the paper.
"William R Stewart, Koroush Shirvan; Capital cost estimation for advanced nuclear power plants" 2021

https://osf.io/erm3g/download

## Quick Install

Use python 3.9

Be sure to update your pip installer which is a python installer:

``pip3 install --upgrade pip``

To install TIMCAT, git clone this package into your preferred location:

``gh repo clone mit-crpg/TIMCAT``

Installing for the first time use which looks at the setup.py file and installs the packages. Run with sudo. If you use
other packages in the code, add the required package to the setup.py file so it will install.

``pip3 install .``

To update, simply reinstall with pip from the TIMCAT directory:

``pip3 install . --upgrade``

(And to uninstall, simply run: ``pip3 uninstall TIMCAT``)

## Usage
As configured, TIMCAT is run by editing input files and their names in cost_sensitivity.py and running
cost_sensitivity.py. 

You must specify the basis table, and the input files. Edit these lines in cost_sensitivity.py:

```python
plant = "PWR12ME"
BASIS_FNAME = (
    "PATHTOFILE/PWR12_ME_inflated_reduced.csv"
)
plant_fname = "inputfile_" + plant + ".xlsx"
```

## File descriptions
#### "PWR12_ME_inflated_reduced.csv"
This is the reference cost data for the PWR12-ME plant. Costs were inflated from 1987 USD in EEDB to 2018 USD.

#### "inputfile_PWR12ME"
This is the input file template for estimating the costs of a new plant. There are 9 tabs: 6 for direct cost categories, 1 for learning inputs, 1 for modularization inputs, and 1 for general plant characteristics. 

#### "inputfile_PWR12ME"
This is the input file template for estimating the costs of a new plant. There are 9 tabs: 6 for direct cost categories, 1 for learning inputs, 1 for modularization inputs, and 1 for general plant characteristics. 


## References
The source cost data was from the Economic Energy Data Base published by the US DOE in 1987. The full dataset can be accessed here: https://rsicc.ornl.gov/codes/psr/psr5/psr-531.html
